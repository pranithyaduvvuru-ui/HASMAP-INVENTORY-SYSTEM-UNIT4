# HASMAP-INVENTORY-SYSTEM-UNIT4
This project uses Java HashMap to manage inventory items efficiently. It supports adding, updating, searching, and deleting products. It demonstrates key-value data handling, fast lookup operations, and effective inventory management using Java collections.
# 📦 Inventory Management System (Java - HashMap)

## 📌 Overview

This project is a simple **Inventory Management System** built using Java.
It demonstrates how **HashMap** can be used to efficiently store and manage product data using key-value pairs.

---

## 🎯 Objective

To design a system that:

* Stores product details
* Calculates total stock value
* Displays inventory report
* Uses efficient data structures for storage

---

## 🧠 Concepts Used

* **HashMap (Key-Value Pair)**
* **Collections Framework**
* **User Input using Scanner**
* **Basic Calculations**

---

## 🛠️ Technologies

* Java
* HashMap (java.util)

---

## 📂 Project Structure

```id="d9k2p1"
InventorySystem/
│
├── InventorySystem.java   (Main File)
```

---

## 💻 Source Code

```java
import java.util.HashMap;
import java.util.Scanner;

public class InventorySystem {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        HashMap<String, Integer> inventory = new HashMap<>();

        System.out.println("===== INVENTORY MANAGEMENT SYSTEM =====");
        System.out.println("Enter the product details below");
        System.out.println();

        System.out.print("Enter Product Name: ");
        String product = sc.nextLine();

        System.out.print("Enter Quantity: ");
        int quantity = sc.nextInt();

        System.out.print("Enter Price of each item: ");
        int price = sc.nextInt();  

        inventory.put(product, quantity);

        System.out.println();
        System.out.println("===== INVENTORY REPORT =====");

        for (String item : inventory.keySet()) {
            int qty = inventory.get(item);
            int totalValue = qty * price;

            System.out.println("Product Name : " + item);
            System.out.println("Available Quantity : " + qty);
            System.out.println("Price per Item : " + price);
            System.out.println("Total Stock Value : " + totalValue);
            System.out.println("--------------------------------------");
        }

        System.out.println("Inventory successfully stored using HashMap.");
        System.out.println("The system allows efficient storage and retrieval of product data.");
        System.out.println("HashMap provides fast access using key-value pair structure.");
    }
}
```
<img width="954" height="437" alt="1" src="https://github.com/user-attachments/assets/68796bb5-7a23-4655-a7ae-0cfadca9ebd4" />

---

## ▶️ How to Run

1. Save file as `InventorySystem.java`
2. Compile:

```id="z1v8p3"
javac InventorySystem.java
```

3. Run:

```id="p7q4n6"
java InventorySystem
```

---

## 📥 Sample Input

```id="k5x9m2"
Laptop
5
50000
```

---

## 📤 Sample Output

```id="c3r8t1"
===== INVENTORY REPORT =====
Product Name : Laptop
Available Quantity : 5
Price per Item : 50000
Total Stock Value : 250000
--------------------------------------
```

---

## 🚀 Future Enhancements

* Store multiple products
* Use ArrayList with HashMap
* Add update and delete operations
* Connect with database
* Build GUI using Java Swing

---

## 📌 Conclusion

This project demonstrates how **HashMap** can be used to efficiently manage data in Java. It provides a simple understanding of storing and retrieving information using key-value pairs.
