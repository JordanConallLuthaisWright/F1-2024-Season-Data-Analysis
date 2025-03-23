# 2024 Monaco Grand Prix – FastF1 Telemetry Analysis

***Analyzing Driver Performance, Tyre Strategy & Team Pace with Python, FastF1, and Matplotlib***

This project explores the **2024 Monaco Formula 1 Grand Prix** using Python and the **FastF1** telemetry library. It demonstrates end-to-end race data analysis: from session loading and telemetry extraction to strategic visualization and predictive modeling.

---

## **Project Aim**
The objective is to perform **technical race analytics** using real telemetry and timing data to:

- Visualize **driver lap time progression and speed traces**.
- Understand **tyre strategies and stint lengths**.
- Compare **qualifying pace and race consistency**.
- Identify **WDC (World Drivers’ Championship) contenders** using theoretical point simulations.

---

## **Technical Skills Demonstrated**
- **Python Data Analysis**: Loading session data using FastF1 and accessing structured objects like laps, telemetry, and weather.
- **Data Preprocessing & Feature Engineering**:
  - Transformed time deltas into seconds for analysis.
  - Filtered quick laps, constructed lap delta and stint length features.
- **Data Visualization with Seaborn & Matplotlib**:
  - Built custom plots: scatterplots, violin/swarm plots, overlays, speed heatmaps.
  - Visualized telemetry on track layout using `LineCollection`.
- **Telemetry Analysis**:
  - Extracted and visualized speed, throttle, brake, gear, and RPM.
  - Compared driver performance across qualifying sectors.
- **Styling & Plot Aesthetics**:
  - Customized team/driver styles using `get_driver_style()` and `get_team_color()`.
  - Sorted legends and reversed axes for intuitive race visuals.
- **Ergast API Integration**:
  - Used the Ergast API to extract driver standings.
  - Simulated maximum possible points to assess championship scenarios.
- **Machine Learning Add-on**:
  - Trained a Gradient Boosting Regressor to predict lap times based on qualifying performance.
  - Evaluated using Mean Absolute Error (MAE).

---

## **Analysis Modules**

### 1. **Charles Leclerc Lap Time Scatterplot**
- Plotted lap number vs lap time for Leclerc with compound color coding.
- Inverted y-axis for improved readability.
- Isolated quick laps to remove outliers and pit laps.

### 2. **Driver-Specific Plot Styling**
- Compared Hamilton, Pérez, Verstappen, Russell, and Leclerc.
- Used built-in FastF1 styles and legend sorting functions.
- Demonstrated custom line widths, alphas, and team color logic.

### 3. **Lap Time Distribution (Top 10 Finishers)**
- Combined violin and swarm plots for visual depth.
- Showcased consistency, compound choices, and pace variability.
- Ordered drivers by finishing position.

### 4. **Race Position Changes**
- Line chart tracking driver positions lap-by-lap.
- Y-axis reversed to show P1 at the top.
- Each driver styled with team color for clarity.

### 5. **Qualifying Lap Time Deltas**
- Horizontal bar plot showing gaps to pole time.
- Color-coded by team.
- Sorted by fastest to slowest qualifier.

### 6. **Speed Heatmap on Track Layout**
- Visualized Leclerc's fastest lap using telemetry.
- Applied color gradient to speed trace with a plasma colormap.
- Generated dynamic segments using `LineCollection`.

### 7. **Telemetry Overlay – Lap Comparison**
- Compared Leclerc vs Piastri speed profiles.
- Mapped speed over distance.
- Used each driver’s team color for differentiation.

### 8. **Tyre Strategy Visualization**
- Horizontal bar chart showing stint length per compound.
- Displayed for all 20 drivers.
- Inverted y-axis to place top finishers at the top.

### 9. **Team Race Pace Comparison**
- Boxplots of quick laps by team.
- Ranked by median lap time.
- Applied team color palette to enhance readability.

### 10. **Championship Contender Logic**
- Pulled standings from Ergast after Round 15.
- Simulated theoretical max points remaining.
- Assessed if each driver could still win the WDC.

---

## **Key Learnings & Outcomes**

### **F1 Telemetry Data Handling**
- Learned to work with multiple session types (Qualifying, Race).
- Mastered extraction of structured telemetry (car data, lap times).

### **Analytical Visualization Techniques**
- Learned to build advanced race plots with Seaborn and Matplotlib.
- Used team and compound-based mappings for context-driven visuals.

### **Strategy and Performance Analytics**
- Developed tire compound timelines and stint breakdowns.
- Compared driver consistency, acceleration/braking zones, and gear usage.

### **End-to-End Project Structuring**
- Followed modular notebook design: loading, transforming, analyzing.
- Documented insights, observations, and applied real-world race logic.

### **Add-on Predictive Modeling**
- Modeled qualifying lap predictions with GradientBoosting.
- Tuned and evaluated model using MAE for performance assessment.

---

## **Potential Extensions**
- Build a **real-time dashboard** using Streamlit for live telemetry overlays.
- Perform **pit stop optimization** using regression models.
- Apply **unsupervised clustering** for compound degradation pattern recognition.

---

## **Contact & Repository Info**
- **Author**: Jordan  
- **Email**: [jordan.c.l.wright@gmail.com](mailto:jordan.c.l.wright@gmail.com)  
- [GitHub Profile](https://github.com/JordanConallLuthaisWright)

### **Repository Structure**
| Folder | Contents |
|--------|----------|
| `F1 2024 Season Data Analysis (1).ipynb` | Jupyter notebooks for each module |
| `fastf1` | Cached or pre-cleaned FastF1 data (excluded via `.gitignore`) |
| `README.md` | Summary overview, run instructions, and image previews |

---

> This project demonstrates the power of **motorsport analytics**—combining data engineering, visualization, and predictive modeling to uncover competitive insights in high-performance environments.
