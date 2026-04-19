# Strava API to Excel

This project uses Python to extract activity and gear data from the Strava API and export it into a structured Excel file.

It is implemented as a step-by-step Jupyter Notebook covering authentication, data retrieval, processing, and export.

---

## 🚀 Overview

The notebook follows a 4-step workflow:

1. Install required libraries
2. Generate an authorization code via Strava
3. Exchange the code for an access token
4. Fetch, process, and export data to Excel

---

## 🔑 Prerequisites

Before running this project, you must:

* Have a Strava account
* Create an application via the Strava API
* Obtain:

  * Client ID
  * Client Secret

---

## 🔐 Authentication Flow

1. Open the authorization URL (Step 2 in the notebook) and log in
2. Authorize the app
3. Copy the `code` from the redirected URL
4. Paste it into the notebook

The notebook will then generate an **access token automatically**.

---

## 📁 Project Structure

```id="p9x2kd"
strava-api-to-excel/
│
├── strava_to_excel.ipynb
├── requirements.txt
└── README.md
```

---

## ⚙️ Requirements

Install dependencies:

```id="l2m8qp"
pip install -r requirements.txt
```

Libraries used:

* pandas
* requests
* openpyxl
* geopy

---

## ▶️ How to Run

1. Open the notebook:

```id="0kq8sl"
jupyter notebook strava_to_excel.ipynb
```

2. Follow each step:

   * Enter your Client ID and Client Secret
   * Generate and paste your authorization code
   * Run the remaining cells

3. The Excel file will be generated automatically.

---

## 📊 Output

The Excel file contains two sheets:

### Activities

* Activity name
* Type
* Distance
* Moving time
* Pace
* City & country (via reverse geocoding)

### Shoes

* Shoe name
* Total distance
* Retirement status

---

## 📝 Notes

* Do not share your API credentials
* Access tokens may expire and need regeneration
* Reverse geocoding may take time due to rate limiting

---

## 📌 Future Improvements

* Automate token refresh
* Add filtering (date ranges, activity types)
* Improve performance of geocoding
* Convert notebook into a Python script or CLI tool

---

## 📄 License

This project is open for personal and educational use.
