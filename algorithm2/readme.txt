
Contact number separation
If a column in your dataset contains two or more numbers separated with a comma,
Eg: 8978987903,7890789045
 Then you need to run them through this 2.2 algorithm which divides the two numbers into 2 columns, and follow the instructions as specified in the algorithm.

Algorithm Explanation:
Step 1: download the file either in csv format or in excel format

Step 2: read the file in the jupyter notebook in its particular format
 i.e(if you download the file in csv--read_csv(“filename.csv”)
Else if you download it in excel format--read_excel(“filename.xlsx”)

step 3: Data.shape
   	Returns tuple of shape (Rows, columns) of dataframe.
   
   	Data.head(n)
   	It is used to get the first n rows(specify the number you want to get)
   
   	Data.describe
   	It is used to view some basic statistical details of a data frame

step 4: Drop the null values and reset the index
   	If the Mobile Number columns have any extra characters, tackle with 
   	them before doing any further operations.

step 5: Creating two lists contact1 and contact2
   	Separating the contact numbers with the help of comma
   	The numbers before comma are stored in contact1 and the numbers after 
   	comma are stored in contact2 list

Step 6: Run the file as mentioned in the document, and be precautious of the
	comments and headings written

step 7: Converting the lists into Dataframe
   	Dropping the Duplicates 
   	Resetting the index
   	Dropping the Phone number column as it is already converted into contact1 and
   	contact2
step 8: data.to_excel("Name_team2.xlsx",index=False)
   	change the "Name" of the file 
   	and it will get downloaded in xlsx format.   	
* please do as mentioned in IPYNB file(2.2 algorithm file)

