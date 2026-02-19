# METU App Files

Open-source data files for [METU App](https://metuapp.ceng.metu.edu.tr) - a comprehensive mobile application for Middle East Technical University (METU) students and staff.

## 📁 Contents

This repository contains data files used by METU App:

- **Cafeteria Data**: Operating hours and pricing information
- **Academic Calendar**: Semester dates and important dates
- **Weather Images**: User-contributed campus weather photos
- **Notifications**: Content for in-app notifications
- **App Images**: UI assets and icons
- **Map Assets**: Campus location data and map marker images

## 📂 Structure

```
metuapp-files/
├── cafeteria_hours.json    # Cafeteria operating hours
├── canteen-prices.csv      # Canteen pricing data
├── semester_dates.json     # Academic calendar dates
├── images/                 # App UI images
│   ├── fruits.png
│   └── vegetarian.png
├── weather/                # Weather images (Git LFS)
│   ├── clear/
│   ├── cloudy/
│   ├── partlyCloudy/
│   └── stormy/
├── notifications/           # Notification content
│   └── index.json
└── map_assets/              # Map location data and assets
    ├── locations.csv        # Campus locations database
    ├── polo.png            # Car marker image
    ├── pin.svg             # Pin icon
    ├── pin.svg.vec         # Pin icon (vector format)
    └── old/                # Legacy map assets
        └── hitchhiker.png
```

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Contributing Weather Images

1. Take a photo of METU campus in different weather conditions
2. Follow the naming convention: `Your Name--Year--description.jpg`
3. Place in the appropriate weather condition folder
4. Submit a pull request

### Updating Cafeteria Hours

1. Edit `cafeteria_hours.json`
2. Follow the existing JSON structure
3. Ensure valid JSON syntax
4. Submit a pull request

### Updating Semester Dates

1. Edit `semester_dates.json`
2. Add new academic calendar dates
3. Ensure dates are in ISO format (YYYY-MM-DD)
4. Submit a pull request

### Contributing Map Locations

1. Edit `map_assets/locations.csv`
2. Add new locations following the CSV format:
   - `latitude`: Decimal degrees (e.g., 39.892239)
   - `longitude`: Decimal degrees (e.g., 32.783748)
   - `name`: Location name (e.g., "Department of Computer Engineering")
   - `location_type`: Category (e.g., "Academic Buildings", "Dining", "Services")
   - `language`: Language code (e.g., "en", "tr")
   - `link`: Optional photo URL
3. Ensure valid CSV format (comma-separated, proper escaping)
4. Verify coordinates are accurate
5. Submit a pull request

### Contributing Map Images

1. Add map marker images to `map_assets/`
2. Supported formats: PNG, SVG, WebP
3. For SVG files, also provide `.vec` version (vector_graphics format)
4. Recommended sizes:
   - Marker icons: 30-50px
   - Vehicle markers: 50-100px
5. Follow naming conventions (e.g., `polo.png`, `pin.svg`)
6. Submit a pull request

## 📝 File Formats

### cafeteria_hours.json

Meal service times for the cafeteria:

```json
{
  "weekday_lunch_start": "11:30",
  "weekend_lunch_start": "12:00",
  "lunch_end": "14:00",
  "dinner_start": "17:00",
  "dinner_end": "19:30"
}
```

**Fields:**
- `weekday_lunch_start`: Lunch start time on weekdays (HH:MM format)
- `weekend_lunch_start`: Lunch start time on weekends (HH:MM format)
- `lunch_end`: Lunch end time (HH:MM format)
- `dinner_start`: Dinner start time (HH:MM format)
- `dinner_end`: Dinner end time (HH:MM format)

### semester_dates.json

Current and next semester dates:

```json
{
  "current_semester": {
    "start_date": "2026-02-16",
    "end_date": "2026-06-05"
  },
  "next_semester": {
    "start_date": "2026-07-13",
    "end_date": "2026-08-21"
  }
}
```

**Fields:**
- `current_semester`: Object containing start and end dates for the current semester
- `next_semester`: Object containing start and end dates for the next semester
- `start_date`: Semester start date in ISO format (YYYY-MM-DD)
- `end_date`: Semester end date in ISO format (YYYY-MM-DD)

### locations.csv

CSV format for campus locations:

```csv
latitude,longitude,name,location_type,language,link
39.892239,32.783748,Academic Writing Center,Academic Buildings,en,https://example.com/photo.jpg
39.884664,32.778206,Department of Aerospace Engineering,Academic Buildings,en,https://example.com/photo2.jpg
```

**Fields:**
- `latitude`: Decimal degrees (WGS84)
- `longitude`: Decimal degrees (WGS84)
- `name`: Location name (can contain commas if properly escaped)
- `location_type`: Category (Academic Buildings, Dining, Services, etc.)
- `language`: Language code ("en" or "tr")
- `link`: Optional photo URL (can be empty)

**Guidelines:**
- Use WGS84 coordinate system
- Verify coordinates using Google Maps or similar
- Escape commas in names with quotes: `"Department, Name"`
- Keep location types consistent
- Provide photo URLs when available

## 🔧 Technical Details

### Git LFS

Large image files (>100KB) are stored using Git LFS. To work with this repository:

```bash
# Install Git LFS
git lfs install

# Clone repository
git clone https://github.com/metuapp/metuapp-files.git
```

### Image Guidelines

- **Format**: JPG, PNG, WebP, SVG
- **Size**: Recommended max 5MB per image
- **Resolution**: 
  - Weather images: Minimum 1920x1080
  - Map markers: 30-100px (icons), 50-100px (vehicles)
- **Naming**: 
  - Weather images: `Author Name--Year--description.extension`
  - Map assets: Descriptive names (e.g., `polo.png`, `pin.svg`)
- **Vector Graphics**: For SVG files, also provide `.vec` version using vector_graphics_compiler

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- All weather image contributors
- Map location data contributors
- METU App development team
- METU community

## 📞 Contact

- **Website**: https://metuapp.ceng.metu.edu.tr
- **Issues**: https://github.com/metuapp/metuapp-files/issues
- **Discussions**: https://github.com/metuapp/metuapp-files/discussions

## 🔗 Related Projects

- [METU App](https://github.com/metuapp/metuapp) - Main application repository
- [METU App Website](https://metuapp.ceng.metu.edu.tr) - Official website

---

Made with ❤️ by the METU App team
