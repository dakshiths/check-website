package DAA_Programs; import java.util.Random;
import java.util.Scanner; public class SelectionSort {
public static int SIZE = 7000;
PROGRAM
        public static void main(String[] args) throws ArrayIndexOutOfBoundsException {
int a[] = new int[SIZE];
System.out.println("Enter the total number of elements for sorting:"); Scanner sc = new Scanner(System.in);
int n = sc.nextInt();
Random m = new Random();
for (int i = 0; i < n; i++) {
a[i] = m.nextInt(10) + 1; }
System.out.println("\nThe elements before sorting...."); for (int i = 0; i < n; i++) {
System.out.println("" + a[i]); }
long start_time, end_time; VTU 4TH SEM
Page 7
         
21CS42 | DESIGN & ANALYSIS OF ALGORITHM | SEARCH CREATORS
  start_time = System.nanoTime();
selectionSort(a, n);
end_time = System.nanoTime(); System.out.println("\nThe elements after sorting"); for (int i = 0; i < n; i++) {
System.out.println("" + a[i]); }
System.out.println("\nThe time required for sorting " + n + " numbers is: " + (end_time - start_time) + " ns");
}
static void selectionSort(int[] a, int n) {
int i, j, minValue = 0, minIndex = 0, temp; for (i = 0; i < n; i++) {
minValue = a[i]; minIndex = i;
for (j = i; j < n; j++) {
if (a[j] < minValue) { minValue = a[j]; minIndex = j;
} }
if (minValue < a[i]) { temp = a[i];
a[i] = a[minIndex]; a[minIndex] = temp;
}
                VTU 4TH SEM
Page 8

} }
}Gmap
Contact Form

Responsive, Bootstrap Mobile First Web Template
 
Author URI: http://webthemez.com/


Credits
=======
Framework  http://getbootstrap.com
Images	Unsplash (http://unsplash.com - CC0 licensed) 
Icons	Font Awesome (http://fortawesome.github.com/Font-Awesome/)
Other	html5shiv.js (@afarkas @jdalton @jon_neal @rem)

