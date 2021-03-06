Algorithm
OBJECTIVE: To segregate EACH NUMBER COLUMN into 3 columns - international, mobile, landline

Purpose: 
To extract International Mobile numbers and put in separate column
To Separate Landlines from India Mobile and India Landline

Algorithm Process
Sort Existing Number Columns one by one
Habitual Criteria
Truncate the data, remove blank spaces
Remove any dashes (-) 
In case there is a slash (/ ) in the number its a landline number
Starting with +91 is india mobile add “ ‘ “
1 in front or beginning  and 11 digits assume that to be an US and canadian number add ‘+
Starting with 91 and having 12 digits its india mobile so put a “ ‘+ ”
Number begins with single 0 its India Landlines
Number begins with double 00 its international replace 00 with a ‘+
Starts with a + is international

You will be left with numbers starting with 1-9
Number is 11 or more digits, without a +. its international number and add '+ in front
Explanation of Algorithm:
Step 1: download the file either in csv format or in excel format
Step 2: read the file in the jupyter notebook in its particular format
i.e(if you download the file in csv--read_csv(“filename.csv”)
Else if you download it in excel format--read_excel(“filename.xlsx”)
Step 3: data=data.copy()--> copies the data frame which is stored in data for further usage
Step 4: 1)data['Mobile Number'].isnull().sum()
This gives the no.of null values present in the particular column
2)data=data.dropna(subset=['Mobile Number'],how='any')
Using this we drop all the Null values in “Mobile Number” column
Step 5: Now we drop all the columns that we don't need(Eg: columns which contain all NaN values)
	data.drop(columns=["Name of column”],inplace=True)
Step 6: address1=list(data["Address"])
	Here we list out the address into address1 column for further usage
Step 7: Creating three lists 
	Indian=[ ],International=[ ],Indian_landline=[ ]
As you need to store the phone numbers which are to be separated into 3 columns from a single column, we need to create 3 lists, and with the help of “for loop” we’ll be separating every number into its respective list
Step 8: The for loop is the “Algorithm Process” mentioned above.
Step 9: Run the file as mentioned in the document, and be precautious of the
	comments and headings written
Step 10: Now we will Convert the lists into Dataframe
   	Then we Drop the Duplicates And Reset the index
   	Now we need to Drop the Phone number column as it is already converted into 3 lists
Step 11: data.to_excel("Name_team2.xlsx",index=False)
   	change the "Name" of the file 
   	and it will get downloaded in xlsx format.   	
