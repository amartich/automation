package cmstest;
import java.io.File;
import java.util.concurrent.TimeUnit;

import jxl.Sheet;
import jxl.Workbook;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;


public class Ebooks {

	public static void main(String[] args) throws Exception {

		File scr = new File("C:/Users/amartich.CMS/Documents/Training/Selenium/Ebooks.xls");
		 
		WebDriver driver = new FirefoxDriver();
		driver.manage().timeouts().implicitlyWait(5, TimeUnit.SECONDS);
		Workbook wb= Workbook.getWorkbook(scr); 
		Sheet sh = wb.getSheet(0);

		for (int fila = 1; fila < sh.getRows(); fila++) {
			
					
			String accesscode = wb.getSheet(0).getCell(0, fila).getContents();
			System.out.println("valor de variable es:" + accesscode);
			// String userpass[]=userpass01.split(";");
			// String user=userpass[0];
			// String pass=userpass[1];
			String email = wb.getSheet(0).getCell(1, fila).getContents();
			System.out.println("valor de variable es:" + email);
			String firstname = wb.getSheet(0).getCell(2, fila).getContents();
			System.out.println("valor de variable es:" + firstname);
			String lastname = wb.getSheet(0).getCell(3, fila).getContents();
			System.out.println("valor de variable es:" + lastname);
			String password = wb.getSheet(0).getCell(4, fila).getContents();
			System.out.println("valor de variable es:" + password);
			

			driver.manage().timeouts().implicitlyWait(8, TimeUnit.SECONDS);
			driver.navigate().to("https://login.cengagebrain.com.mx/cb/login.htm");
			driver.manage().window().maximize();
			driver.findElement(By.id("accesscode")).sendKeys(accesscode);
			driver.findElement(By.className("greenWhiteButton")).click();
			driver.manage().timeouts().implicitlyWait(8, TimeUnit.SECONDS);
			
			
			//String url = ((HttpServletRequest)).getRequestURL().append('?').append(request.getQueryString());
			
			//driver.get("https://login.cengagebrain.com.mx/cb/registerinfo.htm?method=handleAccessCode");
		
			driver.manage().timeouts().implicitlyWait(8, TimeUnit.SECONDS);
			driver.findElement(By.id("newEmail")).sendKeys(email);
			driver.findElement(By.className("greenWhiteButton")).click();
			driver.manage().timeouts().implicitlyWait(8, TimeUnit.SECONDS);
			
			driver.get("https://login.cengagebrain.com.mx/cb/registerinfo.htm?method=noAccessCode");
			driver.manage().timeouts().implicitlyWait(8, TimeUnit.SECONDS);
			driver.findElement(By.id("email")).sendKeys(email);
			driver.findElement(By.id("fname")).sendKeys(firstname);
			driver.findElement(By.id("lname")).sendKeys(lastname);
			driver.findElement(By.id("password")).sendKeys(password);
			driver.findElement(By.id("confirmPassword")).sendKeys(password);
			
			//questionSelect.selectByValue("What is the name of your high school?");
			
			
			WebElement dropDown = driver.findElement(By.id("questionSelectBoxItText"));
			dropDown.click();
		    Select questionSelect = new Select(driver.findElement(By.id("question")));
			questionSelect.selectByValue("What is the name of your high school?");
			
		    //driver.findElement(By.xpath("//span[@id='questionSelectBoxItText']/span[text()]")).click();
		    
			//driver.findElement(By.id("questionSelectBoxItText")).sendKeys("What is the name of your high school?");
			
			
			driver.findElement(By.id("answer")).sendKeys("Carol Morgan School");
			
			//Select timeZone = new Select(driver.findElement(By.id("timeZoneSelectBoxItText" )));
			//timeZone.selectByIndex(1);
			
			WebElement dropDown2 = driver.findElement(By.id("timeZoneSelectBoxItText"));
			dropDown2.click();
		    Select questionSelect2 = new Select(driver.findElement(By.id("timeZone")));
			questionSelect2.selectByValue("America/Halifax");
			//driver.findElement(By.id("timeZoneSelectBoxItText")).click();
			

			
			driver.findElement(By.id("acceptEULA")).click();
			driver.findElement(By.className("greenWhiteButton")).click();
			driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
			
			
			WebElement dropDown3 = driver.findElement(By.id("locationSelectBoxItText"));
			dropDown3.click();
		    Select questionSelect3 = new Select(driver.findElement(By.id("location")));
			questionSelect3.selectByValue("CAR");
			driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
			System.out.println("hOLA");
		
			//JavascriptExecutor js = (JavascriptExecutor)driver;                                         
			//js.executeScript("document.getElementById('case1').style.display='block';");
			//js.executeScript("$('#case1').css('display','block');");
			
			
			
		    //driver.findElement(By.xpath("//div[@class='error']/select[@id='institutionType']")).click();
			Select institution = new Select( driver.findElement(By.cssSelector("#case2>div.formRow>div.input-group>#institutionType")));
			institution.selectByValue("SCHOOLS");
			//WebElement dropDown4 = driver.findElement(By.id("countrySelectBoxItText"));
		    //dropDown4.click();
		 
			
			/*WebElement dropDown4 = driver.findElement(By.id("institutionTypeSelectBoxIt"));
			dropDown4.click();*/
			System.out.println("hOLA1");
			//Select institucion = new Select(driver.findElement(By.id("institutionTypeSelectBoxItOptions")));
			// institucion.selectByValue("SCHOOLS");
		    
			driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
			System.out.println("hOLA2");
		
			
			WebElement dropDown5 = driver.findElement(By.id("countrySelectBoxItText"));
			dropDown5.click();
		    Select questionSelect5 = new Select(driver.findElement(By.id("country")));
			questionSelect5.selectByValue("DOMINICAN REPUBLIC");
			
			/*WebElement dropDown6 = driver.findElement(By.id("citySelectBoxItText"));
			dropDown6.click();
		    Select questionSelect6 = new Select(driver.findElement(By.id("city")));
			questionSelect6.selectByValue("SANTO DOMINGO");*/
			
			Select city = new Select( driver.findElement(By.cssSelector("#case2>div.formRow>div.input-group>#city")));
			city.selectByValue("SANTO DOMINGO");
			
			driver.findElement(By.className("greenWhiteButton")).click();
			driver.manage().timeouts().implicitlyWait(6, TimeUnit.SECONDS);
			
			/*driver.get("https://login.cengagebrain.com.mx/cb/checkuser.htm?method=checkUser");
			driver.manage().timeouts().implicitlyWait(8, TimeUnit.SECONDS);
			Select dropdown = new Select(driver.findElement(By.id("locationSelectBoxItText" )));
			dropdown.selectByIndex(5);
			
			Select dropdown2 = new Select(driver.findElement(By.id("institutionTypeSelectBoxItText" )));
			dropdown2.selectByIndex(1);
			
			Select dropdown3 = new Select(driver.findElement(By.id("countrySelectBoxItText" )));
			dropdown3.selectByIndex(3);
			Select dropdown4 = new Select(driver.findElement(By.id("citySelectBoxIt" )));
			dropdown4.selectByIndex(1);*/
			
			//driver.findElement(By.className("greenWhiteButton")).click();
			//driver.manage().timeouts().implicitlyWait(8, TimeUnit.SECONDS);
			
			driver.findElement(By.id("1-OHRIBJ")).click();
			driver.findElement(By.className("greenWhiteButton")).click();
			driver.findElement(By.linkText("Log Out")).click();

		
		
			
		}

		driver.close();

	}

}
