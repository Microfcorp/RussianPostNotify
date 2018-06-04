# RussianPostNotify
Console application and library<br>
Example applications including
## Library command
```C#
Interface interfac = new Interface(); //initialize new class interfaces

interfac.NewNotifyIcon("App", new Icon(SystemIcons.WinLogo, 40, 40), interfac.NotifyIcon_ShowClose); //created notify icon. Param: Name, icon, EventHadler from click (standart open/close console)

Barcode brc = interfac.ReadFilesBarcode(Environment.CurrentDirectory + "\\barcode.txt"); //loading barcodes from file, and new Barcode(string[] names, string[] barcodes)

int collbarcode = interfac.Gets(brc, Interface.DateType.Barcode).Length - 1; //Get data (Interface.DateType (barcode and names))

interfac.ShowBallownTip(300, "Start", "Start yes", ToolTipIcon.Info); //Show BallownTip (standart)

TrackData trc = ConnectTracking.ConnectToPochta(brc, i); //New trackdata code

string status = ParsingTracking.GetData(trc, ParsingTracking.DataType.humanStatus); //Gets string data on TrackData and ParsingTracking.DataType

interfac.PrintMess(status); //Printing in console
```
