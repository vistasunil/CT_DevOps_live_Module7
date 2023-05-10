<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> TESTNG ANNOTATIONS </p>

# <div align="center"> DevOps Instructor-led Training </div>

# <div align="right"> $`\textcolor{brown}{\text{Contact us: }}`$  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; </div>

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

## TESTNG ANNOTATIONS IN SELENIUM

### The agenda of this demonstration

The example below verifies the title of the [CloudTrain Home Page](https://www.thecloudtrain.com/). The entire test case has been split into 3 parts.

- Launching the browser will be the first step and hence it is included under the  **@BeforeTest**  Annotation.
- Next is the actual test case which verifies the title, and is therefore included in the  **@Test**  annotation.
- Finally, the quit browser test case is considered under the  **@AfterTest**  annotation.

## Install TestNG

### Step 1: Click on **Help**  and then  **Eclipse Marketplace**.

![image](https://user-images.githubusercontent.com/37858762/236047562-aacbafa0-f966-4100-bab3-b76e5b8374ef.png)


### Step 2:  A new window would open up, wherein you need to type "TestNG" in the Find text box and click on the Go button.

![image](https://user-images.githubusercontent.com/37858762/236047525-85f03133-0887-4b1f-8c5b-6aefe988e71c.png)


### Step 3:  You will now see the search results with TestNG for Eclipse at the top. All you need to do now is click on the Install button next to it.

![image](https://user-images.githubusercontent.com/37858762/236047496-cdfe96c7-f9dc-41ea-b675-6a79f17cddf9.png)


### Step 4: Resolving of features might take up a few minutes after which you need to verify that the checkbox for TestNG is checked and click on the Confirm button.

![image](https://user-images.githubusercontent.com/37858762/236047450-ea1ace66-508d-4f37-97b2-63b65a3f7cf3.png)


### Step 5:  Select **Keep my installation the same** option and again click on the **Confirm** button.

![image](https://user-images.githubusercontent.com/37858762/236047416-b2be2386-7efd-46bb-b81b-8973f928385c.png)

### Step 6: Accept the license and click on the **Finish** button.

![image](https://user-images.githubusercontent.com/37858762/236047396-db2d51b5-012b-44d3-a21d-97df871eba46.png)

**Note:  For the change to be effective, you will have to restart Eclipse and you will now be able to see TestNG installed by right-clicking on any project and seeing TestNG in the menu options.**

![image](https://user-images.githubusercontent.com/37858762/236047367-44526adb-6041-4621-830e-c7ae8bdbdf48.png)


### Step 7: In eclipse you need to add testng library to your project after installation. Right click on project --\> build path --\> Add Libraries --\> TestNG library.

Use below code to run and understand above demo in eclipse

```
package test;

import org.testng.annotations.Test;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.Assert;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;

public class Test1 {
  public String baseUrl = " https://www.thecloudtrain.com";
  String driverPath = "C:\\chromedriver.exe";
  public WebDriver driver ;
  
  @BeforeTest
  public void launchBrowser() {
    System.out.println("launching Chrome browser");
    System.setProperty("webdriver.chrome.driver", driverPath);
    driver = new ChromeDriver();
    driver.get(baseUrl);
  }
  @Test
  public void verifyHomepageTitle() {
    String expectedTitle = " DevOps Workshop | Cloudtrain";
    String actualTitle = driver.getTitle();
    Assert.assertEquals(actualTitle, expectedTitle);
  }
  
  @AfterTest
  public void terminateBrowser(){
    driver.close();
  }
}
```

![image](https://user-images.githubusercontent.com/37858762/236047297-6817746c-1ab9-4b84-8628-32d6f493cb81.png)


### Step 8: On executing the code above, the output looks as follows:

![image](https://user-images.githubusercontent.com/37858762/236047226-6f8c2759-b10c-4639-a7bc-ab46c772fbdf.png)


### Step 9:  This is how it works. Now let’s understand how to include @BeforeSuite and @BeforeMethod Annotations.

```
package test;

import org.testng.annotations.AfterClass;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.AfterSuite;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeClass;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.BeforeSuite;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

public class testngAnnotations {
  // Test Case 1
  @Test
  public void test1() {
    System.out.println("Test Case 1");
  }
  
  // Test Case 2
  @Test
  public void test2() {
    System.out.println("Test Case 2");
  }
  
  @BeforeMethod
  public void beforeMethod() {
    System.out.println("Before Method");
  }
  
  @AfterMethod
  public void afterMethod() {
    System.out.println("After Method");
  }
  
  @BeforeClass
  public void beforeClass() {
    System.out.println("Before Class");
  }
  
  @AfterClass
  public void afterClass() {
    System.out.println("After Class");
  }
  
  @BeforeTest
  public void beforeTest() {
    System.out.println("Before Test");
  }
  
  @AfterTest
  public void afterTest() {
    System.out.println("After Test");
  }
  
  @BeforeSuite
  public void beforeSuite() {
    System.out.println("Before Suite");
  }
  
  @AfterSuite
  public void afterSuite() {
    System.out.println("After Suite");
  }
}
```

In the above example, the sequence is changed and then the program is executed. When this program is run, the output will appear in the sequence as shown below. It should look like this:

![image](https://user-images.githubusercontent.com/37858762/236047021-fddb8e04-f49c-4793-839a-10cf8d259977.png)
