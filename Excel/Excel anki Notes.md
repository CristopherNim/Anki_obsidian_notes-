TARGET DECK: EXCEL

What does each formula start with???? #flashcard 
It starts with equal sign (=)
<!--ID: 1625683285494-->

To drag the same formula to the other lines what do you do #flashcard 
go to the corner of the cell and drag to the other cells 
<!--ID: 1625683350300-->

what is the formula to add values from the same column![[Pasted image 20210707144355.png]] #flashcard 
SUM(E1:E12)
<!--ID: 1625683521236-->

what is the formula to sum across columns? #flashcard 
SUM(E24:G24) just an example
<!--ID: 1625683795369-->

How do you reference a cell, and what is the purpose of it #flashcard 
![[Pasted image 20210707145451.png]] 
### The purpose of referencing a cell is to drag the formula to other cells while maintaining the same cell. This is called absolute addressing or locking the row. 
<!--ID: 1625684151861-->

What does pemdas stand for #flashcard 
Please excuse my dear aunt sally
paranthesis exponents Mult div add subtra
<!--ID: 1625684750059-->

Demand curve #flashcard 
[Demand Curve](https://www.economicshelp.org/blog/glossary/demand-curve-formula/) 
![[Pasted image 20210707152225.png]]
<!--ID: 1625685681960-->

Supply curve #flashcard 
The market supply curve shows the combined quantity supplied of goods at different prices. The market supply curve is the horizontal sum of all individual supply curves.
[Supply curve](https://www.economicshelp.org/blog/glossary/supply-curve-equation/)
<!--ID: 1625685939043-->

Locking the column vs the number #flashcard 
=$A3*B$2
- In $A3, you lock the column coordinate because the formula should always multiply the original numbers in column A. The row coordinate is relative since it needs to change for other rows.
- In B$2, you lock the row coordinate to tell Excel always to pick the multiplier in row 2. The column coordinate is relative because the multipliers are in 3 different columns and the formula should adjust accordingly.
- As the result, all the calculations are performed with a single formula, which changes properly for each row and column where it is copied:
![[Pasted image 20210707153114.png]]
<!--ID: 1625686278322-->

What does the MIN() function do #flashcard 
MIN(RETURNS THE SMALLEST NUMBER)
<!--ID: 1625687693806-->


Benefits of using range instead of cell reference #flashcard 
When you create Named Ranges in Excel, you can use these names instead of the cell references.
- For example, you can use =SUM(SALES) instead of =SUM(C2:C11) for the above data set.
- Have a look at ṭhe formulas listed below. Instead of using cell references, I have used the Named Ranges.
	- Number of sales with value more than 500: =COUNTIF(Sales,”>500″)
	-Sum of all the sales done by Tom: =SUMIF(SalesRep,”Tom”,Sales)
	- Commission earned by Joe (sales by Joe multiplied by commission percentage): =SUMIF(SalesRep,”Joe”,Sales)*Commission
<!--ID: 1625689328993-->

What does this do ![[Pasted image 20210707162217.png]] #flashcard 
It grabs the column name and makes it able to grab all the values. For example sum(all_column_B) 
[Excel Link](https://trumpexcel.com/named-ranges-in-excel/)
<!--ID: 1625689606852-->


![[Pasted image 20210707163356.png]] how to grab the avg #flashcard 
I would select command then grab all the cells then name in the name box
<!--ID: 1625690099046-->

Steps to assigning names left instead of the col name #flashcard 
Go to formula then select from selection finally click on the left 
<!--ID: 1625690859956-->

what does average(B:B) do? #flashcard 
AVERAGE(B:B) grabs all the columns in B and averages them, but it causes circular references ![[Pasted image 20210726192414.png]]
<!--ID: 1627341858271-->

how to reference a name from different sheets if the columns have the same name #flashcard 
=SUM(Sheet2!jam)
<!--ID: 1627342456221-->

What is the shortcut to finding a list of all the range names #flashcard 
fn + f3 will give you a list of the special range names
<!--ID: 1627342922151-->

How to create a cell references that uses the values from above #flashcard 
![[Pasted image 20210726204903.png]]
#### create a data range then referring to the value above from the value that you want to use. 
<!--ID: 1627347264878-->

Range data #flashcard 
- You cannot use cell references as names for range data names. For example, you cannot use 3Q.
- only symbols like periods and underscored are allowed.
- make sure data range names make sense to other people and do not put random letters that do not make sense. 
<!--ID: 1627347463367-->

What does the @ do in excel #flashcard 
 - The at symbol is used to shorten formulas inside named tables referencing cells in the same row.
 - to reference the values on the same row for shorten name formulas
 - For example, when averaging the last 5 make sure you the @ to make sure it starts the average from that very row.
 - ![[Pasted image 20210727162823.png]]
<!--ID: 1627416422885-->

VLookup syntax #flashcard 
brackets indicate optional arguments
Vlookup(lookup_value, table_range, column_index, [range_lookups])
# column index 1-col_A, index 2 Col_b etc etc
![[Pasted image 20210727193411.png]]
<!--ID: 1627428772237-->

Lookup best uses and definition #flashcard 
![[Pasted image 20210727193333.png]]
<!--ID: 1627428815965-->

describe false in lookup functions #flashcard 
For example, if you put true it will return a value close to lookup value inputted.
If the value is set to false, and the value is not an exact match in the column it will return N/A. 
![[Pasted image 20210727194822.png]]
<!--ID: 1627429703534-->

What to do when the column is not in ascending order when using the vlookup- #flashcard 
![[Pasted image 20210727195446.png]]
# in the picture the ID has two different answer. The bottom one is right 
![[Pasted image 20210727200750.png]]
# when you omit the fourth value the default value is True ¬
<!--ID: 1627430871821-->

![[Pasted image 20210727203240.png]] syntax to this lookup #flashcard 
=VLOOKUP(45856827,lookup,3,FALSE)
=VLOOKUP(45856827,lookup,2,FALSE)
False because it is not in order 
<!--ID: 1627432414295-->

![[Pasted image 20210727211036.png]] #flashcard 
what does the increment function in the look_up do?
- It gives you the number below from the lookup. In this case if it did you did not input the number it will return the number above since its hlookup function. 
<!--ID: 1627434927251-->


