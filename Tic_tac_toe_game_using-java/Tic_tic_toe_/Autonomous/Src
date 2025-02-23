package com.mcnz.tictactoe;

import java.util.Random;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        char[] board = {'1', '2', '3',
                '4', '5', '6',
                '7', '8', '9'};

        int numberOfSquaresPlayed = 0;
        char whoseTurnItIs = 'x';
        String gameEndingMessage = "";
        Random random = new Random();
        boolean computerPlaysFirst = random.nextBoolean(); //Randomly decide who starts.

        if(computerPlaysFirst){
            System.out.println("Computer plays first!");
        } else {
            System.out.println("You play first!");
        }

        while (numberOfSquaresPlayed < 9) {
            printTheBoard(board);

            if ((computerPlaysFirst && whoseTurnItIs == 'x') || (!computerPlaysFirst && whoseTurnItIs == 'o')) {
                computerMove(board, whoseTurnItIs, random);
            } else {
                getTheUserToSelectTheirSquare(board, whoseTurnItIs);
            }

            if (theyWonTheGame(board, whoseTurnItIs)) {
                gameEndingMessage = (whoseTurnItIs == 'x' && computerPlaysFirst) || (whoseTurnItIs == 'o' && !computerPlaysFirst) ? "Computer won!" : "You won!!! Congratulations!";
                break;
            } else if (numberOfSquaresPlayed == 8) {
                gameEndingMessage = "A tough battle fought to a draw!";
                break;
            } else {
                numberOfSquaresPlayed++;
                whoseTurnItIs = (whoseTurnItIs == 'x') ? 'o' : 'x';
            }
        }
        printTheBoard(board);
        System.out.println(gameEndingMessage);
    }

    private static void computerMove(char[] board, char whoseTurnItIs, Random random) {
        int choice;
        do {
            choice = random.nextInt(9);
        } while (!Character.isDigit(board[choice]));
        board[choice] = whoseTurnItIs;
        System.out.println("Computer chose: " + (choice + 1));
    }

    private static void printTheBoard(char[] board) {
        System.out.printf("%n %s | %s | %s %n", board[0], board[1], board[2]);
        System.out.println(" - + - + - ");
        System.out.printf(" %s | %s | %s %n", board[3], board[4], board[5]);
        System.out.println(" - + - + - ");
        System.out.printf(" %s | %s | %s %n%n", board[6], board[7], board[8]);
    }

    private static void getTheUserToSelectTheirSquare(char[] board, char whoseTurnItIs) {

        do {
            try {
                System.out.printf("Would player %s please choose an unchosen square: ", whoseTurnItIs);
                Scanner scanner = new Scanner(System.in);
                int input = scanner.nextInt();

                if (input >= 1 && input <= 9 && Character.isDigit(board[input - 1])) {
                    board[input - 1] = whoseTurnItIs;
                    break;
                } else {
                    System.out.println("Sorry, that's taken or invalid.");
                }
            } catch (java.util.InputMismatchException e) {
                System.out.println("Invalid input. Please enter a number.");
                Scanner scanner = new Scanner(System.in);
                scanner.next(); // Clear the invalid input from the scanner
            } catch (Exception e) {
                System.out.println("Something went wrong. Let's try that again.");
            }
            printTheBoard(board);
        } while (true);
    }

    private static boolean theyWonTheGame(char[] board, char whoseTurnItIs) {
        return (board[0] == whoseTurnItIs && board[1] == whoseTurnItIs && board[2] == whoseTurnItIs)
                || (board[3] == whoseTurnItIs && board[4] == whoseTurnItIs && board[5] == whoseTurnItIs)
                || (board[6] == whoseTurnItIs && board[7] == whoseTurnItIs && board[8] == whoseTurnItIs)
                || (board[0] == whoseTurnItIs && board[3] == whoseTurnItIs && board[6] == whoseTurnItIs)
                || (board[1] == whoseTurnItIs && board[4] == whoseTurnItIs && board[7] == whoseTurnItIs)
                || (board[2] == whoseTurnItIs && board[5] == whoseTurnItIs && board[8] == whoseTurnItIs)
                || (board[0] == whoseTurnItIs && board[4] == whoseTurnItIs && board[8] == whoseTurnItIs)
                || (board[2] == whoseTurnItIs && board[4] == whoseTurnItIs && board[6] == whoseTurnItIs);
    }
}
