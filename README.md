# DiscountApp

package gr.aueb.cf.ch3;

import java.util.Scanner;

/**
 * o χρηστης εισαγη την τιμη του προιοντος και το ποσοστο εκπτωσης και το προγραμμα
 * υπολογιζει την τελικη τιμη
 *
 * η τιμη θα πρεπει να ειναι μεγαλυτερη  απο το 0
 * και η εκπτωση μεγαλυτερη ιη ιση απο το 0 και μικροτερο η ισο απο το 100
 */

public class DiscountApp {



    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int price = 0;
        int discount = 0;
        int result = 0;

        while (true) {


            System.out.println("Εισαγετε την τιμη του προιοντος");
            price = sc.nextInt();


            if (price == 0){
                System.out.println("Εξοδος");
                break;
            }
            if (price < 0) {
                System.out.println("η τιμη δεν μπορει να ειναι 0");
                continue;

            }
            System.out.println("Παρακαλω εισαγετε την εκπτωση");
            discount = sc.nextInt();
            if ( discount < 0  || discount > 100 ) {
                System.out.println("Η εκπτωση πρεπει να ειναι μεταξυ 0-100.");

            }


            result = price * (100 - discount ) / 100;
            System.out.println("Η τελικη τιμη ειναι \n" + result);

            System.out.println("Ευχαριστουμε που μας επιλεξατε");
            break;





        }


    }
}
