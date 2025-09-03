
#  Student Results Scraper (BEC Bapatla)

This Python project uses **Selenium** to automatically fetch student results from [BEC Bapatla Student Info Portal](http://becbapatla.ac.in:8080/STUDENTINFO/).  
The script extracts **Roll Number, Name, Total Marks, Percentage, and CGPA** for a range of students and saves the data into a **CSV file**.

---

##  Features
- Supports multiple **regulations** (R20, R18, R14, R10)  
- Handles different **branches** (IT, CSE, ECE, EEE, CIVIL, ME, DS, CB)  
- Works for both **Regular (Y)** and **Lateral (L)** students  
- Automatically saves the results into a **CSV file**  
- Handles missing data gracefully  

---

##  Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/Friendlysiva143/Student_results_scrapping.git
   cd student_results_scraper
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Make sure you have **Google Chrome** installed and download **ChromeDriver** that matches your Chrome version:
   - [Download ChromeDriver](https://chromedriver.chromium.org/downloads)
   - Place it in your system PATH.

---

##  Usage

Run the script:

```bash
python results_scraper.py
```

You will be prompted to enter details:

```
enter regulation R20/R18/R14/R10: 20
enter the year: 22
enter branch IT/CSE(CS)/ECE(EC)/EEE(EE)/CIVI(CE)/MECHANICAL(ME)/DS/CB: CS
enter Regular(Y)/Lateral(L): Y
enter start roll_no: 100
enter end roll_no: 110
```

The script will process the roll numbers and save results in a file like:

```
R20_CS_Y22_Results.csv
```

---

##  Example Output (CSV)

| ROLL NO    | NAME        | TOTAL | PERCENTAGE | CGPA |
|------------|-------------|-------|------------|------|
| y22ACS101 | John Doe    | 2450  | 81.67%     | 8.3  |
| y22ACS102 | Jane Smith  | 2320  | 77.33%     | 7.9  |
| y22ACS103 | No data found | No data found | No data found | No data found |

---

##  Requirements

- Python 3.7+
- pandas
- selenium
- Google Chrome + ChromeDriver

Install using:

```bash
pip install pandas selenium
```

---

##  Notes

- The script only works when the **BEC student info site** is online.  
- Make sure your internet connection is stable.  
- If "No data found" appears, it usually means the roll number does not exist or results are not uploaded yet.

---

##  Author

Developed by ** Siva PRASD ** 
Feel free to fork and contribute 
