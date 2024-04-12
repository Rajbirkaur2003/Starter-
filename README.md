public class Starter1 {
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        int roll = 0;
        int[] diceRolls = new int[20];

        int totalRolls = 0;
        for (int count = 0; count < 1000; count++) {
            roll = (int) (Math.random() * 20) + 1;
            diceRolls[roll - 1] = diceRolls[roll - 1] + 1; // corrected indexing
        }
        for (int index = 0; index < diceRolls.length; index++) { // corrected array length accessor
            System.out.printf("Count of %d is : %d%n", (index + 1), diceRolls[index]); // corrected format specifier and indexing
            totalRolls = totalRolls + diceRolls[index];
        }
        System.out.println("Total rolls were: " + totalRolls);
        System.out.println("Program by Rajbir KAUR");
    }
}
