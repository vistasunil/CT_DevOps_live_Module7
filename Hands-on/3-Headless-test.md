<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> HEADLESS TEST </p>

# <div align="center"> DevOps Instructor-led Training </div>

# <div align="right"> $`\textcolor{brown}{\text{Contact us: }}`$  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; </div>

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

## SELENIUM HEADLESS TEST

### The agenda of this demonstration:

We need to automate and run the following test scenario using _Selenium_ **Chrome headless mode** _:_

- Launch the website with the URL https://www.thecloudtrain.com/
- Print the Title of the page.

### Step 1: Use below code to run and understand above demo in eclipse

```
package test;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;

public class headlessDemo {

    public static void main(String[] args) {
        // Selenium Manager (built into Selenium 4.6+) resolves chromedriver automatically,
        // so no System.setProperty("webdriver.chrome.driver", ...) is required.

        //create object of chrome options
        ChromeOptions options = new ChromeOptions();

        //add the headless argument (the new headless mode, Chrome 109+)
        options.addArguments("--headless=new");
        options.addArguments("--disable-gpu");
        options.addArguments("--window-size=1920,1080");

        //pass the options parameter in the Chrome driver declaration
        WebDriver driver = new ChromeDriver(options);

        //Navigate to the site url
        driver.get("https://www.thecloudtrain.com");

        //Print the Title of the Page
        System.out.println("Title of the page is -> " + driver.getTitle());

        //Quit the driver (releases the browser and the driver process)
        driver.quit();
    }
}
```
![image](https://user-images.githubusercontent.com/37858762/236048694-c1d53263-1a52-46cc-8413-8fe57473910c.png)

### Step 2: On executing the code above, the output looks as follows:

![image](https://user-images.githubusercontent.com/37858762/236048726-b4d700e9-6ec8-4806-a847-b43dd2d6daa9.png)

### Refer [Selelinu GitHub Repo](https://github.com/vistasunil/selenium.git) for all source codes.
