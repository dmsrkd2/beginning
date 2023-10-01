# beginning

    import java.io.BufferedReader;
    import java.io.IOExeption;
    import java.io.InputStreamReader;
    public class Main
{
    

	public static void main(String[] args) {
	
    BufferedReader bf= new BufferedReader(new InputStreamReader(System.in));
    int num=bf.readLine();
    String str=bf.readLine();
    String arr1[]=str.split();
    String next;
    String arr[];
    
    boolean result[]= new boolean[str.length];
    for(int i=1;i<num;i++)
        next=bf.readLine();
        arr=next.split();
        k=0;
        while(arr[k]!=null){
            if(arr[k]==arr1[k])
            {
                result[k]=true;
            }
            else{
                result[k]=false;
            }
            k++;
        }
    }

    for(int m=0;m<result.length;m++){
                if(result[m]=false){
            arr1[m]="?";
        }
    }
    m=0;
    while(arr1[m]!=0)
    System.out.println(arr1[m]);
    m++;
	}
}
