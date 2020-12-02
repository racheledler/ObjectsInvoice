package com.company;


import java.util.ArrayList;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        // create an invoice for a store
        // input products and prices
        // print out invoice
        //exit

        ArrayList<ProductInventory> stock = new ArrayList<ProductInventory>();
        ArrayList<Purchases> purchases = new ArrayList<Purchases>();


        ProductInventory inventory = new ProductInventory();
        inventory.setProduct("Bison Sweater");
        inventory.setPrice(55.99);
        stock.add(inventory);

        inventory = new ProductInventory();
        inventory.setProduct("Bison Tee");
        inventory.setPrice(14.99);
        stock.add(inventory);

        inventory = new ProductInventory();
        inventory.setProduct("Bison Hoodie");
        inventory.setPrice(23.99);
        stock.add(inventory);

        inventory = new ProductInventory();
        inventory.setProduct("Bison Bumpersticker");
        inventory.setPrice(4.99);
        stock.add(inventory);

        Scanner input = new Scanner(System.in);
        String answer = "";
        String product = "";
        double total = 0.0;
        int index  = -1;

        do {
            System.out.println("What would you like to do? ");
            System.out.println("1.) Add purchase 2.) Show purchases 3.) Finish transaction");
            answer = input.nextLine();

            if (answer.equals("1")) {
                System.out.print("Product: ");
                product = input.nextLine();
               ProductInventory order = new ProductInventory();

                for (int i =0; i < stock.size(); i++){

                    String t = stock.get(i).getProduct();
                    if (t.equals(product))
                    {
                        index = i;
                        String pProd = stock.get(index).getProduct();
                        double pPrice = stock.get(index).getPrice();
                        order.setPurchase_Product(pProd);
                        order.setPurchase_Price(pPrice);
                        purchases.add(order);

                    }


                }

            } else if (answer.equals("2")) {
                for (int i = 0; i < purchases.size(); i++) {

                    System.out.println(purchases.get(i).getPurchase_Product() + " - " + purchases.get(i).getPurchase_Price());
                }

            }


        } while (!answer.equals("3"));

        for (int i = 0; i < purchases.size(); i++) {

            double productPrice = purchases.get(i).getPurchase_Price();
            total += productPrice;
        }
        System.out.println("Thank you for shopping at Howard University! Your total is:  " + total + ".");
    }
}



