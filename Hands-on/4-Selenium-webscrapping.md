<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> SELENIUM WEBSCRAPPING </p>

# <div align="center"> DevOps Instructor-led Training </div>

# <div align="right"> $`\textcolor{brown}{\text{Contact us: }}`$  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; </div>

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

## SELENIUM AUTOMATED TEST IN ECLIPSE

### The agenda of this demonstration:

1. To open the [https://www.ibm.com](https://www.ibm.com/) website,
2. To put a search input (e.g.: DevOps), click on search,
3. In the last search result page find a 'DevOps – IBM Developer – IBM Developer', click on the item
4. In that last search result page see if the Title matches to our Desired Item or not, if matches display one message and display the Featured Products and Why IBM details.

### Step 1: Before moving ahead let us first add required **Maven Dependencies** in the **pom.xml** file. Also, initialize the web driver. Refer to the Selenium Installation Documentation. Now our **App.java** file should look like this:

![image](https://user-images.githubusercontent.com/37858762/236051171-43879681-c36b-4317-b36b-fbb91ac14c79.png)

And **pom.xml** file should look like this:

![image](https://user-images.githubusercontent.com/37858762/236051194-8e800cfe-5663-4156-928d-b7b92dfe269c.png)

We are all set to start our demonstration,

### Step 2: Open the IBM website.

```
driver.get("https://www.ibm.com");
driver.manage().window().maximize();
```

This command will open the IBM website and then it will maximize the browser window.

![image](https://user-images.githubusercontent.com/37858762/236051218-a0eb27dc-fccb-4f73-8ff3-c1a2007e2484.png)

### Step 3: Import the following before moving ahead.

```
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.By;
```

![image](https://user-images.githubusercontent.com/37858762/236051250-bd18cb87-c651-4f00-a4c4-a144c16779d2.png)

### Step 4: Now we will find the search input element in the website, inspect the element, find the class name, also find the id of the search click button by inspecting.

```
driver.findElement(By.id("q")).sendKeys("DevOps");
driver.findElement(By.className("ibm-search-link")).click();
driver.manage().timeouts().implicitlyWait(3,TimeUnit.SECONDS);
```

Here, we have added one time-out of 3 secs.

![image](https://user-images.githubusercontent.com/37858762/236051277-f1e3adc3-3bcc-49b3-a12e-8e6065dfa2f0.png)

### Step 5: Now in the last search result page we will find a "DevOps – IBM Developer – IBM Developer" and click on the item. If item is not found display a "Item not found" message.

```
	String firstData = driver.findElement(By.className("ibm--result-item__title")).getText();
	String CheckData = "What is DevOps? | IBM";
	System.out.println(firstData);
	
	if(firstData.equals(CheckData)) {
		driver.findElement(By.className("ibm--result-item__title")).click();
		driver.manage().timeouts().implicitlyWait(3,TimeUnit.SECONDS);
	}
	else {
		System.out.println("Item not found");
	}
```

It should look like this:

![image](https://user-images.githubusercontent.com/37858762/236051330-f3dad063-a467-4511-a40e-9a462de4e490.png)

```    
	String actualData = driver.findElement(By.className("bx--type-expressive-heading-05")).getText();
	String expectedData = "DevOps";
	System.out.println(actualData);
		
	if(actualData.equals(expectedData)) {
		System.out.println("Found String!\n---------------");			
		String products = driver.findElement(By.className("ibm-link-list")).getText();
		String whyIbm = driver.findElement(By.className("ibm-plain-list")).getText();
		System.out.println("Featured Products: \n"+ products + "\nWhy IBM:\n---------------\n" + "\n"+ whyIbm);
		System.out.println("---------------\nTest Successful");
		//driver.close();	
	}
	else {
		System.out.println("Oops!! String Not Found.");
	}
```

### Step 6: In that last search result page we will check if the Item Title matches to our Desired Event Title or not, if matches display one message and display the Upcoming events for that item.

It looks like this:

![image](https://user-images.githubusercontent.com/37858762/236051382-f4cba094-4c9e-4fd3-a023-155a995e2335.png)

### Step 7: Now run the program. A Chrome browser window will pop up. See the results as shown below:

First, opens ibm.com website window.

![image](https://user-images.githubusercontent.com/37858762/236051410-2688da22-2a76-42c8-b770-ea78eb9f4f96.png)

Then clicks on the **"What is DevOps? | IBM".**

![image](https://user-images.githubusercontent.com/37858762/236051437-bcb4650d-37e8-44ae-ae62-8245b1f99ed7.png)

Finally lands on the item page. And then window gets closed.

![image](https://user-images.githubusercontent.com/37858762/236051450-aa1217ff-0568-48ae-a00a-ccb81e0f7557.png)

### Step 8: Now see the eclipse console. It should display our **Featured Products and Why IBM** of list item as shown below.

![image](https://user-images.githubusercontent.com/37858762/236051466-6d79b90e-f41f-4b8d-aab6-e6bfd4956b2b.png)

**Congratulations**! You have successfully completed your first **Selenium Automated Test.**


### Test one more example using below code:

```
package test;
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class App {
	public static void main(String[] args) {
		System.setProperty("webdriver.chrome.driver", "C:\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.get("https://www.ibm.com");
		driver.manage().window().maximize();		
		driver.findElement(By.id("q")).sendKeys("Introduction to DevOps Capabilities");
		driver.findElement(By.className("ibm-search-link")).click();
		driver.manage().timeouts().implicitlyWait(3,TimeUnit.SECONDS);
		
		String firstData = driver.findElement(By.className("ibm--result-item__title")).getText();
		String CheckData = "Introduction to DevOps Capabilities";
		
		if(firstData.equals(CheckData)) {
			driver.findElement(By.className("ibm--result-item__title")).click();
			driver.manage().timeouts().implicitlyWait(3,TimeUnit.SECONDS);
		}
		else {
			System.out.println("Course not found");
		}
	    
		driver.findElement(By.className("bx--btn--secondary")).click();
		String actualData = driver.findElement(By.className("pl-header-subtitle")).getText();
		String expectedData = "Course code: C120019G";
		
		if(actualData.equals(expectedData)) {
			System.out.println("Found Course!");			
			String dateView = driver.findElement(By.className("course-card-icons")).getText();
			System.out.println("Course Details: \n"+ dateView + "\n"); 
			System.out.println("Test Successful");
			driver.close();	
		}
		else {
			System.out.println("Oops!! String Not Found.");
		}		
	}
}
```

### New Version with Bing.com example:

```
package test;

import java.util.concurrent.TimeUnit;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class App {

	public static void main(String[] args) {
		System.setProperty("webdriver.chrome.driver", "C:\\chromedriver.exe");
		WebDriver driver;
		driver = new ChromeDriver();
		driver.get("https://bing.com");
		driver.manage().window().maximize();
		
		driver.findElement(By.name("q")).sendKeys("DevOps");
		driver.findElement(By.id("search_icon")).click();
		driver.manage().timeouts().implicitlyWait(8,TimeUnit.SECONDS);
		
		String firstData = driver.findElement(By.className("b_algo")).getText();
		String CheckData = "What is DevOps? DevOps Explained | Microsoft Azure";
		System.out.println(firstData);
		String[] arrOfStr = firstData.split("\n",0);
		System.out.println(arrOfStr[0]);	

		if(arrOfStr[0].equals(CheckData)) {
			driver.findElement(By.className("b_title")).click();
			driver.manage().timeouts().implicitlyWait(3,TimeUnit.SECONDS);
		}
		else {
			System.out.println("Item not found");
		}

		String items = driver.findElement(By.id("global-subnav")).getText();
		System.out.println(items);
		
		driver.close();

	}

}
```
