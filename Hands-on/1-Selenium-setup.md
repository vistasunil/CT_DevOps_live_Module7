<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> SELENIUM SETUP </p>

# <div align="center"> DevOps Instructor-led Training </div>

# <div align="right"> $`\textcolor{brown}{\text{Contact us: }}`$  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; </div>

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

## SELENIUM SETUP IN ECLIPSE

**This documentation is divided into three parts:**

1. **Java JDK installation**
2. **Eclipse installation**
3. **Selenium Test Case**

## 1. Install Java JDK

### Step 1: Download java jdk.

https://www.oracle.com/technetwork/java/javase/downloads/index.html

![image](https://user-images.githubusercontent.com/37858762/236043748-2f82c736-b77c-47a4-8c34-0deae38471bc.png)

Then Click on the oracle Jdk Download button, you will land on a page as shown below. Accept the License Agreement. Download the .exe file.

![image](https://user-images.githubusercontent.com/37858762/236043763-07629117-4744-4adf-a265-2084f2040537.png)

### Step 2: Open that downloaded execution file then click on **Next**.

![image](https://user-images.githubusercontent.com/37858762/236043796-6fd979de-7af8-47cd-a7d4-3b56ec75ee05.png)

### Step 3: Select **Developers Tools** and click **Next**.

![image](https://user-images.githubusercontent.com/37858762/236043834-48334777-dcad-4616-bcd4-5073ac0199c7.png)

### Step 4: It will take a few moments to set up jdk in your system

![image](https://user-images.githubusercontent.com/37858762/236043856-63b31c1a-25d3-4780-ac83-659ff2b9bda5.png)

### Step 5: Click on close to complete the set up.

![image](https://user-images.githubusercontent.com/37858762/236043871-a2fd9e38-8c6d-422e-831f-4303ddcf920d.png)

### Step 5: Before moving ahead, we need **to add the environment variables to the path** as follows. Go to local **C drive**  Program Files java  **jdk-16.0.1**  **bin**

![image](https://user-images.githubusercontent.com/37858762/236043907-fa0ebf57-4ce2-40f1-9821-6579a32ed6e0.png)

### Step 6: Copy the path as shown above. ### Step 7: Go to **Control Panel**  **System and Security**  **System**  **Advanced System Settings**

![image](https://user-images.githubusercontent.com/37858762/236043927-c0187ca9-ffc9-45aa-84aa-5f5e9985c39c.png)

### Step 8: Click on **Environment Variables.**

![image](https://user-images.githubusercontent.com/37858762/236043968-4f252c3b-0c4b-48f4-8ba6-4d2fd0a03dbb.png)

### Step 9: Click on Path in the System Variables section. And then paste the previously copied path (_ **C:\Program Files\Java\jdk-16.0.1\bin** _) as shown below.

![image](https://user-images.githubusercontent.com/37858762/236043993-86358e57-4bd8-439c-b9ac-dac3635cc6f1.png)

### Step 10: Now open **command prompt** and run the following command.

`java -version`

![image](https://user-images.githubusercontent.com/37858762/236044029-4730c7f9-7697-4085-b20d-5178a69124ab.png)

## 2. Eclipse Installation

### Step 1: Go to the eclipse download page.

https://www.eclipse.org/downloads/

![image](https://user-images.githubusercontent.com/37858762/236044066-867929bc-3818-4b36-9a0d-8edc8369d6ec.png)

### Step 2: Click on the download 64-bit link. You should land on a page as shown.

![image](https://user-images.githubusercontent.com/37858762/236044097-f367a6f4-8f69-45d9-9e1a-741cebdde9d1.png)

### Step 3: Once the download is finished launch the installer.

![image](https://user-images.githubusercontent.com/37858762/236044113-a4a8d036-24a0-4db4-9d41-e09dcfc9a01a.png)

### Step 4: Click on **Eclipse IDE for Java Developers**

![image](https://user-images.githubusercontent.com/37858762/236044124-b5c53271-27b6-4305-bdc7-f1574a109da4.png)

### Step 5: Once done, click on LAUNCH.

![image](https://user-images.githubusercontent.com/37858762/236044142-7ffeed73-2f63-4e90-8beb-6590311bff66.png)

### Step 6: Click on Launch.

![image](https://user-images.githubusercontent.com/37858762/236044166-8bd6b333-5fc5-4665-bb28-4be716d6e1f9.png)

**Now that we have successfully set up Java and Eclipse in our environment, we will be Performing a Selenium Test Case using Maven.**

## 3. Selenium Test Case

### Step 1: Download and extract chromedriver.exe from zip file downloaded from [Selenium Download Page](https://chromedriver.chromium.org/downloads) to any location say C:\ drive:

![image](https://user-images.githubusercontent.com/37858762/236044200-0ea5ebbe-c971-4455-92a3-359242a363d1.png)

_**Note:** If running on mac, then running below command to allow it run from unknown developer:_\

`xattr -d com.apple.quarantine chromedriver`

Start a new Maven Project.

![image](https://user-images.githubusercontent.com/37858762/236044217-0b728354-4c27-4b5e-906c-d87bf21435d7.png)

### Step 2: Check the **Create a Simple Project** box. And click **Next.**

![image](https://user-images.githubusercontent.com/37858762/236044236-514a3977-b8a7-44bd-ba84-a7b09bd962ad.png)

### Step 3: Enter **Group Id** and **Artifact Id.** And click on **Finish.**

![image](https://user-images.githubusercontent.com/37858762/236044269-62fb714c-1165-4f9b-a602-eec25ad241ea.png)

### Step 4: Your project should appear in the **Project Explorer** section as shown below.

![image](https://user-images.githubusercontent.com/37858762/236044288-7c3f0dec-badd-4b11-8c25-713f645fb7d9.png)

### Step 5: Right click on **src/main/java** and create a **java package.** Enter a **Package Name (Test** in this case**).** Then click on **Finish.**

![image](https://user-images.githubusercontent.com/37858762/236044311-2696504b-56b0-4471-b831-1318e25b3553.png)

### Step 6: Now create a **Java Class** by right clicking on **test package** , name the class as **App.** Check the **Public static void main(String[] args)** box **.** And click on **Finish.**

![image](https://user-images.githubusercontent.com/37858762/236044334-22bf8b58-0641-4ef0-9677-459ad87a50a6.png)

### Step 7: Now, your eclipse workspace should look like this.

![image](https://user-images.githubusercontent.com/37858762/236044376-a955f3d4-4f90-4b0f-a04c-1b3c699b1e0f.png)

Before moving on to the scripting part we need to **configure the Maven Dependencies to perform Selenium in Eclipse**. We will be adding the **Maven Dependencies** to the **Pom.xml** file under **target folder**.

![image](https://user-images.githubusercontent.com/37858762/236044402-94884ffd-7cca-4783-a698-7a2013aa19f9.png)

Before adding the dependencies, the Pom.xml file looks like this:

![image](https://user-images.githubusercontent.com/37858762/236044434-62a12653-f541-4ed7-b464-3d4090041483.png)

### Step 8: Now go ahead and add the below dependencies to the **pom.xml** file.

```
<dependencies>
  <!-- Selenium -->
  <dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-java</artifactId>
    <version>3.4.0</version>
  </dependency>
  <!-- TestNG -->
  <dependency>
    <groupId>org.testng</groupId>
    <artifactId>testng</artifactId>
    <version>6.8</version>
    <scope>test</scope>
  </dependency>
  <!-- Selenium Server-->
  <dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-server</artifactId>
    <version>3.141.59</version>
  </dependency>
</dependencies>
```
Add the dependencies in between **\<project\> \</project\>** tags.

Refer to the below given image.

![image](https://user-images.githubusercontent.com/37858762/236044490-b9041a42-ce6f-451c-89ba-76b0deaa892e.png)

```
System.setProperty("webdriver.chrome.driver", "C:\\chromedriver.exe");
WebDriver driver = new ChromeDriver();
driver.get("http://www.gmail.com/");
System.out.println("Test Successful");
```

### Step 9: Now, add the below given script to the **main() function** to the **App.java** file.

### Step 10: To make this run properly we need to import **org.openqa.selenium.WebDriver** and **org.openqa.selenium.chrome.ChromeDriver**

```
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
```

It should look like this.

![image](https://user-images.githubusercontent.com/37858762/236044520-3d7ef266-c320-4804-b7bd-6e0732278c8e.png)

### Step 11: Now run **App**. Chrome browser window will pop up with Gmail sign in page.

![image](https://user-images.githubusercontent.com/37858762/236044557-e992a268-5d8b-47c6-bb19-26f60c4626cd.png)

### Step 12: Go to Eclipse again and see the console. You should see the Test Successful message appearing in there.

![image](https://user-images.githubusercontent.com/37858762/236044587-6d854eac-708e-44aa-bbf3-b2f5dc067750.png)
