<!-- this worksheet covers chapters 8 & 16 of Deitel -->

# Correct the Code

1. The code below defines class Product, with a no-argument constructor that sets the product's name to an empty String and the price to 0.00, and a toProductString method that return sa String containing the product's name and its price.
   
   {: .language.java}
       public class Product
       {
           private String name;
           private double price;
       
           public void Product()
           {
               name = "";
               price = 0.00;
           }
       
           public toString()
           {
               return String.format("%s costs %.2d", name, price);
           }
       }
   
2. The code segment below defines another constructor for class Product that takes two arguments and assigns those arguments to the corresponding variables.
   
   {: .language.java}
       public Product(String name, double price)
       {
           name = name;
           price = price;
       }
   
3. The following segment defines two set methods to set the name and the price of the Product.
    
   {: .language.java}
       public setName()
       {
           this.name = name;
       }
       
       public setPrice()
       {
           this.price = price;
       }
   
4. The following two lines should create a Product object and display a String containing the values of the object's instance variables.
   
   {: .language.java}
       Product p1 = new Product("Milk", 5,5);
       System.out.printf("%s %.2f\n", p1.name, p1.price);
   
5. The segment below should create a Product object, set the values of its instance variables and display a String containing the values of the intsance variables.
   
   {: .language.java}
       Product p1 = new Product();
       p1.setName();
       p1.setPrice();
       System.out.println(p1.toString("Eggs", 3));
