Question 1:
 
There is a file containing a word and its possible meanings (like a Dictionary). The contents of the file look like this:
 
Apple – a fruit, a tech firm
Table – an object, contains rows and columns when used in context of computers
Orange – a fruit
 
Given a path to the file, do the following:
 
a) Create a method called doesFileExist(String path) which takes the path of the file and tells the user if the file exists at that path or not. Assume all paths are relative to your project structure. If the file does not exist, catch the


——my code—-
from os.path import exists, join
from os import pathsep
from string import split

def doesFileExist(filename, search_path):
"""Given a search path, find file
"""
file_found = 0
paths = string.split(search_path, pathsep)
for path in paths:
if exists(join(path, filename)):
file_found = 1
break
if file_found:
return abspath(join(path, filename))
else:
return None

if __name__ == '___main__':
search_path = '/bin' + pathsep + '/usr/bin' # ; on windows, : on unix
find_file = doesFileExist('ls',search_path)
if find_file:
print "File found at %s" % find_file
else:
print "File not found
——
b) Read each word and its possible meanings and print them out. Your output should look like this:

Word1
Meaning 1
Meaning 2
Word2
Meaning1
Meaning2
 
Use appropriate data structures wherever necessary.
f=open(“f1.txt”)
lines = f.readlines()
for line in lines:
v=line
a,b=line.split (“-“)
b1,b2=b.split ( “,”)
print a + \n
print b1 + \n
print b2 + \n



 
Question 2:
 
The following exercise does not require user login. Please use ID or class as selectors.
 
Steps:
1. Navigate to https://www.weightwatchers.com/us/
2. Verify loaded page title matches “Weight Loss Program, Recipes & Help | Weight Watchers”
3. On the right corner of the page, click on “Find a Meeting”
4. Verify loaded page title contains “Get Schedules & Times Near You”
5. In the search field, search for meetings for zip code: 10011
6. Print the title of the first result and the distance (located on the right of location title/name)
7. Click on the first search result and then, verify displayed location name matches with the name of the first searched result that was clicked.
8. From this location page, print TODAY’s hours of operation (located towards the bottom of the page)
 
Write an automated test for this scenario using WebDriver.
 ——my code —-
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
public class WW1 {

public static void main(String[] args) {
System.setProperty("webdriver.chrome.driver","G:\\chromedriver.exe");
WebDriver driver = new ChromeDriver();
String baseUrl = "https://www.weightwatchers.com/us/";
String expectedTitle = Weight Loss Program, Recipes & Help | Weight Watchers";
String actualTitle = "";

driver.get(baseUrl);
actualTitle = driver.getTitle();
if (actualTitle.contentEquals(expectedTitle)){
System.out.println("Test Passed!");
} else {
System.out.println("Test Failed");
}
driver.close();
}

//next
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
public class WW2 {

public static void main(String[] args) {
System.setProperty("webdriver.chrome.driver","G:\\chromedriver.exe");
WebDriver driver = new ChromeDriver();
String baseUrl = "https://www.weightwatchers.com/us/";
String expectedTitle = "Get Schedules & Times Near You”
String actualTitle = "";

driver.get(baseUrl);
driver.findElement(By.classname("find-a-meeting")).click();
actualTitle = driver.getTitle();
if (actualTitle.contentEquals(expectedTitle)){
System.out.println("Test Passed!");
} else {
System.out.println("Test Failed");
}
driver.close();
}

May do rest later

Question 3:
 
Generate 500 random numbers and print the nth smallest number in a programming language of your choice.
—-my code——
for 1 in 500:
next_random = random.randint(1,500)
if next_random < smallest:
smallest = next_random
print smallest
 