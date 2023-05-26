# KeePass-CSV-Importer

# KeePass CSV Import Script

This is a PowerShell script that uses KPScript to import data from a CSV file into a KeePass database.

## How to Use

1. Ensure that KPScript.exe is installed and located where KeePass.exe file is.

2. Replace the placeholders in the script with your specific information:

    ```powershell
    # Variables
    $csvFile = "C:\path\to\your\csvfile.csv"    # Replace with your CSV file path
    $kpscript = "C:\path\to\KPScript\KPScript.exe"   # Replace with your KPScript.exe path
    $database = "C:\path\to\your\KeePassDatabase.kdbx"   # Replace with your KeePass database path
    $masterPassword = "your-master-password"  # Replace with your master password
    $groupName = "GroupName"  # Name of the group where entries will be added
    ```

3. Run the script in PowerShell.

    The script reads a CSV file with columns 'Username [Column A]', 'Password [Column B]', and 'Retrieval Email [Column C]'. It creates a new group in the KeePass database (if it doesn't already exist), then creates a new entry in that group for each row in the CSV file.

## Note

Always ensure to have a secure way of providing your master password to avoid any security risk. Also, backing up your KeePass database is crucial before running the script to prevent any data loss.
