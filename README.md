# Transaction Import Filter
Current Version - 1.04

### Version 1.04 Changelog

- Added Data Scraping Tool

### Version 1.03 Changelog

- Added automatic update check
- Fixed category and subcategory being flipped for ING
- Fixed account numbers being displayed in bank format

## INFORMATION

This simple program formats the downloadable transaction csv file from a bank for import to a budget spreadsheet.
The adjustments made are:
- Only import transactions after a specific date
- Find 'labels' in the description and apply a better description, category and subcategory
- Find 'accounts' and replace the number with a more identifiable description
- For labels with a description of '#' the matching entries will be deleted (useful for unnecessary internal transfers)
- Split expenses and income and track the deleted entries
- Format correctly for simple copy and paste into my budget spreadsheet

## SETUP


1. Install the application. It will download MATLAB runtime files automatically if required.
2. Ensure the packaged folder 'Transaction Filter' is located in C:\Users\*USERNAME*\Documents\
3. Do not rename this folder or existing subfolders


## INSTRUCTIONS

1. Download the required transaction files.
BENDIGO - download the 'simple csv' (3 columns) for each account
ING - download the full csv containing all accounts

2. Set a 'Start Date'. Any transactions before this date will be omitted from results.
	Typically this should be the last date you ran the program.
3. Select a bank. Each bank formats the transaction csv file differently.
4. Select an account. Note: ING automatically filters accounts but for Bendigo you must select individually.
5. Click 'Add' to import and filter data.
6. Continue to add all data.
7. When satisfied click save to write the data to a file called 'Results.xlsx'.
8. Click finish or close when done.

NOTE: MATLAB tables are not user friendly for editting, so all editting is best performed in excel.
The ability to edit in MATLAB was removed to avoid accidental errors. Ensure you refresh labels and accounts after editting.

## LABELS

1. Add a 'Search Term' for the program to look for in the description of each transaction
2. Add a 'Description' that you want the program to apply to a matched transaction
	If this description is left blank, the existing description will kept
	If this description is '#' (without apostrophes) the matched entries will be deleted

Terms will be searched sequentially. Therefore, priority will be given to the highest match in the labels list
