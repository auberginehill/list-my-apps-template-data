<!-- Visual Studio Code: For a more comfortable reading experience, use the key combination Ctrl + Shift + V

  _____        _        
 |  __ \      | |       
 | |  | | __ _| |_ __ _ 
 | |  | |/ _` | __/ _` |
 | |__| | (_| | || (_| |
 |_____/ \__,_|\__\__,_|                                                                                 -->



## List My Apps Template - Data

<table>
   <tr>
        <td style="padding:6px"><strong>OS:</strong></td>
        <td style="padding:6px">Android</td>
   </tr>
   <tr>
        <td style="padding:6px"><strong>Type:</strong></td>
        <td style="padding:6px">A template for an Android app called '<a href="https://play.google.com/store/apps/details?id=de.onyxbits.listmyapps">List My Apps</a>'</td>
   </tr>
   <tr>
        <td style="padding:6px"><strong>Language:</strong></td>
        <td style="padding:6px">General (with custom variables) and optionally Windows PowerShell</td>
   </tr>
   <tr>
        <td style="padding:6px"><strong>Description:</strong></td>
        <td style="padding:6px">This template (when run in an Android app called 'List My Apps') creates a list of the apps installed on an Android device in a semi-colon delimited .txt-file. The resulted .txt-file can be imported into Microsoft Excel (as described in the Tutorial Step 10 below) or imported to LibreOffice Calc via Windows Notepad (Tutorial Step 11) or processed directly in Windows PowerShell to convert it to a CSV-file (Tutorial Step 12). The goal is to have a .xlsx or .ods -file as an end product (which itself can be converted to PDF...).</td>
   </tr>
   <tr>
        <td style="padding:6px"><strong>Homepage:</strong></td>
        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data">https://github.com/auberginehill/list-my-apps-template-data</a></td>
   </tr>
   <tr>
        <td style="padding:6px"><strong>Version:</strong></td>
        <td style="padding:6px">1.1</td>
   </tr>
   <tr>
        <td style="padding:6px"><strong>Sources:</strong></td>
        <td style="padding:6px">
            <table>
                <tr>
                    <td style="padding:6px">Emojis:</td>
                    <td style="padding:6px"><a href="https://api.github.com/emojis">https://api.github.com/emojis</a></td>
                </tr>
                <tr>
                    <td style="padding:6px">Descriptions of the variables:</td>
                    <td style="padding:6px"><a href="http://www.onyxbits.de/faq-page/22#t22n48">http://www.onyxbits.de/faq-page/22#t22n48</a></td>
                </tr>
            </table>
        </td>
   </tr>
   <tr>
        <td style="padding:6px"><strong>Downloads:</strong></td>
        <td style="padding:6px">For instance <a href="https://raw.githubusercontent.com/auberginehill/list-my-apps-template-data/master/all_in_one.txt">all_in_one.txt</a> or the same file in <a href="https://raw.githubusercontent.com/auberginehill/list-my-apps-template-data/master/file_header.txt">three</a> <a href="https://raw.githubusercontent.com/auberginehill/list-my-apps-template-data/master/body.txt">separate</a> <a href="https://raw.githubusercontent.com/auberginehill/list-my-apps-template-data/master/file_footer.txt">parts</a>. Or <a href="https://github.com/auberginehill/list-my-apps-template-data/archive/master.zip">everything as a .zip-file</a>.</td>
   </tr>
</table>



#### Screenshot

<img class="screenshot" title="screenshot" alt="screenshot" height="100%" width="100%" src="https://raw.githubusercontent.com/auberginehill/list-my-apps-template-data/master/example.png">



#### Remarks

<table>
   <tr>
        <th>:warning:</th>
        <td style="padding:6px">
            <ul>
                <li>List My Apps custom templates consist of three fields ("List header", "Item format" and "List footer"). The template code in this project is divided into three parts, which correspond the fields found in List My Apps' Template Editor as described below:</li>
            </ul>
        </td>
   </tr>
   <tr>
        <th></th>
        <td style="padding:6px">
            <ul>
                <ol>
                    <p>
                        <table>
                            <tr>
                                <td style="padding:6px"><strong>Filename</strong></td>
                                <td style="padding:6px"><strong>Field in List My Apps' Template Editor</strong></td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/blob/master/file_header.txt">file_header.txt</a></td>
                                <td style="padding:6px">"List header, may be blank"</td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/blob/master/body.txt">body.txt</a></td>
                                <td style="padding:6px">"Item format, may not be blank"</td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/blob/master/file_footer.txt">file_footer.txt</a></td>
                                <td style="padding:6px">"List footer, may be blank"</td>
                            </tr>
                            <tr>
                                <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/blob/master/all_in_one.txt">all_in_one.txt</a></td>
                                <td style="padding:6px">Contains all the above mentioned three parts in one file.</td>
                            </tr>
                        </table>
                    </p>
                </ol>
                <p>
                    <li>Please include one empty row after "File Header" and "Body" in the List My Apps template (so that the script will write each app on its own row instead of all apps in one row).</li>
                </p>
                <p>
                    <li>The resulted .txt-file needs to be further processed in order to create a human readable file.</li>
                </p>
            </ul>
        </td>
   </tr>
</table>



#### Tutorial

<table>
   <tr>
        <th>:book:</th>
        <td style="padding:6px">To open this code with an Android device, for instance:</td>
   </tr>
   <tr>
        <th></th>
        <td style="padding:6px">
            <ol>
                <p>
                    <li>Create a new template in '<a href="https://play.google.com/store/apps/details?id=de.onyxbits.listmyapps">List My Apps</a>' -app's Template Editor by clicking Options (three dots) → Template Editor → Add. [<a href="http://groovyandroid.com/wp-content/uploads/2013/10/List-My-Apps-select-all.png">Screenshot</a>]</li>
                </p>
                <p>
                    <li>Type in a name for the template.<br><br>
                       <ol>
                          <img class="screenshot" title="screenshot" alt="screenshot" height="70%" width="70%" src="https://raw.githubusercontent.com/auberginehill/list-my-apps-template-table/master/list_my_apps_-_template_editor.png">
                       </ol>
                    </li>
                </p>
                <p>
                    <li>Paste all the appropriate template data (the three sections as specified below) to 'List My Apps'. Please include one empty row after "File Header" and "Body" (so that the script will write each app on its own row instead of all apps in one row) and save the template.<br><br>
                        <ul>
                            <p>
                                <table>
                                    <tr>
                                        <td style="padding:6px"><strong>Filename</strong></td>
                                        <td style="padding:6px"><strong>Field in List My Apps' Template Editor</strong></td>
                                    </tr>
                                    <tr>
                                        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/blob/master/file_header.txt">file_header.txt</a></td>
                                        <td style="padding:6px">"List header, may be blank"</td>
                                    </tr>
                                    <tr>
                                        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/blob/master/body.txt">body.txt</a></td>
                                        <td style="padding:6px">"Item format, may not be blank"</td>
                                    </tr>
                                    <tr>
                                        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/blob/master/file_footer.txt">file_footer.txt</a></td>
                                        <td style="padding:6px">"List footer, may be blank"</td>
                                    </tr>
                                    <tr>
                                        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/blob/master/all_in_one.txt">all_in_one.txt</a></td>
                                        <td style="padding:6px">Contains all the above mentioned three parts in one file.</td>
                                    </tr>
                                </table>
                            </p>
                        </ul>
                    </li>
                </p>
                <p>
                    <li>After saving the template go back to the 'List My Apps' -app's home screen and select the name that was created in Step 2 from the 'Copy/Share as:' -dropdown menu. Please also select the apps that you'd like to be included in the list. [<a href="http://groovyandroid.com/wp-content/uploads/2013/10/List-My-App-HTML-list.png">Screenshot</a>]</li>
                </p>
                <p>
                    <li>'Run' the 'List My Apps' -app with the new template by copying the app data to Clipboard [Copy] (since direct sharing may not work, if a lot of applications has been installed).
                        <ul>
                            <li>There seems to be some kind of a limit, how much data the Android Clipboard can contain. With verbose templates ~200 apps might be the upper limit, but with a simple template, the Android Clipboard clearly is capable of containing considerably more app data.</li>
                        </ul>
                    </li>
                </p>
                <p>
                    <li>Open a text editor, such as <a href="https://play.google.com/store/apps/details?id=com.aor.droidedit">DroidEdit Free</a>.</li>
                </p>
                <p>
                    <li>Paste the app data (source code generated by 'List My Apps' in Step 5) from Clipboard to the text editor.
                        <ul>
                            <li>If nothing happens (no data is pasted to a text editor after a few seconds), try selecting fewer apps in 'List My Apps' and go back to Step 5.</li>
                                <ul>
                                    <li>Depending on the device some lagging may occur when trying to paste, say ~10000 lines of code.</li>
                                </ul>
                            <li>If "old data" gets pasted to a text editor (i.e. "the data that was in the Clipboard before List My Apps' 'Copy to Clipboard' -button was clicked"), try selecting fewer apps in 'List My Apps' and go back to Step 5.</li>
                        </ul>
                    </li>
                </p>
                <p>
                    <li>Save the file as a .txt-file, for example as 'Installed_Apps.txt', for example in 'Home/Documents' folder (a filename without any spaces is recommended).</li>
                </p>
                <p>
                    <li>Copy the .txt-file to, for instance, <code>C:\Temp\</code> -directory in Windows.</li>
                </p>
                <p>
                    <li><strong>Microsoft Excel (Text Import Wizard)</strong>
                        <ul>
                            <li>On the Data tab of the Ribbon bar, in the Get External Data group, click From Text. Then, in the Import Text File dialog box, double-click the Installed_Apps.txt file.</li>
                            <li>Step 1 of 3: Set the original data type as Delimited, Start import at row 1 and the choose a character set in File origin, which matches the character set in Step 8 (In most cases, the File origin -setting can be left at its default). Click Next.</li>
                            <li>Step 2 of 3. Select semi-colon under Delimiters and make sure all other options are NOT selected, and also that Text qualifier is set to " and click Next.</li>
                            <li>Step 3 of 3: The Column data format can be set individually for each column. The default General setting works fine for most of the fields, but at least the 'Version' column has to be set to Text in order to preserve the original data during the import. Click Finish.</li>
                            <li>Select where the imported cells are placed and click OK.</li>
                        </ul>
                    </li>
                </p>
                <p>
                    <li><strong>LibreOffice Calc Paste Special via Windows Notepad</strong>
                        <ul>
                            <li>After copying the .txt-file to, for instance, <code>C:\Temp\</code> -directory in Windows (Step 9) open the .txt-file in Windows Notepad, select all text (Ctrl + A) and copy the selection to Windows Clipboard (Ctrl + C).</li>
                            <li>Open LibreOffice Calc and click Edit → Paste Special (Ctrl + Shift + V) and double-click Unformatted Text.</li>
                                <ul>
                                    <li>Paste Special can also be found as an icon in the toolbar or by right-clicking a cell.</li>
                                </ul>
                            <li>Set semi-colon as the Delimiter and make sure all other options are NOT selected, and also that Text qualifier is set to " and start import at row 1 and choose a character set, which matches the character set set in Step 8 (In most cases, the Character set -setting can be left at its default). Click OK.</li>
                                <ul>
                                    <li>In Excel this procedure can be initiated by clicking the text "Paste" below the paste icon in Home tab of the Ribbon bar and selecting Use Text Import Wizard.</li>
                                </ul>
                        </ul>
                    </li>
                </p>
                <p>
                    <li><strong>Windows PowerShell</strong>
                        <ul>
                            <li>After copying the .txt-file to, for instance, <code>C:\Temp\</code> -directory in Windows (Step 9) open Windows PowerShell. Type the script below and press [Enter] (to convert the .txt-file into a .csv-file with semi-colon as delimiter):
                                <ol>
                                    <code>Import-Csv C:\Temp\Installed_Apps.txt -Delimiter ";" | sort Type,Name | Export-Csv C:\Temp\csvfile.csv -Delimiter ";" -NoTypeInformation -Encoding UTF8</code>
                                </ol>
                            </li>
                            <li>Parameters:
                                <ol>
                                    <table>
                                        <tr>
                                            <td style="padding:6px"><code>sort</code></td>
                                            <td style="padding:6px">Sorting can be adjusted to one's liking by adjusting "<code>sort Type,Name</code>" with approppriate column header names (which are set in the "File Header:" -section).</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>-Delimiter</code></td>
                                            <td style="padding:6px">Any single character can be used as a delimiter in the exported CSV-file. For tab character as a delimiter, the two character <code>'t</code> -combo might work.</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>-NoTypeInformation</code></td>
                                            <td style="padding:6px">Without the the <code>NoTypeInformation</code>-parameter the first line of the CSV-file would contain <code>#TYPE</code> followed by the name of the type of the object, and that is not a desired effect here.</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>-Encoding</code></td>
                                            <td style="padding:6px">The default value is <code>ASCII</code>. The acceptable values for this parameter are:
                                                <ul>
                                                    <table>
                                                        <tr>
                                                            <td style="padding:6px"><code>Unicode</code></td>
                                                        </tr>
                                                        <tr>
                                                            <td style="padding:6px"><code>UTF7</code></td>
                                                        </tr>     
                                                        <tr>
                                                            <td style="padding:6px"><code>UTF8</code></td>
                                                        </tr>
                                                        <tr>
                                                            <td style="padding:6px"><code>ASCII</code></td>
                                                        </tr>
                                                        <tr>
                                                            <td style="padding:6px"><code>UTF32</code></td>
                                                        </tr>
                                                        <tr>
                                                            <td style="padding:6px"><code>BigEndianUnicode</code></td>
                                                        </tr>
                                                        <tr>
                                                            <td style="padding:6px"><code>Default</code></td>
                                                        </tr>                                      
                                                    </table>
                                                </ul>
                                            </td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>-Force</code></td>
                                            <td style="padding:6px">If any error messages are detected and you know your're right, use the <code>Force</code>.</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>-NoClobber</code></td>
                                            <td style="padding:6px">Halts the procedure, if overwriting (replacing the contents) of an existing file is about to happen. By default, if a file exists in the specified path, <code>Export-Csv</code> overwrites the file without warning.</td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>-Confirm</code></td>
                                            <td style="padding:6px">Prompts you for confirmation before running the cmdlet.</td>
                                        </tr>
                                    </table>
                                </ol>
                            </li>
                            <li>Further info: <a href="https://technet.microsoft.com/en-us/library/hh849932.aspx">https://technet.microsoft.com/en-us/library/hh849932.aspx</a></li>                            
                        </ul>
                    </li>
                </p>
                <p>
                    <li>Conversion from CSV to .xlsx or .ods should be pretty straightforward with Office apps, such as Microsoft Excel or LibreOffice. A couple of extra Windows PowerShell scripts below:
                    <br>
                    <br>
                        <ul>
                            <li><strong>CSV to Excel</strong> (in Windows PowerShell)
                                <ol>
                                    <table>
                                        <tr>
                                            <td style="padding:6px"><code>$xl = new-object -comobject excel.application</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$xl.visible = $False</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$Workbook = $xl.workbooks.open("C:\Temp\csvfile.csv")</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$Worksheets = $Workbooks.worksheets</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$Workbook.SaveAs("C:\Temp\Excelfile.xlsx",1)</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$Workbook.Saved = $True</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$xl.Quit()</code></td>
                                        </tr>
                                    </table>
                                </ol>
                                <ul>
                                    <table>
                                        <tr>
                                            <td style="padding:6px">Notes:</td>
                                            <td style="padding:6px">In some instances the data in the 'Version' column is deprecated during the conversion.</td>
                                        </tr>
                                        <tr>
                                            <td rowspan="2">Source:</td>
                                            <td style="padding:6px"><a href="https://social.technet.microsoft.com/Forums/windowsserver/en-US/370ee470-f2cd-4f30-a167-b106dd51d47a/">Powershell convert csv to xlsx</a></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><a href="https://learn-powershell.net/2010/09/04/converting-csv-file-or-files-into-an-excel-workbook/">Converting CSV file or files into an Excel workbook</a></td>
                                        </tr>
                                    </table>
                                </ul>
                            </li>
                            <br>
                            <li><strong>Excel to CSV</strong> (in Windows PowerShell)
                                <ol>
                                    <table>
                                        <tr>
                                            <td style="padding:6px"><code>$xlCSV = 6</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$Excel = New-Object -Com Excel.Application</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$Excel.visible = $False</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$Excel.displayalerts=$False</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$WorkBook = $Excel.Workbooks.Open("C:\Temp\Excelfile.xlsx")</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$Workbook.SaveAs("C:\Temp\process.csv",$xlCSV)</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px"><code>$Excel.quit()</code></td>
                                        </tr>
                                    </table>
                                </ol>
                                <ul>
                                    <table>
                                        <tr>
                                            <td style="padding:6px">Source:</td>
                                            <td style="padding:6px"><a href="https://learn-powershell.net/2010/09/04/converting-csv-file-or-files-into-an-excel-workbook/">Converting CSV file or files into an Excel workbook</a></td>
                                        </tr>
                                    </table>
                                </ul>
                            </li>
                            <br>                       
                            <li><strong>Export-XLXS.ps1</strong> (in Windows PowerShell)
                                <ol>
                                    <table>
                                        <tr>
                                            <td style="padding:6px">First:</td>                                            
                                            <td style="padding:6px"><code>. .\Export-XLXS.ps1</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px">Then:</td>
                                            <td style="padding:6px"><code>Get-Command -CommandType Function -Name Export-XLXS</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px">That gave:</td>
                                            <td style="padding:6px"><code>CommandType Name Version Source</code><br>
                                                <code>----------- ---- ------- ------</code><br>
                                                <code>Function Export-XLXS</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px">Then:</td>
                                            <td style="padding:6px"><code>Get-Process | select Name,Id,Handles | Export-XLXS C:\Temp\report.xlsx</code></td>
                                        </tr>
                                    </table>
                                </ol>
                                <ul>
                                    <table>
                                        <tr>
                                            <td style="padding:6px">Source:</td>
                                            <td style="padding:6px"><a href="https://gallery.technet.microsoft.com/office/Export-XLSX-PowerShell-f2f0c035">Export-XLSX PowerShell generate real Excel XLSX files without Excel and COM</a></td>
                                        </tr>
                                    </table>
                                </ul>
                            </li>
                            <br>    
                            <li><strong>ConvertCSV-ToExcel.ps1</strong> (in Windows PowerShell)
                                <ol>
                                    <table>
                                        <tr>
                                            <td style="padding:6px">First:</td>                                            
                                            <td style="padding:6px"><code>. .\ConvertCSV-ToExcel.ps1</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px">Then:</td>
                                            <td style="padding:6px"><code>Get-Command -CommandType Function -Name ConvertCSV-ToExcel</code></td>
                                        </tr>
                                        <tr>
                                            <td style="padding:6px">That gave:</td>
                                            <td style="padding:6px"><code>CommandType Name Version Source</code><br>
                                                <code>----------- ---- ------- ------</code><br>
                                                <code>Function ConvertCSV-ToExcel</code></td>                                            
                                        </tr>
                                        <tr>
                                            <td style="padding:6px">Then:</td>
                                            <td style="padding:6px"><code>ConvertCSV-ToExcel -inputfile 'csvfile.csv' -output 'Excelfile.xlsx'</code></td>
                                        </tr>
                                    </table>
                                </ol>
                                <ul>
                                    <table>
                                        <tr>
                                            <td style="padding:6px">Source:</td>
                                            <td style="padding:6px"><a href="https://gallery.technet.microsoft.com/office/7c56c444-2476-4625-b1d9-821f30280e44">Convert CSV/s to Excel</a></td>
                                        </tr>
                                    </table>
                                </ul>
                            </li>
                        </ul>
                    </li>
                </p>
            </ol>
        </td>
   </tr>
</table>



#### Contributing

<p>Find a bug? Have a feature request? Here is how you can contribute to this project:</p>

 <table>
   <tr>
      <th><img class="emoji" title="contributing" alt="contributing" height="28" width="28" align="absmiddle" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f33f.png"></th>
      <td style="padding:6px"><strong>Bugs:</strong></td>
      <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/issues">Submit bugs</a> and help us verify fixes.</td>
   </tr> 
   <tr>
      <th rowspan="2"></th>
      <td style="padding:6px"><strong>Feature Requests:</strong></td>
      <td style="padding:6px">Feature request can be submitted by <a href="https://github.com/auberginehill/list-my-apps-template-data/issues">creating an Issue</a>.</td>
   </tr> 
   <tr>
      <td style="padding:6px"><strong>Edit Source Files:</strong></td>
      <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data/pulls">Submit pull requests</a> for bug fixes and features and discuss existing proposals.</td>
   </tr>
 </table>   



#### www

<table>
    <tr>
        <th><img class="emoji" title="www" alt="www" height="28" width="28" align="absmiddle" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f310.png"></th>
        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-data">Template Homepage</a></td>
    </tr>
    <tr>
        <th rowspan="10"></th>
        <td style="padding:6px"><a href="https://play.google.com/store/apps/details?id=de.onyxbits.listmyapps">List My Apps</a> (Google Play)</td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="http://www.onyxbits.de/listmyapps">List My Apps' homepage</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="http://forum.xda-developers.com/showthread.php?t=2460266">List My Apps' application thread</a> at xda-developers.com</td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="https://play.google.com/store/apps/details?id=com.aor.droidedit">DroidEdit Free</a> (free code editor)</td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="https://play.google.com/store/apps/details?id=com.alorma.github">Gitskarios for Github</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="http://tmpvar.com/markdown.html">Github Markdown Previewer</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="http://htmlhint.com/">HTMLHint</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="https://text-compare.com/#">Text Compare</a></td>
    </tr>
    <tr>
        <td style="padding:6px"><a href="http://www.freeformatter.com/csv-escape.html">CSV String Escape</a></td>
    </tr>
    <tr>
        <td style="padding:6px">ASCII Art: <a href="http://www.figlet.org/">http://www.figlet.org/</a> and <a href="http://www.network-science.de/ascii/">ASCII Art Text Generator</a></td>
    </tr>
</table>



#### Related scripts

 <table>
   <tr>
        <th><img class="emoji" title="www" alt="www" height="28" width="28" align="absmiddle" src="https://assets-cdn.github.com/images/icons/emoji/unicode/0023-20e3.png"></th>
        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-table">List My Apps Template - Table</a></td>
   </tr>
   <tr>
        <th rowspan="5"></th>
        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-list">List My Apps Template - List</a></td>
   </tr>
   <tr>
        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-pro">List My Apps Template - Pro</a></td>
   </tr>
   <tr>
        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-xml-plain">List My Apps Template - XML plain</a></td>
   </tr>
   <tr>
        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-xml-style">List My Apps Template - XML style</a></td>
   </tr>
   <tr>
        <td style="padding:6px"><a href="https://github.com/auberginehill/list-my-apps-template-json">List My Apps Template - JSON</a></td>
   </tr>
</table>



#### N.B.

 <table>
   <tr>
        <th>:heavy_exclamation_mark:</th>
        <td style="padding:6px">Please include one empty row after "File Header" and "Body" in the List My Apps template (so that the script will write each app on its own row instead of all apps in one row).</td>
   </tr>
</table> 
