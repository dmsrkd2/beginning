# beginning

import java.util.Scanner;
import java.util.Arrays;
public class Main
{

public static void main(String[] args) {

Scanner scanner =new Scanner(System.in);

int num=Integer.parseInt(scanner.nextLine());
String str=scanner.nextLine();
String arr1[]=str.split("");
String next="";
String arr[]=new String[str.length()];
boolean result[]= new boolean[str.length()];
Arrays.fill(result,true);

for(int i=1;i<num;i++){
    next=scanner.nextLine();
    arr=next.split("");
    for(int k=0;k<arr.length;k++){
        if(arr[k].equals(arr1[k]))
        {
            continue;
        }
        else{
            result[k]=false;
        }
    }
}


for(int m=0;m<result.length;m++){
        if(result[m]==false){
        arr1[m]="?";
    }
    else{
        continue;
    }
}

String end=String.join("",arr1);
System.out.println(end);

}
}







//다른 답안

N = int(input())
first_word = list(input())
first_word_len = len(first_word)
             
for i in range(N - 1):
    other_words = list(input())
    for j in range(first_word_len):
        if first_word[j] != other_words[j]:
            first_word[j] = '?'

print(''.join(first_word))


//다른 답안2(StringBuilder 사용할 수도 있음)

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        String[] arr = new String[n];
        StringBuilder sb = new StringBuilder();

        for (int i = 0; i < n; i++) {
            arr[i] = sc.next();
        }

        for (int i = 0; i < arr[0].length(); i++) {
            boolean status = true;

            for (int j = 1; j < n; j++) {
                if (arr[0].charAt(i) != arr[j].charAt(i)){
                    status = false;
                }
                }
            if (status){
                sb.append(arr[0].charAt(i));
            }
            else {
                sb.append("?");
            }
            }
        System.out.println(sb);
        }
}


