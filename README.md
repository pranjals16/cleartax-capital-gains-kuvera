# Installing dependencies

This script requires two Python dependencies: `beautifulsoup4` and `openpyxl`. Install them first using [pip](https://pip.pypa.io/en/stable/):

```sh
$ pip install beautifulsoup4
$ pip install openpyxl
```

You might have to use `sudo` if installing globally.

# Running the script

The script takes as input two excel sheets:

1. The capital gains statement from Kuvera (let's call it `gains.xls`)
2. The Excel template from ClearTax (say, `template.xlsx`)

Note that the Excel file from Kuvera is an `.xls` and the one from ClearTax is `.xlsx`.

For generating the capital gains report for ClearTax, we run the script as follows:

```sh
$ python cleartax_capital_gains_report.py gains.xls template.xlsx output.xlsx
```

This will write a file called `output.xlsx` to the current directory. You can then verify if the information is correct, and then directly upload it to your ITR on ClearTax.

# Known issues

After you upload, if ClearTax complains that it found errors for one or more rows in your Excel sheet, open `output.xlsx` using any spreadsheet program, and save it in the **Microsoft Excel 2007-2013 XML Format**, and then try uploading that Excel sheet.
