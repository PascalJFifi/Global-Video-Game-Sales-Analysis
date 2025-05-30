# Global-Video-Game-Sales-Analysis


## Project Description

This project analyzes global video game sales data to uncover patterns and trends that can inform marketing strategies for 2017. The analysis focuses on identifying leading platforms, popular genres, and regional user preferences. It evaluates the impact of user and professional reviews on sales, examines sales dynamics across different platforms, and investigates how ESRB ratings influence regional markets. The findings provide insights into profitable platforms and genres while offering data-driven recommendations for campaign planning and market targeting.

## Analysis Highlights

* **Data Loading and Preliminary Observation**: The project begins by loading the video game sales dataset and performing an initial inspection of its structure and contents.
* **Data Preparation**:
    * Column names are converted to lowercase for consistency.
    * The `year_of_release` column is converted to integers, and missing values are initially filled with 0 before being filtered out. Erroneous data, such as DS platform games released before 2004, is removed.
    * Rows with missing 'name' or 'genre' are removed, as these missing values were found to be correlated.
    * Missing values in `critic_score` (51.45% missing) and `user_score` (40.16% missing, 'TBD' values converted to NaN) are filled with 0 to facilitate analysis, with the understanding that these missing ratings might indicate games with low sales or those not offered on major platforms.
    * A `total_sales` column is calculated by summing sales from NA, EU, JP, and Other regions.
    * Missing values in the `rating` column (40.59% missing) are replaced with 'Unrated' for visualization purposes, as these could represent games not yet rated or those in niche markets.
* **Annual Game Releases**:
    * The number of games released annually was sparse between 1980-1994 (fewer than 200/year).
    * A steady rise in releases occurred between 1995-2007, corresponding with the expansion of the industry and new platforms like PlayStation, Nintendo 64, and early Xbox.
    * Game releases peaked between 2007-2008 with over 1,400 games released annually.
    * A decline in releases was observed from 2009-2016, with numbers dropping to around 400-600 annually by 2016. This could be due to market saturation, a shift to quality over quantity, or the rise of mobile gaming (which may not be fully represented in the dataset). The drop in 2016 might also reflect incomplete data.
* **Leading Platforms (by total sales)**:
    * PS2: 1233.56 million
    * X360: 961.24 million
    * PS3: 931.34 million
    * Wii: 891.18 million
    * DS: 802.76 million
    * PS: 727.58 million
    * PS4: 314.14 million
    * GBA: 312.88 million
    * PSP: 289.53 million
    * 3DS: 257.81 million

## Technologies Used

* Python
* Pandas
* Matplotlib
* SciPy (stats)
* Seaborn
* NumPy

## How to Use

1.  Clone the repository:
2.  Navigate to the project directory: `cd Global-Video-Game-Sales-Analysis'
3.  Ensure you have Jupyter Notebook installed.
4.  Open the `games.ipynb` notebook to view the analysis.

## Future Work

* Further investigation into the decline of game releases post-2008.
* Analysis of more recent data if available.
* Incorporating mobile gaming data for a more comprehensive market view.
