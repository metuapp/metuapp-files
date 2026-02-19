# METU App Files

Open-source data files for [METU App](https://metuapp.ceng.metu.edu.tr) - a comprehensive mobile application for Middle East Technical University (METU) students and staff.

## 📁 Contents

This repository contains data files used by METU App:

- **Cafeteria Data**: Operating hours and pricing information
- **Academic Calendar**: Semester dates and important dates
- **Weather Images**: User-contributed campus weather photos
- **Notifications**: Content for in-app notifications
- **App Images**: UI assets and icons

## 🚀 Quick Start

### Using as a Submodule

This repository is typically used as a Git submodule in the main METU App repository:

```bash
git submodule add https://github.com/metuapp/metuapp-files.git website/metuapp_files
```

### Cloning with Submodules

```bash
git clone --recurse-submodules https://github.com/metuapp/metuapp.git
```

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
│   ├── weather_images.json
│   ├── clear/
│   ├── cloudy/
│   ├── partlyCloudy/
│   └── stormy/
└── notifications/           # Notification content
    └── index.json
```

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Contributing Weather Images

1. Take a photo of METU campus in different weather conditions
2. Follow the naming convention: `Your Name--Year--description.jpg`
3. Place in the appropriate weather condition folder
4. Update `weather/weather_images.json` with metadata
5. Submit a pull request

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

## 📝 File Formats

### cafeteria_hours.json

```json
{
  "cafeteria_name": {
    "days": ["Monday", "Tuesday", ...],
    "hours": "08:00-18:00",
    "notes": "Optional notes"
  }
}
```

### semester_dates.json

```json
{
  "semester": "Fall 2025",
  "start_date": "2025-09-15",
  "end_date": "2025-12-20",
  "holidays": ["2025-10-29", "2025-11-10"]
}
```

### weather_images.json

```json
{
  "condition": {
    "season": [
      {
        "file": "path/to/image.jpg",
        "author": "Your Name",
        "year": "2025"
      }
    ]
  }
}
```

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

- **Format**: JPG, PNG, WebP
- **Size**: Recommended max 5MB per image
- **Resolution**: Minimum 1920x1080 for weather images
- **Naming**: `Author Name--Year--description.extension`

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- All weather image contributors
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
