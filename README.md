# ThangsScraper

ThangsScraper is a web scraping tool designed to extract 3D model data from [Thangs.com](https://thangs.com). It automates the process of downloading STL files, gathering metadata, calculating material costs, and storing the collected data in a structured format for further analysis.

## Features
- Automates login and navigation on Thangs.com.
- Scrapes model details including names, descriptions, and images.
- Downloads STL files and calculates estimated printing costs.
- Stores scraped data in an SQLite database.
- Supports bulk operations through an Excel interface.

## Installation
### **Prerequisites**
Ensure you have the following installed:
- Python 3.x
- Firefox browser
- Geckodriver (for Selenium)

### **Clone the Repository**
```bash
git clone https://github.com/your-username/ThangsScraper.git
cd ThangsScraper
```

### **Install Dependencies**
```bash
pip install -r requirements.txt
```

## Usage

### **1. Set Up Environment Variables**
Create a `.env` file in the root directory and add the following details:
```env
EMAIL=your_email@example.com
PASSWORD=your_password
PRICE_PER_GRAM=0.05
FILLNESS=0.25
```

### **2. Run the Scraper**
Execute the following command to start the scraping process:
```bash
python thangs.py
```
You will be prompted to:
- Select a category
- Enter the starting and ending pages
- Specify a keyword if needed

### **3. Database Operations**
To manage the scraped data, use `DBoperations.py`:
```bash
python DBoperations.py
```
This allows you to:
- View models
- Add, update, or delete records
- Search and export data
- Update XML files with active records

## File Structure
```
ThangsScraper/
│── thangs.py          # Main scraper script
│── models_db.py       # Database models and operations
│── DBoperations.py    # Database management tool
│── categories.py      # Category handling (if applicable)
│── .env               # Environment variables
│── requirements.txt   # Required Python packages
│── README.md          # Documentation
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss your proposed modifications.

## License
This project is licensed under the MIT License.

