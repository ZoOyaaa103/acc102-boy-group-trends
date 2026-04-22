# Public Attention to Selected Boy Groups: A Python-Based Entertainment Marketing Analysis

This project analyses relative Google Trends search interest for Seventeen, EXO, and Stray Kids over the past 12 months. It compares differences in online public attention and explores how these patterns may provide simple insights for entertainment marketing and audience engagement.

**Main notebook:** `notebook.ipynb`  
**Dataset:** `data/google_trends.csv`  
**Requirements:** `requirements.txt`

## 1. Problem & User

This project compares public search attention across Seventeen, EXO, and Stray Kids using Google Trends data. The intended users are entertainment companies, marketing teams, and students interested in audience attention patterns in the music industry.

## 2. Data

The dataset used in this project comes from Google Trends Explore and was accessed on 21 April 2026. The three groups were compared using the same search settings in order to support a fair comparison. The CSV file is included in this repository because it is small and shareable, which makes the project easier to reproduce locally.

### Data details

- Source: Google Trends Explore
- Access date: 21 April 2026
- Region: Worldwide
- Time range: Past 12 months
- Search type: Web Search
- Search terms: Seventeen, EXO, Stray Kids
- File used in this repository: `data/google_trends.csv`

### Key fields

- `Week`: weekly time period
- `Seventeen`
- `EXO`
- `Stray_Kids`

Google Trends values are presented as a relative search-interest index from 0 to 100 within the selected comparison setting. Therefore, the dataset reflects relative public attention rather than absolute search volume.

## 3. Methods

The project was completed in Python using `pandas` for data loading, cleaning, and descriptive analysis, and `matplotlib` for visualisation. The analytical workflow is simple but structured.

- Load the CSV dataset with pandas
- Skip the category row that is not part of the main data table
- Rename the columns to shorter and clearer names
- Convert the `Week` column into datetime format
- Check data types and missing values
- Generate descriptive statistics
- Create multiple visualisations to compare weekly trends, average attention, distribution, monthly patterns, rolling trends, and variation over time

The notebook is organised from top to bottom so that the analytical workflow can be followed clearly.

## 4. Key Findings

- Stray Kids showed the highest relative search interest overall during the selected period.
- Stray Kids also showed the strongest fluctuations, with a wider spread of values and a much higher standard deviation than the other two groups.
- Seventeen and EXO had relatively similar average levels of attention for much of the period, although EXO showed more noticeable increases in the later months.
- The monthly average and rolling-average charts suggest that the differences between groups were not driven only by one or two isolated weeks.
- These patterns may provide simple insights for entertainment marketing, especially when considering campaign timing, promotional focus, and audience engagement.

## 5. How to Run

To run this project locally:

1. Download or clone the repository.
2. Make sure the following files are included:
   - `README.md`
   - `notebook.ipynb`
   - `data/google_trends.csv`
   - `requirements.txt`
3. Install the required packages:

```bash
pip install -r requirements.txt
```

4. Open Jupyter Notebook:

```bash
jupyter notebook
```

5. Open `notebook.ipynb` and run the notebook from top to bottom.

The notebook uses a relative file path for the dataset, so it should run correctly as long as the folder structure is kept the same.

## 6. Demo

A short demo video accompanies this project. It briefly introduces the problem, dataset, analytical workflow, main outputs, and the repository structure.

## 7. Limitations & Next Steps

This project has several limitations.

First, it focuses on only three selected boy groups, so the findings cannot be used to represent the whole entertainment market. The groups were chosen partly to keep the comparison clearer and more balanced, but this also limits the scope of the analysis.

Second, the project uses only Google Trends data. Since the values are relative index scores rather than absolute search volumes, they should not be interpreted as direct evidence of full popularity, fan loyalty, sales, or revenue.

Third, the analysis does not include event-level explanations such as comebacks, concerts, scandals, or major news coverage. As a result, the notebook can identify spikes and broader patterns, but it cannot fully explain the exact reason behind each change in search interest.

Future improvements could include:
- comparing more groups
- using a longer time range
- adding event-based context
- combining Google Trends with other public datasets for a broader view of audience attention
