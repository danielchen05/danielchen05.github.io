---
layout: page
title: Detecting Homozygous Deletions from Single-Cell DNA Sequencing Data
description: Statistical methods for detecting focal homozygous deletions from low-coverage single-cell DNA sequencing data
img: assets/img/qsure_cover.jpg
importance: 2
category: featured
related_publications: false
github: https://github.com/danielchen05/scDNA-homozygous-deletions
------------------------------------------------------------------

This project developed statistical methods for detecting **focal homozygous deletions from low-coverage single-cell DNA sequencing data**. The central goal was to identify small genomic regions with unusually depleted sequencing signal by pooling evidence across cells, particularly in settings where conventional copy-number segmentation methods may miss short or heterogeneous events.

This work was conducted during the **2026 Quantitative Sciences Undergraduate Research Experience (QSURE)** at Memorial Sloan Kettering Cancer Center, under the mentorship of Andrew McPherson, PhD, and Matthew Myers, PhD, in the Computational Oncology Service.

---

## Overview

Single-cell DNA sequencing enables the study of copy-number variation and genomic heterogeneity at cellular resolution. However, detecting small homozygous deletions is challenging because single-cell whole-genome sequencing data are typically sparse and noisy, with many genomic positions receiving few or no reads.

Standard copy-number methods are often designed to identify larger chromosomal alterations and may have limited sensitivity for focal events spanning only one or a few genomic bins.

This project investigated whether a **deletion-specific statistical scan** could improve detection of these focal events. I benchmarked existing changepoint and segmentation methods, investigated their failure cases, developed a one-sided scan statistic that pools evidence across cells, evaluated the method through simulation studies, and applied the resulting workflow to real single-cell DNA sequencing datasets.

---

## My Contributions

* Benchmarked existing changepoint detection and segmentation approaches for focal deletion detection.
* Designed simulation frameworks spanning sequencing coverage, deletion size, cell number, carrier fraction, and genomic bin size.
* Investigated failure cases of existing methods for short and low-signal deletion events.
* Developed and implemented a **one-sided scan statistic** specifically targeting local depletion in sequencing read counts.
* Extended the method to pool evidence across multiple cells and estimate likely deletion carriers.
* Stress-tested the method across a wide range of simulated single-cell DNA sequencing scenarios.
* Developed a modular Python workflow for applying the scanner to real patient datasets.
* Applied the workflow to samples from the **MSK-SPECTRUM** cohort to identify candidate homozygous deletion events.

---

## Methods

The project combined simulation-based benchmarking, statistical method development, and real-data analysis.

### 1. Simulation framework

Synthetic single-cell read-count data were generated under varying experimental and biological conditions, including:

* sequencing coverage,
* number of cells,
* genomic bin size,
* deletion length,
* deletion carrier fraction, and
* background count variability.

Simulated homozygous deletions were introduced as localized reductions in expected read counts. These experiments were used to quantify detection performance and characterize regimes in which existing methods succeed or fail.

### 2. Benchmarking existing methods

Several changepoint and segmentation strategies were evaluated as candidate approaches for detecting focal deletions.

Performance was assessed using metrics including **recall**, localization accuracy, and false-positive behavior across different deletion sizes and sequencing depths.

The benchmarking results showed that very short events, particularly those spanning only one or two genomic bins, posed a major challenge for general-purpose segmentation approaches.

### 3. One-sided scan statistic

To directly target the signal of interest, I developed a **one-sided scan statistic** designed to detect genomic intervals with unusually low read counts relative to their local background.

Rather than first estimating discrete copy-number states, the method operates directly on binned sequencing read counts. Because read depth is approximately proportional to underlying DNA copy number after normalization and bias correction, homozygous deletions are expected to produce localized depletion in the observed signal.

The statistic pools evidence across cells, increasing sensitivity to recurrent or subclonal events that may be difficult to identify from individual cells alone.

### 4. Carrier inference

For candidate deletion intervals, cell-level evidence can be evaluated to estimate which cells are most consistent with carrying the event.

This allows the workflow to move beyond identifying a genomic interval and toward characterizing **cellular heterogeneity** in deletion status.

### 5. Real-data workflow

The final workflow was implemented in Python for application to binned single-cell DNA sequencing data.

The pipeline includes:

* sample and cell filtering,
* genomic blacklist construction,
* rebinning of raw read-count data,
* scan-statistic calculation,
* candidate interval ranking,
* cell-level posterior evaluation, and
* visualization of candidate homozygous deletion events.

The workflow was initially applied to single-cell whole-genome sequencing data from the **MSK-SPECTRUM** cohort.

---

## Selected Results

Simulation studies showed that detection performance depends strongly on the size of the deletion relative to the genomic bin size and on the amount of sequencing information available.

The deletion-specific one-sided scan performed particularly well for **short focal events**, where conventional segmentation approaches were more likely to smooth over or miss the signal.

The simulations also demonstrated an important limitation of low-coverage single-cell data: very small deletions carried by only a small fraction of cells remain intrinsically difficult to detect. Increasing the number of cells improves sensitivity to rarer events by allowing evidence to accumulate across the population.

Application to real patient datasets produced candidate focal deletion intervals for downstream biological review and comparison with existing copy-number calls.

---

## Tools

`Python` · `statistical genomics` · `single-cell DNA sequencing` · `scan statistics` · `changepoint detection` · `simulation` · `AnnData` · `Snakemake`

---

## Status

The core statistical method and real-data scanning workflow were developed during QSURE 2026 and evaluated through extensive simulation studies and exploratory analysis of the MSK-SPECTRUM cohort.

The project is continuing with applications to additional cancer datasets, including analyses aimed at characterizing genomic heterogeneity and chromosomal instability.
