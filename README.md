# Are Longer Books Rated Higher on Goodreads?

**CIS 605 Programming for Data Science · Project · Fall 2026**  
**Student:** Salam Khalid

## Research question
Is the length of a book associated with its average rating on Goodreads?

## Dataset
- **Source:** [Goodreads-books on Kaggle](https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks), uploaded by Soumik
- **Copy used:** `books.csv` in this repository (11,127 rows, 12 columns). The notebook loads it from here, so anyone who runs it gets the same results.

## What is in this repository
| File | What it is |
|---|---|
| `books_project.ipynb` | The full project: the code, its outputs, and a written description of every step |
| `books.csv` | The dataset used in the project |
| `images/` | The four charts produced by the notebook |
| `screenshots/` | Screenshots of the notebook running and its main outputs |

## Steps
1. **Loading and inspection:** loaded the data with Pandas and checked its shape, column types and summary statistics.
2. **Cleaning:** removed books with 0 pages, audiobooks listed with under 20 pages, books with fewer than 10 ratings, and box sets over 1,500 pages, then kept one edition of each book. This left 9,921 books.
3. **Grouping:** split the books into short (up to 200 pages), medium (201 to 400) and long (401 to 1,500).
4. **Analysis:** descriptive statistics with NumPy, a comparison of the three groups with `groupby`, and the correlation between pages and rating.
5. **Visualizations:** a bar chart, a histogram, a scatter plot with a trend line, and a boxplot.

## Main findings
- Long books have the highest mean rating (4.03), compared with short books (3.94) and medium books (3.90).
- The relationship between length and rating is positive but weak (r = 0.187). Length explains only about 3.5% of the differences in ratings.
- Long books are rated more consistently: only 3 of 2,726 long books are rated under 3.0.

Longer books tend to be rated slightly higher, but the effect is small and does not show that length causes higher ratings.

## How to run
Open `books_project.ipynb` in Jupyter and choose **Run → Run All Cells**. It needs Python with Pandas, NumPy and Matplotlib, and an internet connection to load `books.csv` from this repository.
