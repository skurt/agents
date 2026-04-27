---
mode: agent
description: 'Runs the IbK diagnostic script and collects its output'
---
# Terminology
The script refered to in this file can be later in the workflow refered to as "script", "the script", "IbK", "IbK script"

# Step: Run script
1. Set the script output file name to `APQA_script_output.txt`
2. Check whether `APQA_script_output.txt` already exists in the 'root folder'
3. If the file **exists**, ask the user: *"The script output file already exists. Do you want to run the script again and overwrite it?"*
   - If the user **declines**, skip running the script and proceed using the existing file
   - If the user **confirms**, continue to the next step
4. If the file **does not exist**, or the user confirmed to run the script again, proceed:
   a. Try to locate this script: c:\Users\JanK2\OneDrive - Kentico software s.r.o\Scripts\IbK\main.ps1
   b. If the file **cannot be found**, ask for the scripts location
   c. To run this script you will need 3 parameters:
      - serverName is in this project in appsettings file in connection string
      - databaseName is in this project in appsettings file in connection string
      - projectRoot is the 'root folder'
   d. Run the script with its standard output piped directly into `APQA_script_output.txt` in the 'root folder'
5. Collect and remember all the output information as that will be referenced later
