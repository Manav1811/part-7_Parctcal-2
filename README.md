# part-7_Parctcal-2

package part7;
import java.util.*;

public class Practical_2 {

	public static void main(String[] args) {
		System.out.println("This is created by 21CE063_Manav Luhar");
		System.out.println("Enter the words:");
		Scanner sc = new Scanner(System.in);
		String str = sc.nextLine();
		

		Map<String, Integer> hashMap = new HashMap<>();
		String words[] = str.split(" ");
		for (String word : words) {
			Integer integer = hashMap.get(word);

			if (integer == null) {
				hashMap.put(word, 1);
			} else {
				hashMap.put(word, integer + 1);
			}
		}

		ArrayList<String> sortedKeys = new ArrayList<String>(hashMap.keySet());
		Collections.sort(sortedKeys);

		System.out.println("Printing Words:");
		for (String x : sortedKeys) {
			System.out.println(x + " : " + hashMap.get(x));
		}
	}

}
