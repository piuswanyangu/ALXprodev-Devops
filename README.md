# ALXprodev-Devops
# Task 0: API Request Automation
Description

In this task, I created a shell script that automates the process of fetching data from a RESTful API. The script interacts with the Pokémon API to retrieve information about a specific Pokémon (Pikachu) and saves the response locally for further processing.

# What Was Implemented

Used curl to make an HTTP GET request to the Pokémon API endpoint for Pikachu.

Saved the successful JSON response into a file named data.json.

Implemented basic error handling by checking the exit status of the curl command.

Logged any request failure into an errors.txt file with a timestamp.

Ensured the script is executable and can be run from the terminal.

# Tools Used

bash: for scripting and automation

curl: for making API requests

jq: for validating and previewing the JSON response

How to Run the Script
chmod +x apiAutomation-0x00.sh
./apiAutomation-0x00.sh

  # Expected Output

On success:

A file named data.json containing Pokémon data for Pikachu.

# On failure:

An error message appended to errors.txt.

Sample Verification Command
jq . data.json | head -n 50

# Learning Outcome

This task demonstrates basic API interaction from the command line, file handling, and error checking in shell scripting. It simulates a real-world data extraction step commonly used in DevOps and Data Engineering workflows.

## Task 1: Extract Pokémon Data

This task focuses on extracting and transforming specific fields from a JSON API response using command-line text processing tools.

### Implementation
- Used `jq` to extract the Pokémon’s name, height, weight, and type from `data.json`.
- Used `awk` to convert height and weight into meters and kilograms.
- Used `sed` to format the Pokémon type with proper capitalization.
- Displayed the extracted data in a clear, human-readable sentence.

### Sample Output
Pikachu is of type Electric, weighs 6kg, and is 0.4m tall.


## Task 2: Batch Pokémon Data Retrieval

This task automates fetching data for multiple Pokémon using a loop.

### Implementation
- Created a directory `pokemon_data` to store JSON files.
- Defined an array of Pokémon: Bulbasaur, Ivysaur, Venusaur, Charmander, Charmeleon.
- Used a `for` loop to fetch data from the Pokémon API.
- Saved each Pokémon’s data in a separate JSON file named after the Pokémon.
- Implemented error handling and logged failures to `errors.txt`.
- Added `sleep 1` between requests to avoid rate-limiting.

### Sample Output
Fetching data for bulbasaur...
Saved data to pokemon_data/bulbasaur.json ✅
Fetching data for ivysaur...
Saved data to pokemon_data/ivysaur.json ✅
