## List My Apps Template - Data



|                    |                                                                                |
|  -------------     |  -------------                                                                 |
|  **OS:**           |  Android, Windows                                                              |
|  **Type:**         |  A template for an Android app called '[List My Apps](https://play.google.com/store/apps/details?id=de.onyxbits.listmyapps)'                          |
|  **Language:**     |  General (with custom variables) and optionally Windows PowerShell             |
|  **Description:**  |  This template (when run in an Android app called 'List My Apps') creates a list of the apps installed on an Android device in a semi-colon delimited txt-file. The resulted .txt-file can be imported into Microsoft Excel (as described in the Tutorial Step 10 below) or imported to LibreOffice Calc via Windows Notepad (Tutorial Step 11) or processed directly in Windows PowerShell to convert it to a csv-file (Tutorial Step 12). The goal is to have a .xlsx or .ods file as an end product (which itself can be converted to PDF...).                                                |
|  **Homepage:**     |	<https://github.com/auberginehill/list-my-apps-template-data>                 |
|  **Source:**       |  Descriptions of the variables: <http://www.onyxbits.de/faq-page/22#t22n48>    |


#### Remarks 

- List My Apps custom templates consist of three fields ("List header", "Item format" and "List footer"). The template code in this project is divided into three parts, which correspond the fields found in List My Apps' Template Editor as described below: 

   |  Filename                            |  Field in List My Apps' Template Editor                     |
   |  -------------                       |  -------------                                              |
   |  [file_header.txt](file_header.txt)  |  "List header, may be blank"                                |
   |  [body.txt](body.txt)                |  "Item format, may not be blank"                            |
   |  [file_footer.txt](file_footer.txt)  |  "List footer, may be blank"                                |
   |  [all_in_one.txt](all_in_one.txt)    |  Contains all the above mentioned three parts in one file.  |

- Please include one empty row after [file_header.txt](file_header.txt) and [body.txt](body.txt) in the List My Apps template (so that the script will write each app on its own row instead of all apps in one row).

- The resulted .txt-file needs to be further processed in order to create a human readable file.



#### Tutorial

To open this code with an Android device, for instance:

1. Create a new template in [List My Apps](https://play.google.com/store/apps/details?id=de.onyxbits.listmyapps)' -app's Template Editor by clicking Options (three dots) &rarr; Template Editor &rarr; Add. [[Screenshot](http://groovyandroid.com/wp-content/uploads/2013/10/List-My-Apps-select-all.png)]

2. Type in a name for the template.
   ![Screenshot](https://github.com/auberginehill/list-my-apps-template-table/blob/master/list_my_apps_-_template_editor.png "Screenshot")

3. Paste all the appropriate template data (the three sections as specified below) to 'List My Apps'. Please include one empty row after [file_header.txt](file_header.txt) and [body.txt](body.txt) (so that the script will write each app on its own row instead of all apps in one row) and save the template.

   |  Filename                            |  Field in List My Apps' Template Editor                     |
   |  -------------                       |  -------------                                              |
   |  [file_header.txt](file_header.txt)  |  "List header, may be blank"                                |
   |  [body.txt](body.txt)                |  "Item format, may not be blank"                            |
   |  [file_footer.txt](file_footer.txt)  |  "List footer, may be blank"                                |
   |  [all_in_one.txt](all_in_one.txt)    |  Contains all the above mentioned three parts in one file.  |

4. Go back to the 'List My Apps' -app's home screen and select the name that was created in Step 2 from the 'Copy/Share as:' -dropdown menu. Please also select the apps that you'd like to be included in the list. [[Screenshot](http://groovyandroid.com/wp-content/uploads/2013/10/List-My-App-HTML-list.png)]

5. 'Run' the 'List My Apps' -app with the new template by copying the app data to Clipboard \[Copy\] (since direct sharing may not work, if a lot of applications has been installed).
   - There seems to be some kind of a limit, how much data the Android Clipboard can contain. With verbose templates ~200 apps might be the upper limit, but with a simple template, the Android Clipboard clearly is capable of containing considerably more app data.

6. Open a text editor, such as [DroidEdit Free](https://play.google.com/store/apps/details?id=com.aor.droidedit).

7. Paste the app data (source code generated by 'List My Apps' in Step 5) from Clipboard to the text editor.
   - If nothing happens (no data is copied to a text editor), try selecting fewer apps in 'List My Apps' and go back to Step 5.
   - If "old data" gets copied to a text editor (i.e. "the data that was in the Clipboard before List My Apps' 'Copy to Clipboard' -button was clicked"), try selecting fewer apps in 'List My Apps' and go back to Step 5.

8. Save the file as a .txt-file, for example as 'Installed_Apps.txt', for example in 'Home/Documents' folder (a filename without any spaces is recommended).

9. Copy the .txt-file to, for instance, C:\Temp\ -directory in Windows.

10. **Microsoft Excel** (Text Import Wizard) 
   - On the Data tab of the Ribbon bar, in the Get External Data group, click From Text. Then, in the Import Text File dialog box, double-click the Installed_Apps.txt file.
   - Step 1 of 3: Set the original data type as Delimited, Start import at row 1 and the choose a character set in File origin, which matches the character set set in Step 8 (In most cases, the File origin -setting can be left at its default). Click Next.
   - Step 2 of 3. Select semi-colon under Delimiters and make sure all other options are NOT selected, and also that Text qualifier is set to " and click Next.
   - Step 3 of 3: The Column data format can be set individually for each column. The default General setting works fine for most of the fields, but at least the 'Version' column has to be set to Text in order to preserve the original data during the import. Click Finish.
   - Select where the imported cells are placed and click OK.

11. **LibreOffice Calc** Paste Special via Windows Notepad
   - After copying the .txt-file to, for instance, C:\Temp\ -directory in Windows (Step 9) open the .txt-file in Windows Notepad, select all text (Ctrl + A) and copy the selection to Windows Clipboard (Ctrl + C).
   - Open LibreOffice Calc and click Edit - Paste Special (Ctrl + Shift + V) and double-click Unformatted Text.
      - Paste Special can also be found as an icon in the toolbar or by right-clicking a cell.
   - Set semi-colon as the Delimiter and make sure all other options are NOT selected, and also that Text qualifier is set to " and start import at row 1 and choose a character set, which matches the character set set in Step 8 (In most cases, the Character set -setting can be left at its default). Click OK.
      - In Excel this procedure can be initiated by clicking the text "Paste" below the paste icon in Home tab of the Ribbon bar and selecting Use Text Import Wizard.

12. **Windows PowerShell**
   - After copying the .txt-file to, for instance, C:\Temp\ -directory in Windows (Step 9) open Windows PowerShell. Type the script below and press \[Enter\] (to convert the .txt-file into a .csv-file with semi-colon as delimiter):

      `Import-Csv C:\Temp\Installed_Apps.txt -Delimiter ";" | sort Type,Name | Export-Csv C:\Temp\csvfile.csv -Delimiter ";" -NoTypeInformation -Encoding UTF8`

      |  Parameter             |  Description                                                                        |
      |  -------------         |  -------------                                                                      |
      |  `sort`                |  Sorting can be adjusted to one's liking by adjusting `sort Type,Name` with approppriate column header names (which are set in the [file_header.txt](file_header.txt) -section).                        |
      |  `-Delimiter`          |  Any single character can be used as a delimiter in the exported csv-file. For tab character as a delimiter, the two character `'t` -combo might work.                                                      |
      |  `-NoTypeInformation`  |  Without the the `NoTypeInformation` -parameter the first line of the .csv-file would contain `#TYPE` followed by the name of the type of the object, and that is not a desired effect here.                 |
      |  `-Encoding`           |  The default value is `ASCII`. The acceptable values for this parameter are: `Unicode`, `UTF7`, `UTF8`, `ASCII`, `UTF32`, `BigEndianUnicode`, `Default`, `OEM`                                         |
      |  `-Force`              |  If any error messages are detected and you know your're right, use the `Force`.    |
      |  `-NoClobber`          |  Halts the procedure, if overwriting (replacing the contents) of an existing file is about to happen. By default, if a file exists in the specified path, `Export-CSV` overwrites the file without warning.  |
      |  `-Confirm`            |  Prompts you for confirmation before running the cmdlet.                            |

      Further info: <https://technet.microsoft.com/en-us/library/hh849932.aspx>

13. Conversion from .csv to .xlsx or .ods should be pretty straightforward with Office apps, such as Microsoft Excel or LibreOffice. A couple of extra Windows PowerShell scripts below:

   - **CSV to Excel (in Windows PowerShell)**
   
   |           |                                                                                                   |
   |  -------  |  -------------                                                                                    |
   |           |  `$xl = new-object -comobject excel.application`                                                  |
   |           |  `$xl.visible = $False`                                                                           |
   |           |  `$Workbook = $xl.workbooks.open("C:\Temp\csvfile.csv")`                                          |
   |           |  `$Worksheets = $Workbooks.worksheets`                                                            |
   |           |  `$Workbook.SaveAs("C:\Temp\Excelfile.xlsx",1)`                                                   |
   |           |  `$Workbook.Saved = $True`                                                                        |
   |           |  `$xl.Quit()`                                                                                     |
   |  Notes:   |  In some instances the data in the 'Version' column is deprecated during the conversion.          |
   |  Source:  |  [Powershell convert csv to xlsx](https://social.technet.microsoft.com/Forums/windowsserver/en-US/370ee470-f2cd-4f30-a167-b106dd51d47a/)    |
   |           |  [Converting CSV file or files into an Excel workbook](https://learn-powershell.net/2010/09/04/converting-csv-file-or-files-into-an-excel-workbook/)         |
   
   

   - **Excel to CSV (in Windows PowerShell)** 

   |           |                                                                                                   |
   |  -------  |  -------------                                                                                    |
   |           |  `$xlCSV = 6`                                                                                     |
   |           |  `$Excel = New-Object -Com Excel.Application`                                                     |
   |           |  `$Excel.visible = $False`                                                                        |
   |           |  `$Excel.displayalerts=$False`                                                                    |
   |           |  `$WorkBook = $Excel.Workbooks.Open("C:\Temp\Excelfile.xlsx")`                                    |
   |           |  `$Workbook.SaveAs("C:\Temp\process.csv",$xlCSV)`                                                 |
   |           |  `$Excel.quit()`                                                                                  |
   |  Source:  |  [Converting CSV file or files into an Excel workbook](https://learn-powershell.net/2010/09/04/converting-csv-file-or-files-into-an-excel-workbook/)         |
   
   
   
      - **Export-XLXS.ps1 (in Windows PowerShell)** 

   |              |                                                                                                   |
   |  ----------  |  -------------                                                                                    |
   |  First:      |  `. .\Export-XLXS.ps1`                                                                            |
   |  Then:       |  `Get-Command -CommandType Function -Name Export-XLXS`                                            |
   |  That gave:  |  `CommandType Name Version Source`                                                                |
   |              |  `———– —- ———-`                                                                                   |
   |              |  `Function Export-XLXS`                                                                           |
   |  Then:       |  `Get-Process | select Name,Id,Handles | Export-XLXS c:\Temp\Report.xlsx`                         |
   |  Source:     |  [Export-XLSX PowerShell generate real Excel XLSX files without Excel and COM](https://gallery.technet.microsoft.com/office/Export-XLSX-PowerShell-f2f0c035)                                 | 
   
   
   
      - **ConvertCSV-ToExcel.ps1 (in Windows PowerShell)** 

   |              |                                                                                                   |
   |  ----------  |  -------------                                                                                    |
   |  First:      |  `. .\Export-XLXS.ps1`                                                                            |
   |  Then:       |  `Get-Command -CommandType Function -Name ConvertCSV-ToExcel`                                     |
   |  That gave:  |  `CommandType Name Version Source`                                                                |
   |              |  `———– —- ———-`                                                                                   |
   |              |  `Function ConvertCSV-ToExcel`                                                                    |
   |  Then:       |  `ConvertCSV-ToExcel -inputfile 'file.csv' -output 'report.xlsx'`                                 |
   |  Source:     |  [Convert CSV/s to Excel](https://gallery.technet.microsoft.com/office/7c56c444-2476-4625-b1d9-821f30280e44)                          |
   
   
   
#### Contributing
Find a bug? Have a feature request? Here is how you can contribute to this List My Apps Template -project: 
- [Submit bugs](https://github.com/auberginehill/list-my-apps-template-data/issues) and by help us verify fixes.
- Feature request can be submitted by [creating an Issue](https://github.com/auberginehill/list-my-apps-template-data/issues).
- [Submit pull requests](https://github.com/auberginehill/list-my-apps-template-data/pulls) for bug fixes and features and discuss existing proposals.



#### www

- [Template Homepage](https://github.com/auberginehill/list-my-apps-template-data)
- [List My Apps](https://play.google.com/store/apps/details?id=de.onyxbits.listmyapps) (Google Play)
- [List My Apps' homepage](http://www.onyxbits.de/listmyapps)
- [List My Apps' application thread](http://forum.xda-developers.com/showthread.php?t=2460266) at xda-developers.com
- [DroidEdit Free](https://play.google.com/store/apps/details?id=com.aor.droidedit) (free code editor)

  

#### Related scripts

- [List My Apps Template - Table](https://github.com/auberginehill/list-my-apps-template-table)
- [List My Apps Template - List](https://github.com/auberginehill/list-my-apps-template-list)
- [List My Apps Template - Pro](https://github.com/auberginehill/list-my-apps-template-pro)
- [List My Apps Template - XML plain](https://github.com/auberginehill/list-my-apps-template-xml-plain)
- [List My Apps Template - XML style](https://github.com/auberginehill/list-my-apps-template-xml-style)



|             |                                                             |
|  --------   |  -------------                                              |
|  **N.B.**   |  Please include one empty row after [file_header.txt](file_header.txt) and [body.txt](body.txt) in the List My Apps template (so that the script will write each app on its own row instead of all apps in one row).  |
