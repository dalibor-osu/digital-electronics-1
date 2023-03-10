# Lab 2: Dalibor Dřevojánek

### 2-bit comparator

1. Karnaugh maps for other two functions of 2-bit comparator:

   Greater than:
   
   ![image](https://user-images.githubusercontent.com/77931392/219444448-c315dba0-f829-4c04-9b0d-9443ef8d644c.png)

   Less than:
   
   ![image](https://user-images.githubusercontent.com/77931392/219444516-d2fa727f-8e04-44d0-aa47-a55c91ef4432.png)

2. Mark the largest possible implicants in the K-map and according to them, write the equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   ![image](https://user-images.githubusercontent.com/77931392/219444756-3da0fa03-e21e-4907-afea-7cb321160b00.png)


### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **xxxx47**

```vhdl
    p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started";

       -- First test case
        s_b <= "0100"; 		  -- 4
        s_a <= "0111";        -- 7
        wait for 100 ns;
        -- Expected output
        assert ((s_B_greater_A = '0') and
                (s_B_equals_A  = '0') and
                (s_B_less_A    = '1'))
        -- If false, then report an error
        report "Input combination COMPLETE_THIS_TEXT FAILED" severity error;

        -- Report a note at the end of stimulus process
        report "Stimulus process finished";
        wait;


        -- Report a note at the end of stimulus process
        report "Stimulus process finished";
        wait; -- Data generation process is suspended forever
    end process p_stimulus;
```

2. Link to your public EDA Playground example:

   [https://www.edaplayground.com/x/6nyK](https://www.edaplayground.com/x/6nyK)
