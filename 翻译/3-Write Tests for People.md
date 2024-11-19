## Write Tests for People

You are writing automated tests for some or all of your production code. Congratulations! You are writing your tests before you write the code? Even better!! Just doing this makes you one of the early adopters on the leading edge of software engineering practice. But are you writing good tests? How can you tell? One way is to ask "Who am I writing the tests for?" If the answer is "For me, to save me the effort of fixing bugs" or "For the compiler, so they can be executed" then the odds are you aren't writing the best possible tests. So Who should you be writing the tests for? For the person trying to understand your code.

Good tests act as documentation for the code they are testing. They describe how the code works. For each usage scenario the test(s):

- Describe the context, starting point, or preconditions that must be satisfied
- Illustrate how the software is invoked
- Describe the expected result or postconditions to be verified

Different usage scenarios will have slightly different versions of each of these. The person trying to understand your code should be able to look at a few tests and by comparing these three parts of the tests in question, be able to see  what causes the software to behave differently. Each test should clearly illustrate the cause and effect relationship between these three parts. this implies that what isn't visible in the test is just as important as what is visible. Too much code in the test distracts the reader with unimportant trivia. Whenever possible hide much trivia behind meaningful method calls -- the Extract Method refactoring is your best friend. And make sure you give each test a meaningful name that describes the particular usage scenario so the test reader doesn't have to reverse engineer each test to understand what the various scenarios are. Between them, the names of the test class and class method should include at least the  starting point and how the software is being invoked. This allows the test coverage to be verified via a quick scan of the method names. It can also be useful to include the expected results in the test method names as long as this doesn't cause the names to be too long to see or read.



