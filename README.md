# csvtoconfmd

A fork of mplewis' [csvtomd](https://github.com/mplewis/csvtomd) - hacked together to output a table in Confluence wiki format.

# Usage

`csvtoconfmd.py MY_SPREADSHEET.csv` generates a Markdown table from `MY_SPREADSHEET.csv`.

`csvtoconfmd.py SHEET1.csv SHEET2.csv SHEET3.csv` generates three Markdown tables from the input files and displays them alongside the input filename.

`csvtoconfmd.py` or `csvtoconfmd.py -` generates a Markdown table from standard input. You can type CSV data or pipe a file in.

## Example Input

File: `thrones.csv`

```
First Name,Last Name,Location,Allegiance
Mance,Rayder,North of the Wall,Wildlings
Margaery,Tyrell,The Reach,House Tyrell
Danerys,Targaryen,Meereen,House Targaryen
Tyrion,Lannister,King's Landing,House Lannister
```

## Example Confluence Wiki Table

Command: `csvtoconfmd.py thrones.csv`

||First Name  ||  Last Name  ||  Location           ||  Allegiance ||
|Mance       |  Rayder     |  North of the Wall  |  Wildlings      |
|Margaery    |  Tyrell     |  The Reach          |  House Tyrell   |
|Danerys     |  Targaryen  |  Meereen            |  House Targaryen|
|Tyrion      |  Lannister  |  King's Landing     |  House Lannister|


## Requirements

Python 3.

## Help

Command: `csvtoconfmd.py --help`

```
usage: csvtoconfmd.py [-h] [-n] [-p PADDING] [-d DELIMITER] csv_file [csv_file ...]

Read one or more CSV files and output their contents in the form of Markdown
tables.

positional arguments:
  csv_file              One or more CSV files to be converted

optional arguments:
  -h, --help            show this help message and exit
  -n, --no-filenames    Don't display filenames when outputting multiple
                        Markdown tables.
  -p PADDING, --padding PADDING
                        The number of spaces to add between table cells and
                        column dividers. Default is 2 spaces.
  -d DELIMITER, --delimiter DELIMITER
                        CSV delimiter, expected values: ',', ';'. Default is ,
```

# License

Copyright (c) 2017 Matthew Lewis. Licensed under [the MIT License](http://opensource.org/licenses/MIT).
