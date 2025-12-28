# ALXprodev-Devops
Task 0: API Request Automation
Description

In this task, I created a shell script that automates the process of fetching data from a RESTful API. The script interacts with the Pokémon API to retrieve information about a specific Pokémon (Pikachu) and saves the response locally for further processing.

What Was Implemented

Used curl to make an HTTP GET request to the Pokémon API endpoint for Pikachu.

Saved the successful JSON response into a file named data.json.

Implemented basic error handling by checking the exit status of the curl command.

Logged any request failure into an errors.txt file with a timestamp.

Ensured the script is executable and can be run from the terminal.

Tools Used

bash: for scripting and automation

curl: for making API requests

jq: for validating and previewing the JSON response

How to Run the Script
chmod +x apiAutomation-0x00.sh
./apiAutomation-0x00.sh

Expected Output

On success:

A file named data.json containing Pokémon data for Pikachu.

On failure:

An error message appended to errors.txt.

Sample Verification Command
jq . data.json | head -n 50

Learning Outcome

This task demonstrates basic API interaction from the command line, file handling, and error checking in shell scripting. It simulates a real-world data extraction step commonly used in DevOps and Data Engineering workflows.