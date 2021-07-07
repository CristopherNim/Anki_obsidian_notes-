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


