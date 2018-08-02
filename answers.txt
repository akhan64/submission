{\rtf1\ansi\ansicpg1252\cocoartf1504\cocoasubrtf830
{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;\red25\green25\blue25;\red255\green255\blue255;\red106\green62\blue181;
}
{\*\expandedcolortbl;;\cssrgb\c12941\c12941\c12941;\cssrgb\c100000\c100000\c100000;\cssrgb\c49412\c34118\c76078;
}
\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\sl300\partightenfactor0

\f0\b\fs26 \cf2 \cb3 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Question 1:
\b0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 \'a0\
There is a file containing a word and its possible meanings (like a Dictionary). The contents of the file look like this:\
\'a0\
Apple \'96 a fruit, a tech firm\
Table \'96 an object, contains rows and columns when used in context of computers\
Orange \'96 a fruit\
\'a0\
Given a path to the file, do the following:\
\'a0\
a) Create a method called doesFileExist(String path) which takes the path of the file and tells the user if the file exists at that path or not. Assume all paths are relative to your project structure. If the file does not exist, catch the\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 \'97\'97my code\'97-\
\pard\pardeftab720\sl300\partightenfactor0

\b \cf2 from
\b0 \'a0os.path\'a0
\b import
\b0 \'a0exists
\b ,
\b0 \'a0join\

\b from
\b0 \'a0os\'a0
\b import
\b0 \'a0pathsep\

\b from
\b0 \'a0string\'a0
\b import
\b0 \'a0split\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0

\b \cf2 \cb3 def
\b0 \'a0doesFileExist
\b (
\b0 filename
\b ,
\b0 \'a0search_path
\b ):
\b0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0

\i \cf2 \cb3 """Given a search path, find file
\i0 \cb1 \

\i \cb3 """
\i0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 file_found\'a0
\b =
\b0 \'a0
\b 0
\b0 \cb1 \
\cb3 paths\'a0
\b =
\b0 \'a0string
\b .
\b0 split
\b (
\b0 search_path
\b ,
\b0 \'a0pathsep
\b )
\b0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0

\b \cf2 \cb3 for
\b0 \'a0path\'a0
\b in
\b0 \'a0paths
\b :
\b0 \cb1 \

\b \cb3 if
\b0 \'a0exists
\b (
\b0 join
\b (
\b0 path
\b ,
\b0 \'a0filename
\b )):
\b0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 file_found\'a0
\b =
\b0 \'a0
\b 1
\b0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0

\b \cf2 \cb3 break
\b0 \cb1 \

\b \cb3 if
\b0 \'a0file_found
\b :
\b0 \cb1 \

\b \cb3 return
\b0 \'a0abspath
\b (
\b0 join
\b (
\b0 path
\b ,
\b0 \'a0filename
\b ))
\b0 \cb1 \

\b \cb3 else:
\b0 \cb1 \

\b \cb3 return
\b0 \'a0None\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0

\b \cf2 \cb3 if
\b0 \'a0__name__\'a0
\b ==
\b0 \'a0'___main__'
\b :
\b0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 search_path\'a0
\b =
\b0 \'a0'/bin'\'a0
\b +
\b0 \'a0pathsep\'a0
\b +
\b0 \'a0'/usr/bin'\'a0
\i # ; on windows, : on unix
\i0 \cb1 \
\cb3 find_file\'a0
\b =
\b0 \'a0doesFileExist
\b (
\b0 'ls'
\b ,
\b0 search_path
\b )
\b0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0

\b \cf2 \cb3 if
\b0 \'a0find_file
\b :
\b0 \cb1 \

\b \cb3 print
\b0 \'a0"File found at %s"\'a0
\b %
\b0 \'a0find_file\

\b else:
\b0 \cb1 \

\b \cb3 print
\b0 \'a0"File not found\
\'97\'97\
\
b) Read each word and its possible meanings and print them out. Your output should look like this:\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 Word1\
Meaning 1\
Meaning 2\
Word2\
Meaning1\
Meaning2\
\'a0\
Use appropriate data structures wherever necessary.\
f=open(\'93f1.txt\'94)\
lines = f.readlines()\
for line in lines:\
v=line\
a,b=line.split (\'93-\'93)\
b1,b2=b.split ( \'93,\'94)\
print a + \\n\
print b1 + \\n\
print b2 + \\n\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 \'a0\
\pard\pardeftab720\sl300\partightenfactor0

\b \cf2 Question 2:
\b0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 \'a0\
The following exercise does not require user login. Please use ID or class as selectors.\
\'a0\
Steps:\
1. Navigate to\'a0{\field{\*\fldinst{HYPERLINK "https://www.weightwatchers.com/us/"}}{\fldrslt \cf4 \ul \ulc4 \strokec4 https://www.weightwatchers.com/us/}}\
2. Verify loaded page title matches \'93Weight Loss Program, Recipes & Help | Weight Watchers\'94\
3. On the right corner of the page, click on \'93Find a Meeting\'94\
4. Verify loaded page title contains \'93Get Schedules & Times Near You\'94\
5. In the search field, search for meetings for zip code: 10011\
6. Print the title of the first result and the distance (located on the right of location title/name)\
7. Click on the first search result and then, verify displayed location name matches with the name of the first searched result that was clicked.\
8. From this location page, print TODAY\'92s hours of operation (located towards the bottom of the page)\
\'a0\
Write an automated test for this scenario using WebDriver.\
\'a0\'97\'97my code \'97-\
import org.openqa.selenium.WebDriver;\
import org.openqa.selenium.chrome.ChromeDriver;\
public class WW1 \{\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 public static void main(String[] args) \{\
System.setProperty("webdriver.chrome.driver","G:\\\\chromedriver.exe");\
WebDriver driver = new ChromeDriver();\
\
String baseUrl = "{\field{\*\fldinst{HYPERLINK "https://www.weightwatchers.com/us/"}}{\fldrslt \cf4 \ul \ulc4 \strokec4 https://www.weightwatchers.com/us/}}";\
String expectedTitle = Weight Loss Program, Recipes & Help | Weight Watchers";\
String actualTitle = "";\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 driver.get(baseUrl);\
actualTitle = driver.getTitle();\
if (actualTitle.contentEquals(expectedTitle))\{\
System.out.println("Test Passed!");\
\} else \{\
System.out.println("Test Failed");\
\}\
driver.close();\
\}\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 //next\
import org.openqa.selenium.WebDriver;\
import org.openqa.selenium.chrome.ChromeDriver;\
public class WW2 \{\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 public static void main(String[] args) \{\
System.setProperty("webdriver.chrome.driver","G:\\\\chromedriver.exe");\
WebDriver driver = new ChromeDriver();\
\
String baseUrl = "{\field{\*\fldinst{HYPERLINK "https://www.weightwatchers.com/us/"}}{\fldrslt \cf4 \ul \ulc4 \strokec4 https://www.weightwatchers.com/us/}}";\
String expectedTitle = "Get Schedules & Times Near You\'94\
String actualTitle = "";\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 driver.get(baseUrl);\
driver.findElement(By.classname("find-a-meeting")).click();\
actualTitle = driver.getTitle();\
if (actualTitle.contentEquals(expectedTitle))\{\
System.out.println("Test Passed!");\
\} else \{\
System.out.println("Test Failed");\
\}\
driver.close();\
\}\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 May do rest later\
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0

\b \cf2 \cb3 Question 3:
\b0 \cb1 \
\pard\pardeftab720\sl300\partightenfactor0
\cf2 \cb3 \'a0\
Generate 500 random numbers and print the nth smallest number in a programming language of your choice.\
\'97-my code\'97\'97\
for 1 in 500:\
next_random = random.randint(1,500)\
if next_random < smallest:\
smallest = next_random\
print smallest\
}