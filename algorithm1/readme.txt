 Data Cleaning/Management || Final check after Data Cleaning/Management

Explain here the process and the difference use cases or situations you found that you had to resolve and how did you do it
Add any demo files with code in the folder

If all the values of email, phone numbers and addresses are in the same column, segregate it into different columns. After the email, phone numbers, and address are segregated, final duplicacy among the columns are checked. If the email column contains more than one email, it has to be checked whether or not it is the same as the previous. Same has to be done for phone numbers and addresses.

Python -  
Data Filtering -

1.)To separate the email address and phone numbers from a single column, download the file which needs to be segregated in csv format and import it in a jupyter notebook.

2.)  Read and analyze the data to understand which columns/ attributes to work upon. Once the columns are identified, copy its data in a new variable and split it according to its punctuation.
3.) Store the new formed column in the dataset and delete the old column. 
4.) Analyze the new data and repeat the process as many times as need be. 
5.) Store the intermediate data into temporary csv/excel files to understand the further process properly. 
6.) Once the data is cleaned and separated. Save the final file in local PC in excel format inorder to upload it on the google drive.

Data Cleaning - 

1.)Download the file uploaded on the drive in the previous step. 
2.) First create a dataframe with the help of pandas and store the column in which you want to check duplicacy into a variable.
3.)  After that with the help of split() function segregate the values inside the rows on the basis of (/) or (,) into 2 or the no of required different columns. 
4.) Store the 2 columns into different variables. With the help of 2 for loops check every value of one column with every value of the second and if the value matches replace value in any one column with an empty string. Repeat these steps for other columns if needed. Finally save the file into a csv format file and download it into a local PC. Upload the file onto the drive.  

Excel - Same duplicacy checking can be done with the help of excel. 
1.) For splitting into two columns we can use split text to columns function inside the Data tab on the toolbar. 
2.)After that make a new empty column adjacent to the columns you want to check duplicacy. In the empty column make a conditional if function and give an argument as if the value inside column A matches with column B then print True otherwise False. 3.)Append the formulae to all the rows of the datasheet. 
4.)Then with find function search all the true values and manually delete all the duplicate values. This step is more time consuming as compared to using python code. But in case of smaller duplicate values this method shall be preferred.

5.)After checking all the duplicacy, freeze the first row and BOLD all the headings for efficient viewing. Finally save the file as google sheets and repeat the steps for other files. 

