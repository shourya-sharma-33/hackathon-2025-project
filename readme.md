
  

#  OneEarth International Hackathon 2025

 
##  Official Hackathons Requirements

  

###  Themes & Challenges

  

AI-Powered Waste Management System
Predictive Analytics for Climate Change Impact
Green Energy Optimization through Data Analytics
AI-Driven Precision Agriculture for Sustainable Farming
Smart Urban Planning with Big Data for Green Cities
###  Conditions and Process

Participate individually or in teams (max. 5 members).
No prior experience required!

  

##  Event Process

  

1. Register & Form Teams (Free Registration)
2. Submit Your Idea via Google Form (https://forms.gle/wEi38tStCtVuoamZ8)
3. Present to Experts & Compete for prizes
4. Final Hackathon & Awards Ceremony
  

##  Key Dates

  

Registration Opens: 01 August 2025
Submission Deadline: 30 September 2025
48-Hour Hackathon & Awards: 24–25 October 2025

  

##  Prizes & Opportunities

  

1st Prize: £1,000
2nd Prize: £500
3rd Prize: £250
£100 prize in each Thematic Category
For Queries: ai@oneearthhackathon.com

  

-------

##  The Project

This Doc will contain:

1. The advancement in our project
2. Explanation of all the relevant tools and concepts we need for our project
3. The plan of this project flowchart all the info
4. The actual docs and presentation are separate, here only just all the plans will be recorded

  

##  Contributors

  

###  Shourya Sharma

Twitter: [shouryasharma33](https://x.com/shouryasharma33)
GitHub: [shourya-sharma-33 (Shourya Sharma)](https://github.com/shourya-sharma-33)

  

###  Hitori

Twitter:
GitHub:

  
## File Structure

**All Plans can be changed later as our discussion will proceed, its just a foundation that i am planning**


1. `Readme.md` file contains thee plan, ideas and project structure
2. Each folder for each part of project explained in its md file, like data analysis, frontend, UI design, Backend etc etc


##  What we will do

  

###  1. Data Collection & Preparation 

  

Task: Collect historical and live climate/environment data.
Sources :
**AI Recommended Data**
-  [NASA Climate Data](https://data.giss.nasa.gov/gistemp/)
-  [Kaggle Climate Datasets](https://www.kaggle.com/datasets?search=climate+change)
-  [NASA POWER API](https://power.larc.nasa.gov/) → real-time global climate data.
-  [OpenWeatherMap API](https://openweathermap.org/api) → current + forecast weather
-  [NOAA Climate API](https://www.ncdc.noaa.gov/cdo-web/webservices/v2) → live + historical climate records.
 

What to do:

- Load historical data using pandas.
- Fetch live data via API calls (`requests` or `httpx`).
- Clean missing values, normalize columns, align formats.
- Merge static + live data if required.
- Split into train/test sets for model training.
  

Output: A clean dataset + live data pipeline ready for ML.

  

---

  

###  2. Model Training (Core Brain)

  

Task: Train a predictive ML model.

What to do:
- Use Scikit-learn (start with Linear Regression / Random Forest).
- Train model using historical dataset.
- Evaluate using metrics like RMSE or MAE.
- Save trained model as `.pkl` using `joblib` or `pickle`.
  

Output: A trained ML model `.pkl` + evaluation report.

  

---

  

###  3. Model Integration with Live Data

  

Task: Connect your trained model with live climate APIs.

What to do:

1. Create a data fetching function:
-- Call chosen API
-- Get real-time data in JSON.
-- Extract relevant features (temperature, rainfall, CO₂, etc.).

2. Preprocess fetched data (scaling/encoding like training data).
3. Pass it into your trained ML model.
4. Return real-time prediction.

  

Output: Model predictions based on current climate conditions.

  

---

  

###  4. Model Explainability (XAI Layer)

  

Task: Show why the model predicts what it does.
What to do:
- Use SHAP or LIME for explainability.
- Generate feature importance plots:
- Example: CO₂ > rainfall > forest cover.
- Visualize live + static feature impacts.
  

Output: Interactive charts showing factor contributions.

  

---

  

###  5. Data Visualization (Graphs, Maps, Live Updates)

  

Task: Create visuals for better insights.
What to do:
- Use matplotlib / plotly for historical trends (e.g., temperature vs year).
- Use folium or plotly choropleth for geographical heatmaps.
- Enable auto-refreshing live charts when new API data arrives.
- Combine historical + predicted + live visuals in one dashboard.

  

Output: Graphs, maps, and charts with real-time updates.

  

---

  

###  6. Scenario Simulator (“What If” Analysis)

  

Task: Let users test scenarios like reducing CO₂ or increasing forest cover.

What to do:

- Accept user inputs:

Example → “Reduce CO₂ by 15%” or “Increase green cover by 20%”.

- Update dataset variables accordingly.
- Re-run prediction pipeline.
- Show new predicted outcome dynamically.

  

Output: An interactive simulator for policy and environmental planning.

  

---

  

###  7. Backend API (Model + Live Data Serving)

  

Task: Serve the ML model + live API integration.

What to do:

- Use FastAPI (preferred) or Flask.

- Create endpoint `/predict`:

1. Accept user input (location, year, scenario).
2. Fetch live API data.
3. Pass processed data to the ML model.
4. Return predictions + explainability metrics as JSON.

  

Output: A fully functional backend serving real-time climate predictions.

  

---

  

###  8. Frontend UI (Dashboard)

  

Task: Build a dashboard for visualization + interaction.

Options:

- Streamlit → faster, simpler, great for hackathons.
- React + Chart.js/Plotly → advanced, more customizable.

  

What to do:

- Add options to:
- Select region/city.
- Get live predictions.
- View historical trends.
- Visualize model explanations.
- Run “what-if” simulations.
- Display real-time graphs and live API-based results.

  

Output: A working interactive dashboard powered by ML + live data.

  

---

  

###  9. Deployment (Make It Live)

  

Task: Deploy the full stack app online.

Options:

- HuggingFace Spaces → best for Streamlit + ML.
- Render / Railway / Heroku → for FastAPI + React setups.

  

What to do:

- Deploy both frontend and backend.
- Set up live API keys via environment variables.
- Test real-time predictions online.

  

Output: A live, accessible web app judges can test instantly.

  

---

  

###  10. Live Prediction Flow (Final Judge Experience)

  

1. Judge opens the dashboard.
2. Selects a city/region.
3. App calls OpenWeatherMap/NASA API → fetches latest conditions.
4. ML model predicts future climate impact instantly.
5. Dashboard shows:
-- Prediction results.
-- Feature contribution charts.
-- Real-time updated graphs + maps.
-- “What if” simulation outcomes.

  

---

