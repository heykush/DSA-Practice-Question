# Solutions

- **Input a year and find whether it is a leap year or not.**
    
    > *The year is multiple of 400.
    The year is multiple of 4 and not multiple of 100.*
    > 
    
    ```java
    int year = input.nextInt();
    if (year%400==0 || (year%4==0 && year%100!=0)){
        System.out.println("This is Leap year");
    
    } else{
        System.out.println("not leap year");
    }
    ```
    
- **Take two numbers and print the sum of both.**
    
    ```java
    Scanner input= new Scanner(System.in);
    int num1=input.nextInt();
    int num2 =input.nextInt();
    int sum = num1+num2;
    System.out.println("Sum of numbers= "+ sum);
    ```
    
- **Take a number as input and print the multiplication table for it.**
    
    ```java
    Scanner in = new Scanner(System.in);
    int number= in.nextInt();
    for (int count=1; count<=10;count++ ){
        int table=number*count;
        System.out.println(number +"x" + count+ "=" + table);
    }
    ```
    
- **Write a program to print whether a number is even or odd, also take input.**
    
    ```java
    Scanner in= new Scanner(System.in);
    int num=in.nextInt();
    if (num % 2 != 0) {
        System.out.println("odd number");
    } else {
        System.out.println("Even number");
    }
    ```
    
- **Take name as input and print a greeting message for that name.**
    
    ```java
    Scanner in=new Scanner(System.in);
    String name=in.next();
    System.out.println("Hello" +" "+ name);
    ```
    
- **Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest.**
    
    > *Simple Interest = (P*R*T)/100*
    > 
    
    ```java
    Scanner in = new Scanner(System.in);
    float Principal = in.nextFloat();
    float Time= in.nextFloat();
    float Rate= in.nextFloat();
    float SI= (Principal*Time*Rate)/100;
    System.out.println(SI);
    ```
    
- **Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions).**
    
    ```java
    Scanner in = new Scanner(System.in);
    int num1 =in.nextInt();
    char op=in.next().charAt(0);
    int num2 = in.nextInt();
    
    int result=0;
    if (op=='+'){
        result = num1+num2;
        System.out.println(result);
    }
    else if( op =='-'){
        result=num1-num2;
        System.out.println(result);
    }
    else if (op == '*'){
        result=num1*num2;
        System.out.println(result);
    
    }else if(op=='/'){
        result=num1/num2;
        System.out.println(result);
    }
    else {
        System.out.println("InValid Operator");
    }
    ```
    
- **Take 2 numbers as input and print the largest number**.
    
    ```java
    Scanner in = new Scanner(System.in);
    int num1 = in.nextInt();
    int num2 = in.nextInt();
    if (num1>num2){
        System.out.println("Largest number :" + " " + num1);
    } else {
        System.out.println("Largest number :" + " " + num2);
    }
    ```
    
- **Input currency in rupees and output in USD.**
    
    ```java
    Scanner in = new Scanner(System.in);
    float indianrupee = in.nextFloat();
    float usd = (float) (0.01326*indianrupee);
    System.out.println(indianrupee + " INR" +" : "+ usd +" " + "USD");
    ```
    
- **To calculate Fibonacci Series up to n numbers.**
    
    <aside>
    💡 Fibonacci Series : 0 1 1 2 3 5 8 13 21 34
    
    </aside>
    
    ```java
    Scanner in= new Scanner(System.in);
    int n=in.nextInt();
    int a= 0, b=1;
    for (int count =0;count<n; count++ ) {
        System.out.println(a);
        int temp = b;
        b = a + b;
        a = temp;
    }
    ```
    
- **To find out whether the given String is Palindrome or not.**
    
    <aside>
    💡 A palindrome is a string, which, when read in both forward and backward ways is the same.
    
    </aside>
    
    ```java
    Scanner in = new Scanner(System.in);
    String str = in.nextLine();
    int length = str.length();
    String rev = "";
    for (int i = length - 1; i >= 0; i--) {
        rev = rev + str.charAt(i);
    }
    if (str.equals(rev)) {
        System.out.println("its a palindrome");
    } else {
        System.out.println("its not palindrome");
    }
    ```
    
- **To find Armstrong Number between two given numbers.**
    
    <aside>
    💡 **Armstrong number** is a number that is equal to the sum of cubes of its digits. For example 0, 1, 153, 370, 371 and 407 are the **Armstrong numbers**.
    
    </aside>
    
    ```java
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int num1=in.nextInt();
        int num2=in.nextInt();
        for (int i = num1; i < num2; i++) {
            if (fun(i)) {
                System.out.println(i);
            }
        }
    }
    
        static boolean fun ( int num){
            int orignal = num;
            int sum = 0;
            while (num > 0) {
                int rem = num % 10;
                sum = sum + rem * rem * rem;
                num = num / 10;
            }
            return sum == orignal;
        }
    ```
    
- **Area of Circle**
    
    ```java
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        float radius = in.nextFloat();
        System.out.println(area(radius));
    
    }
    static float area(float radius){
        float a=(22*radius*radius)/7;
        return a;
    }
    ```
    
- **Area of Triangle**
    
    ```java
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        float height =in.nextFloat();
        float base=in.nextFloat();
        System.out.println(area(height, base));
    }
    static float area(float a, float b){
        float area = (a*b)/2;
        return area;
    }
    ```
    
- **Area of Triangle if sides are given**
    
    <aside>
    💡 Condition: Sum of either two sides greater than third side                                                                                           *S=(a+b+c)/2*                                                                                       **Area=sqrt(s*(s-a)*(s-b)*(s-c))(s*(s-a)*(s-b)*(s-c))**
    
    </aside>
    
    ```java
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int s1=in.nextInt();
        int s2=in.nextInt();
        int s3=in.nextInt();
        System.out.println(area(s1,s2,s3));
    
    }
    static float area(int a, int b, int c) {
        if ((a + b) > c && (b + c) > a && (c + a) > b) {
            int s = (a + b + c) / 2;
            float area = (float) Math.sqrt(s * (s - a) * (s - b) * (s - c));
            return area;
        }
        return 0;public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int s1=in.nextInt();
        int s2=in.nextInt();
        int s3=in.nextInt();
        System.out.println(area(s1,s2,s3));
    
    }
    static float area(int a, int b, int c) {
        if ((a + b) > c && (b + c) > a && (c + a) > b) {
            int s = (a + b + c) / 2;
            float area = (float) Math.sqrt(s * (s - a) * (s - b) * (s - c));
            return area;
        }
        return 0;
    ```
    
- **Area Of Rectangle**
    
    ```java
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int length=in.nextInt();
        int breadth =in.nextInt();
        System.out.println((area(length, breadth)));
    }
    static int area(int a, int b){
        return a*b;
    }
    ```
