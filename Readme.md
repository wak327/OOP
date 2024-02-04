# PF: 
 - Input - Output
 - Conditions -  if-else - loop
 - DataType

        Combination 2 things:

        1. How to read Data in the Memory
            a. Integer Type  - Integeral - Integerity - discrete 0 - 1
                aa. char
                00111100  binary to decimal conversion   50
            b. Floating Type - continous 0 - 1 infinite 
                00111100  - 2.8
                IEEE - 
        2. How much memory to read

            1. int - integer - 4 bytes
            2. short(short int) - integer - 2 bytes
            3. long (long int) - integer - 8 bytes
            4. long long (long long int) - integer - 16 bytes
            5. float - floating(IEEE) - 4 bytes
            6. double - floating(IEEE) - 8 bytes
            7. long double - floating(IEEE) - 16 bytes
            8. char - integer - 1 byte

 - Variable

        Combination of 2 compulsory and one supplementary thing
        1. Data Type (Compulsory)
        2. Address in the memory (Compulsory)
        3. Name of the Variable (Supplementary)

    - Declaration of Variable:

        [extra information] [Datatype] [Variable Name];

        e.g. 

        static const int a;

    - Initialization:

        {Declaration} = [value];
        [extra information] [Datatype] [Variable Name] = [value];


    
 - Pointers

        Pointer is a special type of variable which stores addresses of different varibales
        Datatype:
                * - integer - 64 bit (8 byte)

        - Declaration:
            extra-info datatype name

            ```c++
            void * ptr;
            int * int_ptr = 4;
            cout<<int_ptr+1; // 8
            cout<<int_ptr; // 4
            cout<<*int_ptr; //    01101010 01001011 01001010 00100101 // 1783319077
            short int * short_ptr = (short int*)4;
            cout<<short_ptr; // 4
            cout<<short_ptr+1; // 6
            cout<<  * short_ptr; //  01001010 00100101 // 18981
            ```
        - Initialization:
            extra-info(variable type) * name = address of same variable type
    
            ```c++
            int a=10; // 0x000542
            int * int_ptr = &a;
            // short * s_ptr = &a; /// error
            cout <<int_ptr; // 0x000542
            cout << *int_ptr; // 10
            *(int*)(0x000542) = 20;
            cout<<a; // 20
            *int_ptr = 30
            cout<<a; // 30
            ```

    - Array:

        special pointer 
        (variable-type)  name[100] = address of first variable
        ```c++
        short * arr = 4;
        int arr_size = 3;
        *(arr+0) - arr[0] // 01001010 00100101
        *(arr+1) - arr[1] // 01101010 01001011
        *(arr+2) - arr[2] // 10101010 00010101
        ```
            
## Memory
00000001 - 1

10001010 - 2

00010101 - 3

00100101 - 4

01001010 - 5

01001011 - 6

01101010 - 7 

00010101 - 8

10101010 - 9

10010101 - 10

10010101 - 11

10101001 - 12

10101001 - 13

00101010 - 14

01010101 - 15

01001010 - 16

01010101 - 17

10100100 - 18

00001101 - 19


# OOP in C++
- Basic Pillars of OOP
    1. Encapsulation
    2. Abstraction
    3. Inheritance
    4. Polymorphism
## Encapsulation
    same type of data and functions ko eik jagah akatha krny ko encapsulation kehty
    4 tyre
    1 gear box
    1 frame
    4 seats
    4 doors
    2 front lights
    2 back lights
```c++
    bool is_tyres_okay(t1,t2,t3,t4);

    int t1_c1,t2_c1,t3_c1,t4_c1
    int g1_c1
    int f1_c1
    int s1_c1,s2_c1,s3_c1,s4_c1
    int d1_c1,d2_c1,d3_c1,d4_c1
    int f1_c1,f2_c1
    int b1_c1,b2_c1

    

    int t1_c2,t2_c2,t3_c2,t4_c2
    int g1_c2
    int f1_c2
    int s1_c2,s2_c2,s3_c2,s4_c2
    int d1_c2,d2_c2,d3_c2,d4_c2
    int f1_c2,f2_c2
    int b1_c2,b2_c2

    is_tyres_okay(t1_c1,t2_c1,t3_c2,t4_c1);

    class Tyre{
        int size;
        int rim_size;
        int pressure;
        Date Manufacture_date;
        Date Expiry;
    }
    
    class GearBox{
        public:
            string type = Automatic/Manual;
        private:
            string ClutchType = CCVT / AVT / DCT / ; 
    }

    class Car
    {
        Tyre t1,t2,t3,t4;
    public:
        GearBox g;
        Frame f;
        Seat s1,s2,s3,s4;
        Door d1,d2,d3,d4;
        FrontLight f1,f2;
        BackLight b1,b2;

        bool is_tyres_okay();
    };

    Car c1;
    c1.is_tyres_okay(); //
    c1.g.type;
```