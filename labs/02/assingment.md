# Lab 2: YOUR_FIRSTNAME LASTNAMEE

### 2-bit comparator

1. Karnaugh maps for other two functions:

   Greater than:

   ![image](https://user-images.githubusercontent.com/99410759/155109033-d8e74a73-29c4-4f93-8911-d1d2d7d8a184.png)


   Less than:

  ![image](https://user-images.githubusercontent.com/99410759/155108903-859121c9-2620-4a08-8477-3e03c7b1a322.png)


2. Equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

![image](https://user-images.githubusercontent.com/99410759/155108729-3a72de9c-b33c-4b56-9e58-9a7fa173d1bf.png)

### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **xxxx??**

```vhdl
    p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started" severity note;

        -- First test case
        s_b <= "0001"; -- my ID = xxxx19
        s_a <= "1001";        -- my ID = xxxx19
        wait for 100 ns;
        -- Expected output
        assert ((s_B_greater_A = '0') and
                (s_B_equals_A  = '0') and
                (s_B_less_A    = '1'))
        -- If false, then report an error
        report "Input combination FAILED" severity error;

        -- Report a note at the end of stimulus process
        report "Stimulus process finished" severity note;
        wait;
    end process p_stimulus;
```

2. Text console screenshot during your simulation, including reports.

   ![image](https://user-images.githubusercontent.com/99410759/155112830-04792c37-b804-449c-9f53-9ff7654b8597.png)


3. Link to your public EDA Playground example:

   https://www.edaplayground.com/x/Vnqb
