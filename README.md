
# Final Project: GOOGLE

## Analysis of Cyclistic Bike Usage: Annual Members vs. Casual Riders

### Introduction

Cyclistic is a fictional company that rents bikes. The marketing director believes the company's future success depends on maximizing the number of annual memberships. Therefore, they want to run a marketing campaign focused on converting casual riders into Cyclistic members.

The company has two types of customers: **Casual** and **Members**:

- **Casual riders**: Purchase single-ride or full-day passes.
- **Members**: Purchase annual memberships.

During the team assembly and task division, I was assigned a question to answer:

**How do Cyclistic annual members and casual riders use the bikes differently?**

The data used spans from August 2023 to July 2024 and was analyzed using Python for data cleaning, exploratory analysis, and creating visualizations.

### Project Structure

The project follows these steps:

1. **Data Collection**: 
    - 12 CSV files corresponding to each month of the analyzed period were used. Each file contains around 500,000 rows.
   
2. **Data Cleaning**:
    - The data was preprocessed to correct date formats, remove extra spaces, and handle missing or NaN values.
    - **Date-time format**: Text columns were converted to `datetime` for consistency. Text columns with missing values were filled with 'None', and numerical columns with 0 to ensure proper data loading into the database.
    - **Outliers handling**: Outliers in ride duration were identified and removed to avoid skewed analysis results.

3. **Exploratory Analysis**:
    - Statistical analyses were conducted to understand usage patterns. These include:
        - **Average ride duration**: Key differences between casual riders and annual members.
        - **Rides by day of the week**: Analysis of which days each user type prefers.
        - **Time of day**: Distribution of rides by hour to understand commuting habits.

4. **Visualization**:
    - Charts were created using `matplotlib` and `seaborn` to visualize key metrics such as ride durations, usage by day of the week, and time of day. 

### Key Findings

#### Total Trips per Month
- **Annual members** and **casual cyclists** show a considerable decrease in bicycle use during the winter season.

#### Ride Duration
- **Annual members** tend to use the bikes for shorter and more frequent rides, possibly as part of their daily routines (e.g., commuting to work or school).
  
#### Usage by Day of the Week
- **Annual members** show higher activity during the weekdays, especially during peak hours (8 AM and 5-6 PM), reinforcing the hypothesis that they use bikes for regular commuting.
- **Casual riders** prefer weekends, with more usage during the afternoon, indicating that their trips are more leisure-related.

#### Usage by Time of Day
- **Annual members** concentrate their use in the morning and afternoon hours, which is common during their daily commute.
- **Casual riders** focus their usage in the afternoon, showing a considerable increase between 4 PM and 6 PM.

### Recommendations

- Offer weekend deals since casual riders use bikes more frequently on weekends.
- Promote afternoon deals, as casual riders have a higher usage concentration during the afternoon.
- Summer promotions, as casual riders are more active during the summer months.

### Technologies Used

- **Python**: Used for data cleaning, analysis, and visualization.
  - Libraries: `pandas`, `matplotlib`, `seaborn`, `numpy`
- **MySQL**: Used for storing preprocessed data.
- **Git**: Version control for the project.

### File Structure

1. **`/data`**:
   - [Archivos csv](https://divvy-tripdata.s3.amazonaws.com/index.html)

2. **`/notebooks`**:
   - **`clean_data.ipynb`**: Jupyter notebook for data cleaning. It corrects date formats, handles NaN values, and prepares the data for MySQL loading.
   - **`visualizations.ipynb`**: Jupyter notebook for generating the visualizations used to demonstrate differences in bike usage.

3. **`requirements.txt`**:
   - Lists all the dependencies needed to run the Python scripts, including:
     - `pandas`, `matplotlib`, `seaborn`, `numpy`, `mysql-connector`

4. **`README.md`**:
   - Documentation file that explains the project, its purpose, and how to reproduce the analysis.


### Instructions to Reproduce the Project

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Tomas-Quero/Final-Project-Google-data-analysis
   cd Final-Project-Google-data-analysis
   ```

2. **Install dependencies**:
   Run the following command to install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the analysis**:
   Execute the scripts or Jupyter notebooks to generate the analysis and visualizations.

