
		
		package sample;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;

public class verifySignUp {

	public static void main(String[] args) {
	verifySigningup();

	}
 public static void  verifySigningup(){
	 
	 WebDriver driver;
		System.setProperty("webdriver.gecko.driver", "F:\\Geckodriver\\geckodriver.exe");
		
		driver =new FirefoxDriver();
		driver.get("https://www.facebook.com");
		driver.findElement(By.cssSelector("#u_0_1")).sendKeys("John");// I have choose name by using 
		driver.findElement(By.cssSelector("#u_0_3")).sendKeys("Samuel");
		driver.findElement(By.cssSelector("#u_0_6")).sendKeys("john.samuel@gmail.com");
		driver.findElement(By.cssSelector("#u_0_9")).sendKeys("john.samuel@gmail.com");
		driver.findElement(By.cssSelector("#u_0_d")).sendKeys("john@123");
		Select day=new Select(driver.findElement(By.xpath(".//*[@id='day']")));
		day.selectByValue("14");
		Select month=new Select(driver.findElement(By.xpath(".//*[@id='month']")));
		month.selectByValue("Mar");
		Select year=new Select(driver.findElement(By.cssSelector(".//*[@id='year']")));
		year.selectByValue("1997");
		driver.findElement(By.xpath(".//*[@id='u_0_n']/span[2]/label")).click();
		driver.findElement(By.cssSelector("#u_0_h")).submit();
		
		
}
}
