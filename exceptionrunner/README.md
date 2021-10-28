Timmy Frederiksen

1) logger.log is all logger messages, regardless of their logging levels; whereas with the logged messages on the console have a certain level that it cares about (I see INFO on there, so we know it's at least INFO level).

2) That line comes from the logger.log after a JUnit5 Condition Evaluator tells us that a specific test is not Disabled.

3) Assertions.assertThrows asserts that a certain Exception has been thrown at this point.

4.1) On the internet, I have read that we include this to help with version control of Exceptions, so that we know that we are dealing with a specific version of an Exception and with the class(es) it might interact with

4.2) We do this so that our Exception is meaningful in place of a general Exception. If we are taking the time to write a custom Exception class, why would we want it to be constructed with the general superclass constructor. 

4.3) All we want is for our exception to give us more specific information than a general Exception, there is no need to change Exception functionality. 

5)  The static block gets executed when the class first initializes. This specific block opens the logger.properties file and runs the file as code. This code basically sets up logging properties (shocking, I know).

6) It is written in markdown language. This is a quote from bitbucket on how they use markdown language: "Bitbucket Data Center and Server uses Markdown for formatting text"

7)  We were getting a NullPointerException because of the finally block trying to use a null timeNow in a calculation, now I have changed the code to skip it in that case.

8) The actual issue was that the block did not account for the fact that in the case of a TimerException, we would never get it returned that way because the logic would always cause a NullPointerException before the end of the function.

9 & 10) okay done. will be included in Canvas submission.

11) A NullPointerException is a runtime Exception and the TimerException is an extended class from Exception.

12) okay. 