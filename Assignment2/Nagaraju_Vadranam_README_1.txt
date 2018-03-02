Aim: To fimplement secondary sort on values descending and show the maximum discharges for Cities

Instructions(s) to Execute the program:

 -->The Usage of this Jar is as follows use the following commands to run the Jar in Hadoop
	-->To Run the required Program (question) in this Jar just pass partial or full name of the program that you want to Run
		    Syntax:: <command> { hadoop jar <this Jar Name>.jar <ProgramName> <inputFile> <OutputFolder> 
		    Example :: <commandExample> { hadoop jar Nagaraju_Vadranam_PA2.jar program1 hdfs://hadoop1:9000/CS5433/PA1/Medicare.csv hdfs://hadoop1:9000/nvadran/Outputs/TestOutput1Attempt2 }
	--> To View Available Classes :: <commandExample> { hadoop jar Nagaraju_Vadranam_PA2.jar -ls } 
	--> To View output in part File ::   <command Syntax> { hdfs dfs -cat <Your output folder until part file>} 
		    <commandExample> { hdfs dfs -cat hdfs://hadoop1:9000/nvadran/Outputs/TestOutput1Attempt1/par* } 

Architectural Flow:
  Entry point:

  	Calling starts from HadoopPATwo.Driver.Main() which Inturns calls the Initiate() method in each program
  
  Design :
  
	The Nagaraju_Vadranam_Program_1.Java file consists its required Mapper and Reducer and Initiate() to process the job
        The CompositeKey (Mykeypair.jva) consists custom class type
        The Partitioner(MyPartitioner.jva) consists partitioner logic
        The Keycomparator(KeyComparer.jva) consists compare logic on keys
	The GroupComparator(Grouper.jva) consists Grouping logic on keys
	Finally,Driver.java(main()) to organize help and calling the initiate() in Nagaraju_Vadranam_Program_1.Java 


 Output :
   
       the output

       "<Key>" "<Value>"


--> To View output in part File(s) ::   <command Syntax> { hdfs dfs -cat <Your output folder until part file>} 
		    <commandExample> { hdfs dfs -cat hdfs://hadoop1:9000/nvadran/Outputs/TestOutput1Attempt1_*/par* } 

