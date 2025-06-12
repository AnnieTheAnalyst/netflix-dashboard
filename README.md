# Netlix Dashboard
**Power BI Dashboard for (TV) Shows and Movies**  
*Track TV Shows and Movies by different segments such as country, rating, genres, type and so on*  
 
**Included Files**:  
- `Netflix Dashboard.pbix` - Ready-to-explore Power BI dashboard.  
- `netflix_titles.csv` - Synthetic dataset for practice.
- `Netflix Logo.png` - Netflix logo
- `Country.json`- Geographic data for a custom map
  
## 🖼️ **Dashboard Preview**  
![Dashboard Background](https://github.com/AnnieTheAnalyst/netflix-dashboard/blob/main/netflix%20dashboard%20snapshot.png?raw=true)

---

## 📂 How to Use This Repository  

### For Inspiration  
Explore my *Netflix Dashboard.pbix** to:  
- See how I designed metric calculations or DAX formulas 
- Get ideas for layout, color schemes, and interactive filters.  

### 🛠️ Hands-On Practice Guide

#### 📂 Using `netflix_titles.csv`, practice:
1. **Recreate** the dashboard with your own design
2. **Calculate** these key metrics (after data cleaning):

#### 🔢 Key Metrics to Calculate:
1. **Content Distribution**  
   - Movies vs TV Shows  
   - By release year  
   - By content rating  

2. **Geographic Analysis**  
   - Content by country (using `Country.json`)  

3. **Genre Popularity**  
   - Top 10 genres  


#### 📊 Sample DAX Measures:
```dax
// Core KPIs
Total Shows = CALCULATE(DISTINCTCOUNT(netflix_titles[show_id])) // using DISTINCTCOUNT to handle duplicates
Movies = CALCULATE([Total Shows], netflix_titles[type] = "Movie" )
TV Shows = CALCULATE( [Total Shows], netflix_titles[type] = "TV Show" )

// Additional useful measures
Movie Percentage = DIVIDE([Movies], [Total Shows], 0)
TV Show Percentage = DIVIDE([TV Shows Count], [Total Shows], 0)

```

*Design inspired by [@DataMindsAcademy](https://www.youtube.com/watch?v=Dq2cXSOJRPw&t=624s) (with custom enhancements).*  

---

## 🛠️ Technical Notes  
- **Dataset**: Synthetic data (safe to share).  
- **Compatibility**: Power BI Desktop 2023+.  

---

## 📜 License  
MIT License - Feel free to adapt for your projects (credit for the author as well as myself appreciated).  
