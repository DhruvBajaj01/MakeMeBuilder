
Number Segregation by Length (with country in address column)

Based on Country and length (where there is no + in the front)

Number is 8 digits - if address has India assume India

Else assume international
Match for countries name for those that have number without ISD as 9, and if matching put +country code  

Number is 9 digits - if address has India assume India

Else assume international 
Match for countries name for those that have number without ISD as 9, and if matching put + country code  

Number is 10 digits

IF the number is 10 digits check if address column has “India” Else assume international
		
Based on the country in the text put +country code
(watch out for those countries where ISD and number is 10 digits such as Malaysia and Singapore)

Explanation of Algorithm:
(Everyting is same as 2.3 except that Step 7 changes , and from step 8 it is same as step 7 in 2.3 and also the (“for loop”) changes )
Step 1: download the file either in csv format or in excel format
Step 2: read the file in the jupyter notebook in its particular format
i.e(if you download the file in csv--read_csv(“filename.csv”)
Else if you download it in excel format--read_excel(“filename.xlsx”)
Step 3: data=data.copy()--> copies the dataframe which is stored in data for further usage
Step 4: 1)data['Mobile Number'].isnull().sum()
This gives the no.of null values present in the particular column
2)data=data.dropna(subset=['Mobile Number'],how='any')
Using this we drop all the Null values in “Mobile Number” column
Step 5: Now we drop all the columns that we dont need(Eg: columns which contain all NaN values)
	data.drop(columns=["Name of column”],inplace=True)
Step 6: address1=list(data["Address"])
	Here we list out the address into address1 column for further usage
Step 7: If you have 2 columns having address 
1)then just remove the “#” before  this statement #address2=list(data["STATE"])
	2)’’’for i in range(len(address2)):
   		 if type(address2[i])==float:
       			 address2[i]="-" ‘’’
	In this You need to remove the ‘’’ (3 quotation marks before and after loop)
3)Also you need to remove the #: (hash and colon ) before address2 in the for loop (Please refer the IPNB file for the for loop)
Step 8: Creating three lists 
	Indian=[ ],International=[ ],Indian_landline=[ ]
As you need to store the phone numbers which are to be separated into 3 columns from a single column, we need to create 3 lists, and with the help of “for loop” we’ll be separating every number into its respective list
Step 9: The for loop is the “Algorithm Process” mentioned above.
Step 10: Run the file as mentioned in the document, and be precautious of the
	comments and headings written
Step 11: Now we will Convert the lists into Dataframe
   	Then we Drop the Duplicates And Reset the index
   	Now we need to Drop the Phone number column as it is already converted into 3 lists
Step 12: data.to_excel("Name_team2.xlsx",index=False)
   	change the "Name" of the file 
   	and it will get downloaded in xlsx format.   	

