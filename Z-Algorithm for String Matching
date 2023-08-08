import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.*;
public class StringMatching {
    public static void main(String[] args) throws IOException {
        BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
        String str=br.readLine();
        String pattern=br.readLine();
        String string=pattern+"$"+str;
        int[] z=new int[string.length()];
        z[0]=0;
        int l=0,r=0;
        int count=0;
        for(int i=1;i<string.length();i++)
        {
            if(i>r)
            {
                l=i;
                r=i;
                while(r<string.length()&&string.charAt(r)==string.charAt(r-l))r++;
                z[i]=r-l;
                r--;
                if(z[i]==pattern.length())count++;
            }else
            {
                int pos=i-l;
                if(z[pos]+i<=r)
                    z[i]=z[pos];
                else
                {
                    l=i;
                    while(r<string.length()&&string.charAt(r)==string.charAt(r-l))r++;
                    z[i]=r-l;
                    r--;
                }
                if(z[i]==pattern.length())count++;
            }
        }
        System.out.println(count);
    }
}
