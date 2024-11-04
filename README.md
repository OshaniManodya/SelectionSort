import java.util.Arrays;
public class SelectionSortTest{
    Integer[] a;
    public SelectionSortTest(Integer[] a){
        this.a = a;

    }
    public void swap(int i,int j)
        {
            int temp= a[i];
            a[i]=a[j];
            a[j]=temp;
        }
    public void selectionSort()
    {
        int n = a.length;
        for(int i = 0; i<n-1; i++)
        {
            int min_idx = i;//meya hithagannawa ,eya thamai kotama kiyala 
            for(int  j=i+1; j<n; j++)
            {
                if(a[j] < a[min_idx])
                {
                    min_idx = j;
                }

                System.out.println(
                    "i = " 
                    + (i)
                    + "; j = "
                    + (j)
                    +"; min ="
                    +a[min_idx]
                    +"; "
                    +Arrays.deepToString(a)

                );
            }
            swap(i,min_idx);

        }

    }
    public static void main(String[] args)
    {
       Integer[] a ={76,6, 107,92,21,23,5,9,8,8143};
       System.out.println("Array before sorting =" +Arrays.deepToString(a));
       SelectionSortTest sorter = new SelectionSortTest(a);
       sorter.selectionSort();
       System.out.println("Array After sorting =" +Arrays.deepToString(sorter.a));
    }
}
