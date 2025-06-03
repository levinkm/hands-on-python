

# 🗺️ Location Logger & Distance Estimator

This is a beginner-friendly Python project designed for students who have completed the CS50 Python course and are studying Geomatics or Geospatial Engineering.

The project involves:
- Logging named geographical locations with latitude and longitude
- Storing them in a JSON file
- Calculating the great-circle distance between any two saved locations

It reinforces concepts like:
- File handling
- JSON data manipulation
- Using Python packages and modules
- Applying math to geospatial data
- Building simple CLI apps

---

## 📦 Features

- ✅ Add new locations with names and coordinates  
- 📁 Stores data in a local `locations.json` file  
- 📍 View saved locations  
- 📏 Calculate distances between any two saved points using the haversine formula  
- 🧱 Structured into modules: `main.py`, `location_utils.py`, and `distance_utils.py`  

---

## 🧠 Skills Practiced

- Python functions, conditionals, and loops  
- Working with files and directories  
- Using `math` and `json` modules  
- Modular coding: splitting logic into separate `.py` files  
- Basic geospatial computation (distance estimation using coordinates)

---

## 🚀 How to Run

1. Make sure you have Python installed (version 3.10 or higher).
2. Clone or download the repository.
3. Open a terminal and run:

```bash
python3 main.py
````

---

## 📁 Project Structure

```
GOESPATIAL_LOGGER/
├── main.py                    # Entry point of the application
├── README.md                  # Project description and usage instructions
├── data/
│   ├── .gitkeep               # Keeps the data folder in version control
│   └── locations.json         # Stores the saved geospatial location data
├── utils/
│   ├── .gitkeep               # Keeps the utils folder in version control
│   ├── helpers.py             # General utility functions
│   ├── distance_utils.py      # Haversine distance calculation and related helpers
│   └── location_utils.py      # Functions for loading, saving, and displaying locations

```

---

## 🌍 Sample Coordinates to Try

| Location | Latitude | Longitude |
| -------- | -------- | --------- |
| Nairobi  | -1.2921  | 36.8219   |
| Mombasa  | -4.0435  | 39.6682   |
| Eldoret  | 0.5204   | 35.2698   |

---

## 📌 Future Enhancements (Optional)

* Support for importing locations from CSV
* Visualizing points on a map using `folium` or `matplotlib`
* Adding time of logging
* Categorizing locations (e.g. City, Landmark, Site)


---

### ✅ Sample Interaction

```bash
$ python3 main.py

📍 Welcome to Location Logger & Distance Estimator
--------------------------------------------------

Please choose an option:
1. Add new location
2. View saved locations
3. Calculate distance between locations
4. Exit
> 1

Enter location name: Nairobi
Enter latitude: -1.2921
Enter longitude: 36.8219
✅ Location 'Nairobi' saved!

--------------------------------------------------
Please choose an option:
1. Add new location
2. View saved locations
3. Calculate distance between locations
4. Exit
> 1

Enter location name: Mombasa
Enter latitude: -4.0435
Enter longitude: 39.6682
✅ Location 'Mombasa' saved!

--------------------------------------------------
Please choose an option:
1. Add new location
2. View saved locations
3. Calculate distance between locations
4. Exit
> 2

🌍 Saved Locations:
-------------------
1. Nairobi (Lat: -1.2921, Lon: 36.8219)
2. Mombasa (Lat: -4.0435, Lon: 39.6682)

--------------------------------------------------
Please choose an option:
1. Add new location
2. View saved locations
3. Calculate distance between locations
4. Exit
> 3

Enter name of the first location: Nairobi
Enter name of the second location: Mombasa
📏 The distance between Nairobi and Mombasa is approximately 441.08 km.

--------------------------------------------------
Please choose an option:
1. Add new location
2. View saved locations
3. Calculate distance between locations
4. Exit
> 4

👋 Goodbye!
```

---

### 📁 `locations.json` After Saving

```json
[
  {
    "name": "Nairobi",
    "latitude": -1.2921,
    "longitude": 36.8219
  },
  {
    "name": "Mombasa",
    "latitude": -4.0435,
    "longitude": 39.6682
  }
]
```


