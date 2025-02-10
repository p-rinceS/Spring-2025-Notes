1/23/25
PTDS Chapters 6.2 & 8.1-8.4


TLDR: Make the data more structured so you can use them.


Common mistake/overlooked is the process of getting the data


Data can be split across files of different types and reference other data


### **Definition**




Transforming the data to be rectangular



### Questions to ask about the structure:
Is the data in a standard format? (CSV/TSV)
is the data organized in records?
Is the data nesting? etc.



Structure: [[Keys]]

Often data will reference other pieces of data

#### When joining 2 Tables
1) Ensure that the primary keys match, they are unique, they should match.
2) I think you can only join tables that utilize a foreign key. 
#### Kinds of Data


Quantitative
	Continuous
		Could be measured to arbitrary precision
	Discrete
		Countable values
	
Categorical
	Ordinal
		Categories with ordered levels, no consistent meaning to difference
	Nominal
		Categories with no specific ordering
		Example:
			Political Affiliation
			Call ID Number
