# CodeMinSwap
public class HelloWorld{

public static void minimumBribes(int[] q) {
  //  [2,1,5,3,4]
  //  [1,2,5,3,4]
  //1,2,3,4,5
  int n=q.length;
  int bribe =0;
  int flag=0;
  for(int i=0;i<n;i++)
        if(q[i]==i+1){
            bribe ++;
            int temp=q[i];
                q[i]=q[i+1];
                q[i+1]=temp;
        }
        else if(q[i]==i+2){
             bribe +=2;
           
             int temp=q[i];
                q[i]=q[i+1];
                q[i+1]=temp;
        }
        else{
            flag++;
        
        }
        if(flag==1)  System.out.println("Too chaotic");
        System.out.println(bribe);
    }
     public static void main(String []args){
            int[] arr={2 ,1, 5, 3, 4};
            minimumBribes(arr);
     }
}
