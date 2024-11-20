# Recycling Data Engineering Project

This project processes recycling business data from JSON files and loads it into a structured SQL database. It handles business information, operating hours, materials accepted, and services offered by recycling facilities in the Middlesbrough, UK area.

## Project Structure

```
├── reporting_engineer.py     # Main data processing script
├── database_definitions.py    # SQL table definitions
├── existing_materials.py    # List of recyclable materials
├── requirements.txt          # Project dependencies
└── .env                      # Environment variables
```

## Database Schema

The project uses a relational database with the following tables:

- `recycling.Businesses`: Core business information
- `recycling.AddressComponents`: Business location details
- `recycling.BusinessHours`: Operating hours for each day
- `recycling.BusinessMaterials`: Materials accepted for recycling
- `recycling.BusinessServices`: Services offered
- `recycling.Materials`: Master list of recyclable materials

## Features

- Parses complex JSON data structures
- Handles various time formats for business hours
- Manages relationships between businesses and materials
- Supports multiple address formats
- Error logging and transaction management
- Geocoding support

## Installation

1. Clone the repository
2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
Create a `.env` file with your API keys and database connection details.

## Usage

1. Prepare your JSON data file with recycling business information
2. Run the data processing script:
```bash
python reporting_engineer.py
```

3. Check the generated SQL statements in `city_country.sql`

## Data Processing

The script performs the following operations:
- Parses business information from JSON
- Converts opening hours to standardized format
- Generates SQL insert statements
- Handles foreign key relationships
- Manages transaction integrity
- Logs any processing errors

## Dependencies

- sqlalchemy
- python-dotenv


## Error Handling

The script includes comprehensive error handling:
- Transaction rollback on failures
- Detailed error logging
- Data validation
- Time format normalization

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

MIT license

## Contact

fitzroypetgrave@gmail.com
