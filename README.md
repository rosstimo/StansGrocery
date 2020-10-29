# StansGrocery
Stan's Grocery Search Program
***
## Program Function
* Stan's Grocery Store wants to implement a search app
* Write a program that will input items from the disk file
* The program should load the item data into an array that will be accessed as: 
  * `Food$(item, location, category)`
* Allow Stan's customers to enter the name of an item they want to locate by either:
  * typing the item’s name in a text box
  * selecting the item from a combo-box
  * selecting the item from a listbox
* The app will then search the array `Food$` for the desired item
* If found display the item's name, location, and description properly formatted in a the Display Label control
* If the item is not found, inform the customer
* When zzz is typed in the search text box the program stops
***
The Display Label output should resemble the following:

**You will find Cinnamon on aisle 7 with the Spices & herbs**

***
Name program elements **exactly** as follows:
### Files:
StansGrocery.sln
StansGroceryForm.vb
SplashScreenForm.vb
### Controls:
SearchTextBox
SearchButton
DisplayComboBox
DisplayListBox
DiplayLabel
TopMenuStrip
  * File
    * Search
    * Exit
  * Help
    * About

ContextMenuStrip
  * Search
  * Exit

MainToolTip

***

Add the data file "Grocery.txt" to the project Resources folder.

When the program starts, load the contents of the data file into a global array in the StansGroceryForm Class.

  `Dim temp() As String`

  `temp = Split(My.Resources.Grocery, vbNewLine)`

Use this temp array to properly load `Food$(item, location, category)`
