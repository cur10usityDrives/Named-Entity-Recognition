# Named Entity Recognition (NER) using spaCy

## Overview

This project implements Named Entity Recognition (NER) using the spaCy library in Python. NER is a fundamental task in 
Natural Language Processing (NLP) that involves identifying and categorizing entities (such as names of persons, organizations, 
locations, dates, etc.) within a body of text. The goal of this project is to demonstrate how to extract these entities using a 
pre-trained spaCy model and additional custom rules.

## Features

- **Entity Types Recognized**:
  - **PERSON**: Names of persons (e.g., "John Smith", "Mary Jane").
  - **GPE (Geo-Political Entity)**: Names of countries, cities, states, etc.
  - **ORG**: Names of organizations, companies, institutions, etc.
  - **TITLE**: Government official titles (e.g., "President", "Prime Minister").
  - **DATE**: Dates and times mentioned in the text (e.g., "January 1, 2023", "tomorrow").

- **Implementation Details**:
  - **spaCy Integration**: Utilizes the `en_core_web_sm` model from spaCy, which is pre-trained on a large corpus of text.
  - **Regex Patterns**: Custom regex patterns are used to enhance entity recognition for specific categories like country names and dates.
  - **Functionality**: Includes functions for extracting each type of entity separately, providing flexibility and modularity in usage.

## Project Structure

- **`README.md`**: This file provides an overview of the project, installation instructions, usage guidelines, and examples.
- **`ner_project.py`**: Python script containing functions for extracting named entities using spaCy and regex.
- **`NER_Dataset.csv`**: Sample dataset used for testing the NER functions.
- **`requirements.txt`**: Lists the Python packages required to run the project (e.g., spaCy, pandas).
- **`LICENSE`**: License information for the project.

## Usage

1. **Installation**:
   - Clone the repository: `git clone https://github.com/cur10usityDrives/Named-Entity-Recognition.git`
   - Install dependencies: `pip install -r requirements.txt`

2. **Running the Code**:
   - Modify `ner_project.py` to process your specific text data or integrate into your own Python projects.
   - Use the functions like `extract_person_names`, `extract_country_names`, etc., to extract named entities from text data.

3. **Example**:
   ```python
   from ner_project import extract_person_names, extract_country_names, extract_organization_names, extract_official_titles, extract_datetimes

   sample_text = "In Beirut, a string of officials voiced their anger, while at the United Nations summit in New York, Prime Minister Fouad Siniora said the Lebanese people are resolute in preventing such attempts from destroying their spirit."

   print("Person Names:", extract_person_names(sample_text))
   print("Country Names:", extract_country_names(sample_text))
   print("Organization Names:", extract_organization_names(sample_text))
   print("Official Titles:", extract_official_titles(sample_text))
   print("Datetimes:", extract_datetimes(sample_text))
   ```

## Contributing

Contributions to improve this project are welcome! You can contribute by:

- Opening issues for bugs or feature requests.
- Forking the repository and submitting pull requests with improvements.
- Providing feedback on the project and its documentation.

## Author

Natnael Haile
