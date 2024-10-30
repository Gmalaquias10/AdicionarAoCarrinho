import org.junit.After;
import org.junit.Before;
import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;


public class Teste_Compra {

	WebDriver driver;
	
	
	@Before
	public void precondicao(){
		System.setProperty("webdriver.chrome.driver", "C:\\Users\\anton\\Downloads\\chromedriver-win64\\chromedriver-win64\\chromedriver.exe");
			driver = new ChromeDriver();
			driver.get("https://www.nike.com/"); 
			driver.manage().window().maximize();

	}
	
	@Test
	public void testeCompra() throws InterruptedException{
		
		driver.findElement(By.xpath("//button[@class='nds-btn mismatch-country-button css-1snynq4 ex41m6f0 btn-primary-dark  btn-md']")).click();
		Thread.sleep(5000);
		driver.findElement(By.name("search")).sendKeys("Camisa Corinthians");
		Thread.sleep(5000);
		driver.findElement(By.xpath("//button[@class='adopt-c-gSZeic']")).click();
		Thread.sleep(5000);
		driver.findElement(By.xpath("//button[@class='ButtonIcon__StyledButton-sc-wd4o68-0 hScimd']")).click();		
		Thread.sleep(5000);
		driver.findElement(By.xpath("//div[@class='ProductCard-styled__ProductName-sc-31abfcd5-9 cqAYrK']")).click();
		Thread.sleep(5000);
		driver.findElement(By.xpath("//input[@data-testid='product-size-GGG']")).click();
		Thread.sleep(5000);
		driver.findElement(By.xpath("//button[@class='ButtonFill__StyledButton-sc-d418d4ee-0 hYCukR']")).click();
	}
	
	@After
	
	public void posCondicao(){
		
	}
}
