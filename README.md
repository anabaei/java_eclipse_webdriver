# java_eclipse_webdriver
Selenium Webdriver starting 

///////

package gooogl;

import java.io.*;

import org.openqa.selenium.By;
import org.openqa.selenium.NoSuchElementException;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;

public class gooogl {
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		WebDriver driver = new FirefoxDriver();	
	//	driver.get("http://solo.test.bcldb.com/");
	//	driver.findElement(By.className("yellow-button")).click(); 
	//	driver.findElement(By.id("user")).sendKeys("amir.nabaei@bcldb.com");
	//	driver.findElement(By.id("password")).sendKeys("Mahnazaz3");

		   // The name of the file to open.
        String fileName = "sourc4.txt";

        // This will reference one line at a time
        String line = null;

        try {
            // FileReader reads text files in the default encoding.
            FileReader fileReader = 
                new FileReader(fileName);

            // Always wrap FileReader in BufferedReader.
            BufferedReader bufferedReader = 
                new BufferedReader(fileReader);
            
        	driver.get("http://solo.test.bcldb.com/");
        	driver.findElement(By.className("yellow-button")).click(); 
            while((line = bufferedReader.readLine()) != null) {
                driver.findElement(By.id("user")).sendKeys("amir.nabaei@bcldb.com"); 
            	driver.findElement(By.id("password")).sendKeys(line);
            	driver.findElement(By.tagName("input")).submit(); 
         //   	try
       //    	{
//                
//     //       	// driver.findElement(By.className("yellow-button")); 
          //    driver.findElement(By.linkText("GO TO MY APPLICATIONS"));
        //    	 System.out.println(line);	
         //  	}
//            	
        //   	catch(NoSuchElementException ignored)
        //    	{
             System.out.println(line);	
//           //	/.out.println(line);	
          //  	}
            	//	if (w == null)
            //	{
            	//	 System.out.println(w);	
	
            //	}
                                 
            }   

            // Always close files.
            bufferedReader.close();         
        }
        catch(FileNotFoundException ex) {
            System.out.println(
                "Unable to open file '" + 
                fileName + "'");                
        }
        catch(IOException ex) {
            System.out.println(
                "Error reading file '" 
                + fileName + "'");                  
            // Or we could just do this: 
            // ex.printStackTrace();
        }
		
		
		
	//	driver.findElement(By.tagName("input")).submit();
		
		//driver.findElement(By.linkText("GO TO MY APPLICATIONS")).click();
	}
	
	

}
