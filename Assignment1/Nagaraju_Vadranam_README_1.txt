Aim: To find the number of Discharges in each state 

Instructions(s) to Execute the program:

 -->The Usage of this Jar is as follows use the following commands to run the Jar in Hadoop
	-->To Run the required Program (question) in this Jar just pass partial or full name of the program that you want to Run
		    Syntax:: <command> { hadoop jar <this Jar Name>.jar <ProgramName> <inputFile> <OutputFolder> 
		    Example :: <commandExample> { hadoop jar Nagaraju_Vadranam_PA1.jar program1 hdfs://hadoop1:9000/CS5433/PA1/Medicare.csv hdfs://hadoop1:9000/nvadran/Outputs/TestOutput1Attempt2 }
	--> To View Available Classes :: <commandExample> { hadoop jar Nagaraju_Vadranam_PA1.jar -ls } 
	--> To View output in part File ::   <command Syntax> { hdfs dfs -cat <Your output folder until part file>} 
		    <commandExample> { hdfs dfs -cat hdfs://hadoop1:9000/nvadran/Outputs/TestOutput1Attempt1/par* } 

Architectural Flow:
  Entry point:

  	Calling starts from HadoopPAOne.Driver.Main() which Inturns calls the Initiate() method in each program
  
  Design :
  
	The Nagaraju_Vadranam_Program_1.Java file consists its required Mapper and Reducer and Initiate() to process the job


 Output :
   
       The Following String is added to Key and value to make more sense to the output

       "The state :: "+<Key>+" :: has the discharges as follows :: "+<Value>"

Note::You can run all programs with one command line

   ccommand  :: hadoop jar Nagaraju_Vadranam_PA1.jar all hdfs://hadoop1:9000/CS5433/PA1/Medicare.csv hdfs://hadoop1:9000/nvadran/Outputs/TestOutput1Attempt1

in case if you run all programs at one you coul dsee all the outputs at once to 

--> To View output in part File(s) ::   <command Syntax> { hdfs dfs -cat <Your output folder until part file>} 
		    <commandExample> { hdfs dfs -cat hdfs://hadoop1:9000/nvadran/Outputs/TestOutput1Attempt1_*/par* } 

