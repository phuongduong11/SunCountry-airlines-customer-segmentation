# ✈️ Sun Country Airlines Customer Segmentation Analysis

## Project Purpose
This project aims to enhance Sun Country Airlines’ marketing strategy through customer segmentation analysis. By applying **K-Means clustering**, the analysis identifies meaningful customer segments based on booking behaviors and demographic data, enabling more personalized engagement and improved operational efficiency.

## Dataset Description

Used three main datasets derived from internal airline booking data:
- **`sample_data_transformed.csv`** – Original customer booking dataset with mixed categorical and numeric features.
- **`Clustering Data.csv`** – Cleaned and encoded version (converted category variables to numerical values) used for modeling.
- **`final_dataframe_clusters.csv`** – Final data frame with assigned cluster labels 

**Data Dictionary:**
| Column Name        | Description                                                   |
|--------------------|---------------------------------------------------------------|
| `uid`              | Unique identifier for each customer                           |
| `age_group`        | Categorized customer age group (0–17, 18–24, etc.)            |
| `true_origins`     | Departure location                                            |
| `true_destination` | Actual landing location                                       |
| `final_destination`| Final destination of the passenger                            |
| `rountrip`         | 1 if the trip was a round trip and 0 if one way                     |
| `group_size`       | Number of people in the booking group                         |
| `group`            |1 if travel in group and 0 if travel solo                    |
| `seasonality`      | Booking season (Q1–Q4)                                        |
| `days_prebooked`   | Days between booking and departure                            |

## Methodology

### 1️⃣ Data Preprocessing
- Checked for null values and normalized numerical fields.
- Encoded categorical features (age group, trip type, etc.) for clustering.

### 2️⃣ K-Means Clustering
- Applied the elbow method to determine the optimal number of clusters.
- Set K=5 based on the curve’s inflection point
- Assigned customers to one of five clusters based on booking behavior and demographics.
- Merged cluster labels into final dataset for analysis and visualization.

### 3️⃣ Visualization & Interpretation
Visualized behavior across clusters to understand customer characteristics:
- Age distribution by cluster
- Group size, booking channels, and trip type
- Days prebooked and roundtrip preferences
- Travel seasonality (Q1–Q4)

## Key Insights

### **Segment 1: Family & Organized Travelers** (cluster 0)
- Mostly 55+ travelers, with minors in group travel.
- Long pre-booking periods, especially in Q1 and Q4.
- Prefer booking via Sun Country website or agents.
- **Marketing Strategy**: Promote warm weather getaways and spring break family packages.

### **Segment 2: Career-driven Travelers** (cluster 1)
- Young-to-mid age professionals.
- Book one-way tickets via external channels.
- Prefer flexible booking and economy class.
- **Marketing Strategy**: Offer easy rebooking/cancellation options and corporate rewards.

### **Segment 3: Planned & Seasonal Travelers** (cluster 2)
- Middle-aged and senior travelers.
- Strong Elite program presence.
- Prefer direct booking and winter vacations.
- **Marketing Strategy**: Promote premium packages, loyalty perks, and early bird deals.

### **Segment 4: Seasonal Travelers & Self-Service Bookers** (cluster 3)
- Mix of families and working adults.
- Heavy use of direct website booking.
- Book for Q3 and Q4 holidays in advance.
- **Marketing Strategy**: Boost website UX, offer family vacation bundles.

### **Segment 5: Independent & Improvised Visitors** (cluster 4)
- Even age mix, low loyalty membership.
- Book close to travel date via outside channels.
- **Marketing Strategy**: Incentivize direct booking, mobile app promotions.

## Business Recommendations
- **Invest in Mobile App UX**: Enable personalized travel deals, track loyalty status.
- **Partner with T-Mobile or Wi-Fi providers**: Improve in-flight digital experience.
- **Loyalty Expansion**: Encourage Ufly membership across low-engagement segments.

## Conclusion
This customer segmentation project analyzes booking behavior using K-Means clustering to uncover five distinct customer personas. The insights inform actionable marketing and loyalty strategies that Sun Country Airlines can leverage to enhance customer experience, increase engagement, and drive revenue growth

## 🛠 Tools Used
- **Python**
  - `pandas`, `numpy` – Data manipulation
  - `matplotlib`, `seaborn` – Visualization
  - `scikit-learn` – K-Means clustering, preprocessing
- **Jupyter Notebook** – Interactive exploratory analysis

## 📂 Repository Files
- `Clustering.ipynb` – Full segmentation notebook
- `README.md` – Project documentation
- `sample_data_transformed.csv` – Original dataset
- `Clustering Data.csv` – Preprocessed dataset used for modeling
- `final_dataframe_clusters.csv` – Dataset with cluster labels
  
