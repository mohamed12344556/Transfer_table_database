# Project Title

Excel to Multiple Formats Transformation

## Description

This project provides a script to transform Excel sheets into separate Excel, JSON, and SQL files. It takes all worksheets from a given Excel file, processes them, and saves the transformed data into specified formats. This can be useful for data manipulation, storage, and integration with different systems or databases, saving you significant time and effort.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [Example](#example)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/repo-name.git
    cd repo-name
    ```
2. Create and activate a virtual environment (optional but recommended):
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```
3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

1. Place your Excel file in the project directory. Make sure it's named `schedule.xlsx` or adjust the script to your file name.
2. Run the script:
    ```sh
    python transform_script.py
    ```
3. Follow the prompts to enter the `plans_number` for each sheet.
4. The transformed files will be saved in the `transformed_data` directory.

## Folder Structure

The script will create the following folder structure to save the transformed files:

project_directory/
│
├── schedule.xlsx
├── transform_script.py
├── transformed_data/
│   ├── excel_files/
│   │   ├── sheet1_transformed.xlsx
│   │   ├── sheet2_transformed.xlsx
│   │   └── ...
│   ├── json_files/
│   │   ├── sheet1_transformed.json
│   │   ├── sheet2_transformed.json
│   │   └── ...
│   └── sql_files/
│       ├── sheet1_transformed.sql
│       ├── sheet2_transformed.sql
│       └── ...



## Example

1. Input Excel Sheet:

    | اليوم/الوقت | 08:00 - 09:00 | 09:00 - 10:00 | 10:00 - 11:00 | 11:00 - 12:00 |
    |--------------|---------------|---------------|---------------|---------------|
    | الأحد        | Math          | Science       | History       | PE            |
    | الاثنين      | English       | Math          | Art           | Music         |

2. Transformed JSON Example:

    ```json
    [
        {
            "plans_id": 1,
            "plans_number": 1,
            "plans_day": "الأحد",
            "plans_time_1": "08:00 - 09:00",
            "plans_subject_1": "Math",
            "plans_time_2": "09:00 - 10:00",
            "plans_subject_2": "Science",
            "plans_time_3": "10:00 - 11:00",
            "plans_subject_3": "History",
            "plans_time_4": "11:00 - 12:00",
            "plans_subject_4": "PE"
        },
        ...
    ]
    ```

3. Transformed SQL Example:

    ```sql
    INSERT INTO `plans` VALUES (NULL, 1, 'الأحد', '08:00 - 09:00', 'Math', '09:00 - 10:00', 'Science', '10:00 - 11:00', 'History', '11:00 - 12:00', 'PE');
    INSERT INTO `plans` VALUES (NULL, 1, 'الاثنين', '08:00 - 09:00', 'English', '09:00 - 10:00', 'Math', '10:00 - 11:00', 'Art', '11:00 - 12:00', 'Music');
    ```

## Contributing

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## License

Distributed under the MIT License. See `LICENSE` for more information.
