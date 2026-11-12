<p align="center">
  <img src="../01_Background/images/banner_1.svg" alt="Data Interpretation — Blue Carbon Eelgrass Workshop banner" width="100%">
</p>

*From sediment samples to carbon-stock estimates.*

[← 3 — Field Methods](../03_Field_Methods/) · [Back to main guide](../README.md)

---

> The guide covers field-to-lab preparation and includes a separate [Community Analysis, Mapping, and Reporting](#community-analysis-mapping-and-reporting) walkthrough. See [resource availability](../resources.md#pending-materials) for materials still in development.

## Overview

This section covers what happens after the cores come out of the field: prepping your samples,
digitizing your field sheet, sending samples to a lab, checking what comes back, and turning it
into a carbon stock you can report.

It follows WWF-Canada's field guide (*Part 3: Sample Analysis* and *Part 4: Calculating Carbon
Stocks*, pp. 15–19 of the [Coastal Blue Carbon Field Guide](https://wwf.ca/wp-content/uploads/2026/04/Coastal-Blue-Carbon-Field-Guide-FINAL.pdf)),
with a dedicated [Lab Guide](../resources.md#pending-materials) for the laboratory procedures, alongside
Howard et al. (2014).

Everyone follows the same four steps. They take you from bagged samples to checked core stocks
that can be compared with each other. Then the path splits, depending on the question you chose
in [Part 2](../02_Project_Planning/):

| # | Step | Answers |
|---|------|---------|
| 1 | **[From the field to the lab](#step-1--from-the-field-to-the-lab)** | *How do I prep samples, digitize my data, and find a lab?* |
| 2 | **Enter the lab results** *(planned)* | *Where does each number from the lab go?* |
| 3 | **Check the data** *(planned)* | *Is anything missing, mislabelled or inconsistent?* |
| 4 | **Core stocks on a common footing** *(planned)* | *How much carbon is in each core, to which depth?* |
| A | **Option A — our cores, and how they compare** *(planned)* | *What do our samples tell us, and how do they compare?* |
| B | **Option B — an estimate for a defined area** *(planned)* | *What do our measurements imply for this meadow or study area?* |
| 5 | **Report the results** *(planned)* | *What do I report, and what does each number mean?* |

Files: the
> [example digital data sheet](../resources.md#pending-materials), the
> [example lab results sheet](../resources.md#pending-materials) and the
> [community analysis workflow](#community-analysis-mapping-and-reporting).

---

## Step 1 — From the field to the lab

You come back from the field with two things:

1. **A cooler of bagged samples**, which need to be processed and prepped for the lab.
2. **A completed paper field data sheet**, which needs to be digitized.

<p class="resource-note">The field-sheet and sample-bag illustration is being prepared.</p>

*What to notice: every bag label matches a row on the field sheet — Core ID, Sample ID and depths.
This is the **constructed Tsawwassen** field example; from Step 2 onwards the analysis uses the
published Cowichan cores, which have no paper sheet of their own.*

The rest of this step deals with each in turn, then with getting the samples analysed.

> 🎥 **Watch:** [*Processing cores*](https://www.youtube.com/shorts/wZccCeFPZqY) — a short
> walkthrough of what sample processing looks like.

---

### 1.1 Digitize the data sheet

*Type your field notes into the digital sheet, which calculates the rest for you.*

The paper datasheet records information at two levels, and the digital sheet keeps them on two
separate tabs for that reason: some things are true of the **whole core**, and some are true of a
**single slice**.

The examples in these two tables are the **constructed Tsawwassen** field example (Part 3).

**Recorded once per core** — the *Plot & Core Log* tab:

| Field | What it is | Example |
|---|---|---|
| Plot ID | The plot the core was taken in | `WWF-01` |
| Core ID | Unique identifier: site, plot, sampling location | `WWF-01-A` |
| Date / Time | When the core was taken | 2026-06-16, 10:45 |
| Study area / site | Location | Tsawwassen Beach |
| Latitude / Longitude | Coordinates of the core | 49.033540, −123.131287 |
| Photo series ID | Links the core to its photo record | `WWF-01-A-P` |
| Weather / tidal conditions | Context for the sampling day | Partly cloudy, low tide |
| Corer internal diameter (cm) | Only if this core used a different tube from the one on the Instructions tab — **measure it, don't assume it** | *(blank)* |
| Outside depth (cm) | How far the corer was driven in (penetration) | 65.0 |
| Inside depth (cm) | Length of core actually recovered | 58.0 |
| Stratum (code) | The stratum from your sampling design, if you stratified | `Zone 3` |

**Recorded once per slice** — the *Sample Data* tab:

| Field | What it is | Example |
|---|---|---|
| Core ID | Must match the Core Log exactly | `WWF-01-A` |
| Sample ID | Slice number, counting down from the surface | 1 |
| Top depth (cm) | Top of the slice, measured down the core | 0 |
| Bottom depth (cm) | Bottom of the slice | 5 |
| Notes | Texture, colour, roots, shell, rocks | Dense live root mat, dark brown silty clay |

> 📸 **[SCREENSHOT NEEDED]** — the completed paper field data sheet.
>
> 📸 **[SCREENSHOT NEEDED]** — the same sheet digitized, so readers can see how one transfers
> onto the other.

**The digital data sheet**

**📊 [Blank digital data sheet — availability](../resources.md#pending-materials)**
· filled-in example: [`files/Eelgrass_Carbon_DigitalData_Example.xlsx`](../resources.md#pending-materials)
· works in Excel, LibreOffice and Google Sheets (*File → Import*)

<!-- TODO (Cathal): an online Google Sheets copy used to be linked here; it predated the 2026 revision. Re-upload the blank .xlsx and link it here if you want an online copy. -->

The workbook has four tabs, in the same order as the workflow:

| Tab | What it holds | Do you type in it? |
|---|---|---|
| **1. Instructions** | Legend, colour key, units — and three settings: your **corer's internal diameter** and the **LOI equation** (intercept and slope) | Only the three settings |
| **2. Plot & Core Log** | One row per core — plot/core notes, insertion depths, stratum | Yes |
| **3. Sample Data** | One row per slice, in five bands: field · calculated · lab · calculated · check | Yes |
| **4. Core Summary** | Per-core totals and standard depth increments, calculated automatically | No |

Only the **yellow cells** are for typing. Everything grey is a formula — depth interval, volume,
compaction factor, and, once lab results arrive, bulk density and carbon stock.

> ⚠️ **Core IDs must match across tabs.** The compaction factor and corer diameter are looked up
> from the Core Log by Core ID. If the ID on the *Sample Data* tab doesn't match, those cells stay
> blank rather than silently using another core's geometry.

---

## Community Analysis, Mapping, and Reporting

Follow a worked example from a completed sediment data sheet to carbon-stock
estimates, maps and a Quarto report. The example uses **12 cores and 120 sediment
sections with simulated measurements**. It is a separate exercise from the
field-to-lab example above.

[Open the Community Blue Carbon Analysis and Mapping repository](https://github.com/CathalD/BlueCarbon_Community_Carbon_Analysis_Mapping)
· [Setup and run instructions](https://github.com/CathalD/BlueCarbon_Community_Carbon_Analysis_Mapping#run-the-workshop)

### 1. Check the completed data sheet

Open the [example field workbook](https://github.com/CathalD/BlueCarbon_Community_Carbon_Analysis_Mapping/blob/main/data/field/blue_carbon_field_cores.xlsm)
and find the **3. Sediment Data** tab. Each row represents one section of a core.
Match the plot and core IDs across the workbook. Check that section depths are
in order, the units are correct, and dry bulk density and organic carbon values
are present or flagged for review. Keep measured zeros distinct from missing
values. The example includes core locations and a study boundary so you can
take the same data through to a map.

[![Example Sediment Data tab with core IDs, section depths, bulk density and organic carbon inputs](images/community-analysis-data-sheet.png)](images/community-analysis-data-sheet.png)

### 2. Run the analysis and explore the maps in R

Download the analysis repository. Install R, Quarto and the R packages listed
in the setup instructions. Open the downloaded folder as your working directory
in R or RStudio, then run:

```r
source("Run_and_Visualize.R")
view_plot("cores")
view_map(30)
view_table("totals")
```

The runner calculates carbon stock for each core at the 30, 50 and 100 cm targets.
It sums carbon down to the target or to the sampled bottom, whichever comes first.
Check the core summary and the number of shorter or flagged cores before comparing
results at the same depth. Use `view_plot("cores")` to compare the sampled cores
and `view_map(30)` to explore estimates across the study area. Switch between the
stock and uncertainty layers to see where estimates are more or less precise.

[![R console running the workshop analysis and showing the example core-stock summary](images/community-analysis-r.png)](images/community-analysis-r.png)

[![Example 0–30 cm carbon-stock map with core locations, a study boundary and a menu for stock and uncertainty layers](images/community-analysis-map.png)](images/community-analysis-map.png)

*The 0–30 cm map shows the local Matérn stock estimate for the simulated example. White dots mark the core locations.*

### 3. Read and report the results

Open `Blue_Carbon_Report.html` in your browser after the run finishes. The
[Quarto report source](https://github.com/CathalD/BlueCarbon_Community_Carbon_Analysis_Mapping/blob/main/Blue_Carbon_Report.qmd)
contains the methods, tables, figures and interactive maps.

Start with **Summary** to check how many cores contributed at each depth. At
the 30 cm target, the example mean across the 12 cores is **2.96 kg C/m²**.
In **Stock across the study boundary**, compare how the estimated total varies
by method. For your own report, state the depth, study boundary and area,
number of usable cores, estimation method and uncertainty. Keep stock per unit
area (kg C/m²) distinct from the estimated total for the study area (Mg C).

[![Quarto report summary with the simulated-data note and stock table by depth](images/community-analysis-report-summary.png)](images/community-analysis-report-summary.png)

[![Quarto report chart comparing study-area stock estimates and uncertainty by method and depth](images/community-analysis-report-totals.png)](images/community-analysis-report-totals.png)
