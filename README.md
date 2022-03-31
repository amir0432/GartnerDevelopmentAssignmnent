# GartnerDevelopmentAssignmnent

**Please note the project is added as a zip file named 'DevelopmentAssignmnent', kindly unzip and download to see the project.**

  - Installation steps  
  The code is created using visual studio, it is simple console application after importing the code you click on sln file present in the root directory and that shall open the code in visual studio, you may then run the code via start button of visual studio.
  
  
  - How to run your code / tests
	Code can be run on visual studio by clicking on start button, Unit tests are present in project named 'DevelopmentAssignmnent.Tests' of the same solution, as the unit tests are created using MS Test, hence no additional package is required, you can simply run the by going on 'Test' > 'Run All Tests', you can also run them clicking Ctrl + R, A
	After running the code it would ask user "Please enter type of weekly feed", then user can add any stirng, currently dummy static data is displayed for any string apart from where user enters "csv", if user enters "csv" the logic for csv data would be called as curently no logic is provied for the same hence, it will throw exception "NotImplementedException"
  
  - Where to find your code
  Code is present on below mentioned link, same is shared in email body.
  
  
  - Was it your first time writing a unit test, using a particular framework, etc?
  No, I have created Unit Tests previously as well, I have used MS Test and for mocking I have used Moq.
  
  - What would you have done differently if you had had more time
  If I had more time I would had implemented Data Access Layer as well that would be loosely coupled and would had been able to implement various types of data sources.
  I also would have implemented more dynamic input output format, wherein any type of input type can be given for various types of source content eg yaml, txt, json, XML etc.
  
  - Code Explanation
	I have a created a solution wherein the service for reading the data from various sources is abstracted using interfaces, these service are defined in Business folder as Contracts and Implementation.
	I have also created a factory class named 'WeeklyFeedFactory' that creates the implementation class for our interface service depending on the user input, for example if user provides csv as the input format, it shall call the 'ImportWeeklyFeedCsv' concrete class to implement weekly feed reading logic for csv, please note currently the feed reading logic of csv is not implemented.
	Currently I have created a 'ImportWeeklyFeed' concrete class in which dummy data is created in static manner, later on if team needs to call any data source the can do so by adding that logic here.
	I have created a unit test case project named "DevelopmentAssignmnent.Tests" that is covering method "PrintFeedData" present in "WeeklyFeed.cs" class, it uses Moq mocking to separate the external dependencies present on this method.
