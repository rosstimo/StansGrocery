## Stan's Grocery Search Program
***
## Program Function
* Stan's grocery store wants to implement a search app
* Write a program that will input items from the disk file
* The program should load the item data into an array that will be accessed as: 
  * `food$(n,3) 'n is the number of items`
  * `food$(n,0) '0 is the item name`
  * `food$(n,1) '1 is the item aisle`
  * `food$(n,2) '2 is the item category`
* Allow Stan's customers to enter the name of an item they want to locate by either:
  * typing the item’s name in a text box
  * selecting the item from a combobox
  * selecting the item from a listbox
* The app will then search the array `food$` for the desired item
* If found display the item's name, location, and description properly formatted in a the Display Label control
* If the item is not found, inform the customer
* When zzz is typed in the search text box the program stops
  
***
The Display Label output should resemble the following:<br>
>**You will find Cinnamon on aisle 7 with the Spices & herbs**
***

Name program elements **exactly** as follows:
### Files:
* StansGrocery.sln
* StansGroceryForm.vb
* SplashScreenForm.vb
* AboutForm.vb
### Controls:
* SearchTextBox<br>
* SearchButton - Accept Button<br>
* FilterComboBox<br>
* DisplayListBox<br>
* DisplayLabel<br>
* FilterGroupBox<br>
  * FilterByAisleRadioButton - Selected by default<br>
  * FilterByCategoryRadioButton<br>
 ### Menus
* TopMenuStrip<br>
  * File<br>
    * Search<br>
    * Exit<br>
  * Help<br>
    * About<br>
* ContextMenuStrip<br>
  * Search<br>
  * Exit<br>
### Other
* MainToolTip<br>

***

* Add the data file "Grocery.txt" to the project folder.<br>
* When the program starts, load the contents of the data file into a global array in the StansGroceryForm Class.
```vb
  Dim fileName as String
  Dim temp() As String

```
Use this temp array to properly load:
`food$(n,0) '0 is the item name`
`food$(n,1) '1 is the item aisle`
`food$(n,2) '2 is the item category`
### DisplayListBox
* The DisplayListBox will contain only item names
* Show only unique names (no duplicates)
* The item names should be in alphabetical order
* Show only the item names from the aisle/category selected in the FilterComboBox
* See also SearchTextBox below

### FilterComboBox
* The first index in the combobox should always be "Show All"
* When the **FilterByAisleRadioButton** is checked
  * The FilterComboBox will contain unique aisle numbers in descending order
* When the **FilterByCategoryRadioButton** is checked
  * The Display ComboBox will contain only unique category names in alphabetical order

### SearchTextBox
* When the SearchButton is clicked the SearchTextBox.Text is evaluated
* The DisplayListBox should show any/all items that contain the search string in any field
* The radio buttons should return to default selection
* The FilterComboBox should update to select "Show All"
* If no match is found:
  * The DisplayListBox should be empty
  * The DisplayLabel should say "Sorry no matches for {searchString}"

### DisplayLabel
* Display only the information of the item currently selected in the DisplayListBox
* Show properly formatted information for the selected item. (name, aisle number, category)
