# Reading the files


## Method1 

``` java
import java.io.*;
import java.util.*;
public class Read {

	public static void main(String[] args)  {
		
		try {
			File file=new File("input.properties");
			Scanner sc=new Scanner(file);
			
			while(sc.hasNextLine()) {
				String data=sc.nextLine();
				System.out.println(data);
			}
		}catch (Exception e) {
			e.printStackTrace();
		}
		
	}

}


```

## Output

```Java
M3BE.DB.HOST = 13.250.67.210
M3BE.DB.USER = MDBUSR
M3BE.DB.ENV = MVXJDTA
M3BE.DB.DBNAME = M3FDBM3M
M3BE.DB.PWD = Infor2013

```

## Method2

``` java
import java.io.BufferedReader;
import java.io.File;
import java.io.FileReader;

public class ReadFile {

	public static void main(String[] args) {
		
		try {
			
			File file=new File("C:\\\\Users\\\\SPURGEE\\\\Documents\\\\input.properties");
			FileReader fr=new FileReader(file);
			
			BufferedReader br=new BufferedReader(fr);
			
			String line;
			
			while((line=br.readLine())!=null) {
				
				System.out.println(line);
			}
			
			
		}catch(Exception e) {
			e.printStackTrace();
		}
		
		
		
	}

}
```

## Output

```Java
M3BE.DB.HOST = 13.250.67.210
M3BE.DB.USER = MDBUSR
M3BE.DB.ENV = MVXJDTA
M3BE.DB.DBNAME = M3FDBM3M
M3BE.DB.PWD = Infor2013

```



## Assingment


``` Java
import java.io.File;
import java.util.Scanner;

public class FileReading {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int count=0;
		int line=1;
		int lineNum=0;
		
		try {
			File file =new File("C:\\Users\\SPURGEE\\Downloads\\input.properties");
			Scanner fileRead=new Scanner(file);
			
			while(fileRead.hasNextLine()) {
				count++;
				String data=fileRead.nextLine();
//				String g=new String(data);
				if(count==line) {
					System.out.println(count);
					System.out.println(data);
					
					for(int i=0;i<data.length();i++) {
						if(data.charAt(i)== '=') {
							lineNum=i;
							String user=data.substring(0,i-1);
							String password=data.substring( i+2,data.length()-1);
							System.out.println(user);
							System.out.println (password);
							
						}
					}
					
					break;
				}
				
			}

		}catch(Exception e) {
			System.out.println(e);
			e.printStackTrace();
		}

	}

}

```

## Output

```Java
M3BE.DB.HOST
13.250.67.210


```
