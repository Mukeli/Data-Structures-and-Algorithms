package algorithms;

/**
 * Created by mukeli on 10/11/15.
 */
public class SpellChecker {
    public static void main(String[] args) {
        SET<String> dictionary = new SET<String>();

        // read in dictionary of words
        In dict = new In(args[0]);
        while (!dict.isEmpty()) {
            String word = dict.readString();
            dictionary.add(word);
        }
        System.out.println("Done reading dictionary");

        // read strings from standard input and print out if not in dictionary
        System.out.println("Enter words, and I'll print out the misspelled ones");
        while (!StdIn.isEmpty()) {
            String word = StdIn.readString();
            if (!dictionary.contains(word)) System.out.println(word);
        }
    }
}

