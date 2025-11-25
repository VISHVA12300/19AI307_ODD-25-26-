# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers.  
The base class **Customer** contains:

- `customerId`  
- `name`  
- `purchaseWeight` (in grams)  
- `goldRatePerGram`

There are two special customer types:

### **RegularCustomer**
- Gets **2% discount** on gold rate per gram.

### **PremiumCustomer**
- Gets **5% discount**  
- Plus an additional **cashback = 1% of final price**

The formula used:

```
finalPrice = purchaseWeight * (goldRatePerGram - discountPerGram)
```

Cashback for premium customers:

```
cashback = 1% of finalPrice
```

Given customer type and purchase details, calculate and display the final price and cashback (if applicable).

---

## AIM:
To write a Java program demonstrating inheritance, method overriding, and dynamic binding to calculate the final price of gold purchases for different types of customers.

---

## ALGORITHM :
1. Start the program.  
2. Create a base class **Customer** with attributes and default discount method.  
3. Extend the class into **RegularCustomer** and **PremiumCustomer** with overridden discount rates.  
4. Implement a method to calculate final price after applying discount.  
5. For PremiumCustomer, also compute cashback = 1% of final price.  
6. In `main()`, read user inputs:  
   - customer type (Regular/Premium)  
   - customerId  
   - name  
   - purchase weight  
   - gold rate per gram  
7. Create the appropriate customer object using dynamic binding.  
8. Display all details including final price and cashback (if applicable).  
9. End the program.

---

## PROGRAM:
```
/*
Program to calculate gold price for different customer types using inheritance
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 2.0;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 5.0;
    }

    double getCashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String type = sc.nextLine().trim();
        String id = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double weight = Double.parseDouble(sc.nextLine().trim());
        double rate = Double.parseDouble(sc.nextLine().trim());

        Customer c;
        if (type.equalsIgnoreCase("Regular")) {
            c = new RegularCustomer(id, name, weight, rate);
        } else {
            c = new PremiumCustomer(id, name, weight, rate);
        }
        c.display();
    }
}
```

---

## OUTPUT:
<img width="823" height="698" alt="image" src="https://github.com/user-attachments/assets/807b0ea9-39c0-4906-b38f-a1ce4c97e20f" />


---

## RESULT:
Thus, the program successfully applies inheritance, method overriding, discount calculations, and cashback computation for different customer types at a jewelry store.
