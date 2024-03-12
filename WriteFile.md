# Writing data into files

``` java
import java.io.FileWriter;

public class WriteFile {

	public static void main(String[] args) {
		
		try {
			
			FileWriter fw=new FileWriter("C:\\Users\\SPURGEE\\Documents\\new.txt");
			String str="The man";
			
			fw.write(str);
			fw.close();
			
			System.out.println("Writing is completed");
			

			
			
		}catch(Exception e) {
			e.printStackTrace();
		}

	}

}



```


## output

``` java
Writing is completed.
```
