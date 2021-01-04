import java.util.*;
class twosum
{
    public static int[] twos(int [] nums,int target)
    {
        Map <Integer, Integer> hm = new HashMap<>();
        for(int i=0;i<nums.length;i++)
        {
            int compliment = target-nums[i];
            
            if(hm.containsKey(compliment))
            {
                return new int []{hm.get(compliment),i};
            }
            hm.put(nums[i],i);
        }
        //throw new IllegalArgumentException("No match found");
        return new int[0];
    }

    public static void main(String[] args)
    {
        int arr[]={2,7,11,15,23};
        int tar=9;
        int store[]=new int[5];
        store= twos(arr,tar);
        for (int i=0;i<store.length;i++)
        System.out.print(store[i]);
    }
}
