
# OneEarth International Hackathon 2025
**Website:** [http://oneearthhackathon.com](http://oneearthhackathon.com)

---

## Official Hackathon Requirements

### Conditions and Process

- Participate individually or in teams (maximum of 5 members).
- No prior experience required.

---

### Event Process

1. Register & Form Teams (Free Registration)
2. Submit Your Idea via Google Form → [https://forms.gle/wEi38tStCtVuoamZ8](https://forms.gle/wEi38tStCtVuoamZ8)
3. Present your idea to experts & compete for prizes
4. Final Hackathon & Awards Ceremony

---

### Key Dates

- Registration Opens: **01 August 2025**
- Submission Deadline: **30 September 2025**
- 48-Hour Hackathon & Awards: **24–25 October 2025**

---

### Prizes & Opportunities

- **1st Prize:** £1,000  
- **2nd Prize:** £500  
- **3rd Prize:** £250  
- **Special Prize:** £100 in each thematic category  
- **For Queries:** ai@oneearthhackathon.com

---

# Predictive Analytics for Climate Change Impact

## The Project

We have chosen **Predictive Analytics for Climate Change Impact** as our project.  
This document will contain:

1. Progress and advancements in our project.
2. Explanation of all relevant tools, technologies, and concepts required.
3. Project plan, architecture, and flowcharts.
4. References to other documents and presentations (kept separate).

---

## Contributors

### Hitori
- Twitter:  [hitorii (@panic_coder) / X](https://x.com/panic_coder)
- GitHub: [hitoriiiiiiii](https://github.com/hitoriiiiiiii)

### Shourya Sharma
- Twitter: [shouryasharma33](https://x.com/shouryasharma33)
- GitHub: [shourya-sharma-33](https://github.com/shourya-sharma-33)

### shivraj
- Twitter:  [Shivaraj (@shivaraj215) / X](https://x.com/shivaraj215)
- GitHub: [shivraj](https://github.com/Shivaraj-0001)

### yadnesh
- Twitter:  [Yadnesh (@yadneshx17) / X](https://x.com/yadneshx17)
- GitHub: [yadneshx17](https://github.com/yadneshx17)

### Billu
- Twitter:  [Billu (@aka_billu) / X](https://x.com/aka_billu)
- GitHub: [10xbillu (Gaurav )](https://github.com/10xbillu)

---
## Roles (changeable as per meeting)

### Hitori :
1. **Machine Learning Part** : will train and test the ML model on the dataset
2. **Design** : Not sure but depends on what will be the future 

### Shourya Sharma :
1. Will do the data analysis part
2. Data explainablility chatbot using SHAP and LIME
3. Real time data analysis, fetch data from api and then do it, something on this line

### Shivaraj :
1. Will build the presentation and the video editting part
2. will do the frontend part

### Billu :
1. Backend and testing using Next.js

## Work Flow (changeable as per meeting) 

**Start by Data analysis and Model Training and collective planning with the process**

we will begin with choosing the dataset, and we will parallely analyse (Shourya Sharma) and report (Shivaraj) and train the ML model (Hitori), all the analysis will be in this repo, shivaraj will take it and form a beautiful report and presentation

**Plan, Design and Frontend** 

we will plan what components will be where, like say the chat section on right and and  then real time analysis graph then ML prediction page, you guys know the drill

**Backend and Final Work**
then we will build the final and test it, connect the API to fetch data and train the ML model
impliment the ML model
use the built pipeline to analysis





## File Structure

**Note:** All plans are flexible and subject to change as discussions progress.  
This is just a foundational structure.

1. **`README.md`** → Contains plans, ideas, and project structure.
2. Each project module has its own dedicated folder:
   - Data analysis
   - Frontend
   - UI/UX design
   - Backend
   - Documentation

---

<img src="./PlanFlowChart/pl.svg" alt="Logo" style="width:100%; height:auto;" />


## Project Plan

### 1. Data Collection & Preparation

**Task:** Collect historical and real-time climate/environmental data.


## 🌍 Climate Dataset Overview
**Dataset for Data Analysis and Model Training**
- [Dataset for Data Analysis and Model Training] https://ds.nccs.nasa.gov/thredds/catalog/AMES/NEX/GDDP-CMIP6/ACCESS-CM2/historical/r1i1p1f1/catalog.html

- **Dataset Source**: NASA Earth Exchange (NEX) Climate Data via THREDDS Data Server.
- **Why We Chose This Dataset**:  
  - Reliable and high-quality data from NASA.  
  - Covers multiple climate variables needed for predictive analysis.  
  - Includes historical data + future projections based on climate models.
- **What's Inside the Dataset**:  
  - Multi-dimensional data containing **temperature, precipitation, humidity, wind speed**, etc.  
  - Time-series data: daily values spanning multiple years.  
  - Geo-spatial data: values mapped across different latitudes and longitudes.
- **What We Plan to Do**:  
  - Analyze **historical climate trends** using statistical and visual methods.  
  - Build **predictive models** for future climate impact scenarios.  
  - Extract region-specific data to focus on targeted analysis.
- **Starter Notebook Added**:  
  - Notebook includes steps to **load the dataset** directly into Google Colab.  
  - Covers **dataset exploration**, listing variables, and `.head()` previews.  
  - Provides a clean starting point for further **data cleaning, feature engineering, and modeling**.





---

## 🌐 Live Climate Data APIs (For Future Integration)

I (**Shourya**) have also found a few potential APIs that we might be able to use for **real-time climate data fetching** and **live visualizations** in our project.  
However, I **haven’t tested or verified** them yet, so we’ll discuss these options in our next team meeting before finalizing anything.

Some API ideas (to be reviewed):

- [NASA POWER API](https://power.larc.nasa.gov/) → Global, real-time data.
- [OpenWeatherMap API](https://openweathermap.org/api) → Current + forecasted weather.
- [NOAA Climate API](https://www.ncdc.noaa.gov/cdo-web/webservices/v2) → Historical + live data.

We'll go through these options together and decide if we should integrate **real-time fetching** into our workflow.





**Steps:**
- Load historical datasets using **pandas**.
- Fetch live data via APIs using `requests` or `httpx`.
- Handle missing values, normalize columns, and ensure consistent formats.
- Merge static and live datasets if required.
- Split processed data into training and testing sets.

**Output:** A cleaned dataset + integrated live data pipeline ready for machine learning.

---

### 2. Model Training (Core Brain)

**Task:** Train a predictive machine learning model.

**Steps:**
- Use **Scikit-learn** (start with Linear Regression or Random Forest).
- Train using the historical dataset.
- Evaluate using metrics like **RMSE** or **MAE**.
- Save the trained model as a `.pkl` file using `joblib` or `pickle`.

**Output:**  
- Trained ML model (`.pkl` file).  
- Evaluation report with performance metrics.

---

### 3. Model Integration with Live Data

**Task:** Integrate the trained model with real-time climate APIs.

**Steps:**
1. Create a **data fetching function**:
   - Call the selected API.
   - Get JSON response with real-time data.
   - Extract required features (temperature, rainfall, CO₂ levels, etc.).
2. Preprocess the fetched data (scale, normalize, encode as required).
3. Pass processed inputs into the trained ML model.
4. Return real-time predictions.

**Output:**  
Live predictions based on current climate conditions.

---

### 4. Model Explainability (XAI Layer)

**Task:** Make the model explainable and transparent.

**Steps:**
- Use libraries like **SHAP** or **LIME**.
- Generate feature importance plots.
- Example output: CO₂ > Rainfall > Forest Cover.
- Visualize the contribution of live and static features.

**Output:**  
Interactive charts showing which factors influenced each prediction.

---

### 5. Data Visualization (Graphs, Maps, Live Updates)

**Task:** Create an interactive data visualization dashboard.

**Steps:**
- Use **Matplotlib** or **Plotly** for historical trend graphs (e.g., temperature vs. years).
- Use **Folium** or Plotly Choropleth for geographic heatmaps.
- Enable **auto-refreshing live charts** when API data updates.
- Combine historical, predicted, and real-time visuals in a single dashboard.

**Output:**  
Real-time graphs, maps, and charts.

---

### 6. Scenario Simulator (“What If” Analysis)

**Task:** Allow users to test hypothetical climate change scenarios.

**Steps:**
- Accept custom user inputs:
  - Example: “Reduce CO₂ by 15%” or “Increase forest cover by 20%”.
- Update dataset variables based on user input.
- Re-run the prediction pipeline.
- Display dynamically updated results.

**Output:**  
An interactive simulation tool for testing climate-related policy decisions.

---

### 7. Backend API (Model + Live Data Serving)

**Task:** Serve the ML model and live predictions via API.

**Technology Choice:**  
- **FastAPI** (preferred) or **Flask**.

**Steps:**
- Create an endpoint: **`/predict`**
  1. Accept inputs: location, year, and scenario adjustments.
  2. Fetch relevant live API data.
  3. Preprocess and pass inputs to the ML model.
  4. Return predictions + feature contribution metrics as JSON.

**Output:**  
A functional backend serving real-time predictions.

---

### 8. Frontend UI (Dashboard)

**Task:** Build an intuitive, interactive dashboard.

**Technology Options:**
- **Streamlit** → Quick, simple, ideal for hackathons.
- **React + Chart.js/Plotly** → More customizable, production-ready.

**Features to Include:**
- Region/city selection.
- Live prediction view.
- Historical climate trends.
- Model explainability visualization.
- “What-if” simulations.
- Real-time interactive graphs and API-based insights.

**Output:**  
A user-friendly dashboard powered by ML and live climate data.

---

### 9. Deployment (Make It Live)

**Task:** Deploy the project for judges and participants.

**Options:**
- **HuggingFace Spaces** → Best for Streamlit + ML apps.
- **Render**, **Railway**, or **Heroku** → Ideal for FastAPI + React setups.

**Steps:**
- Deploy frontend and backend separately (or together).
- Configure environment variables for API keys securely.
- Test live predictions before release.

**Output:**  
A fully functional, publicly accessible web app.

---

### 10. Live Prediction Flow (Final Judge Experience)

**Steps:**
1. Judge opens the dashboard.
2. Selects a region or city.
3. Application fetches latest weather/climate data via OpenWeatherMap or NASA APIs.
4. ML model predicts future climate impact instantly.
5. Dashboard displays:
   - Prediction results.
   - Feature contribution and importance charts.
   - Updated graphs and maps.
   - “What-if” simulation outcomes.

---


