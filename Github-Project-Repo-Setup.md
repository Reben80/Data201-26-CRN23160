# GitHub Project Repository Setup Guide

This guide will help you organize your DATA 201 project using a clean, professional GitHub structure. This structure keeps your work easy to follow, reproducible, and ready for presentation.

A PDF copy of this guide is also available: [Github Project Repo.pdf](Github%20Project%20Repo.pdf).

---

## Step 1: Create your GitHub repository

1. Go to [GitHub](https://github.com) and click **New Repository**.
2. Name your repository (use a clear project name).
3. Set the repository to **Public**.
   - Use public unless your instructor explicitly tells you otherwise.
4. Initialize with a README file.
5. Click **Create Repository**.

## Step 2: Add your instructor as a collaborator

1. Go to your repository.
2. Click **Settings**.
3. Click **Collaborators**.
4. Click **Add people**.
5. Enter `maisAlraee`.
6. Send the invitation.

## Step 3: Create the required folder structure

GitHub does not let you create empty folders. Create a file inside each folder so Git will track it.

Git does **not** track empty folders. If a folder has no files inside, it will not show up in your repository.

### Create one folder together: `data/raw`

1. Click **Add file** → **Create new file**.
2. In the filename box, type: `data/raw/.gitkeep`

### Repeat for the rest of the folders

Create a `.gitkeep` file in each of these paths:

```text
data/raw/.gitkeep
data/interim/.gitkeep
data/processed/.gitkeep
data/external/.gitkeep
ingestion/notebooks/.gitkeep
ingestion/docs/.gitkeep
ingestion/scripts/.gitkeep
eda/notebooks/.gitkeep
eda/docs/.gitkeep
eda/images/.gitkeep
eda/scripts/.gitkeep
analysis/notebooks/.gitkeep
analysis/docs/.gitkeep
analysis/images/.gitkeep
analysis/scripts/.gitkeep
models/.gitkeep
reports/plan/.gitkeep
reports/final/.gitkeep
reports/figures/.gitkeep
docs/references/.gitkeep
docs/sources/.gitkeep
```

The finished structure should look like this:

```text
data/
├── raw/
├── interim/
├── processed/
└── external/
ingestion/
├── notebooks/
├── docs/
└── scripts/
eda/
├── notebooks/
├── docs/
├── images/
└── scripts/
analysis/
├── notebooks/
├── docs/
├── images/
└── scripts/
models/
reports/
├── plan/
├── final/
└── figures/
docs/
├── references/
└── sources/
```

## Step 4: Understand what goes where

### Data folder

- `raw/` — original data (**do not modify**)
- `interim/` — intermediate files created while cleaning
- `processed/` — final datasets used for analysis
- `external/` — data you obtained from an outside source

### Ingestion folder

Loading and cleaning data.

**Examples:** reading CSV files, fixing missing values.

### EDA (exploratory data analysis)

Graphs, summaries, and early insights.

**Examples:** histograms, correlation plots.

### Analysis folder

Final modeling and results.

**Examples:** statistical models, machine learning.

### Models folder

Saved models or model outputs.

### Reports folder

Presentations and final deliverables, including:

- project plan
- final report

## Step 5: Where your code goes (important)

Put your `.qmd`, `.Rmd`, or `.ipynb` files in:

```text
ingestion/notebooks/
eda/notebooks/
analysis/notebooks/
```

### Scripts (reusable code)

Put `.R` or `.py` files in `scripts/` **inside the matching section**:

```text
ingestion/scripts/
eda/scripts/
analysis/scripts/
```

## Step 6: Naming convention

Use clear, consistent file names:

```text
1.0-initial-data-cleaning.qmd
1.1-eda-summary.ipynb
2.0-final-model.R
```

**Format:** `[number]-[short-description]`

---

## Best practices

- Do **not** modify files in `data/raw/`.
- Keep your folders organized at all times.
- Write clear file names (no random names like `final_final_v2`).
- Add comments in your code.
- Push your work regularly (you will learn this next).

## Final checklist

Before moving on, make sure:

- [ ] Repository is public
- [ ] I am added as a collaborator
- [ ] Folder structure is created
- [ ] You understand where your files go
- [ ] You are ready to start adding code
