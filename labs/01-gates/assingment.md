# Lab 1: Radek Bábíček

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

  ![image](https://user-images.githubusercontent.com/99410759/154337212-ea6a6800-7841-40ad-91bd-9aa02d56cbca.png)


2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of demorgan is
begin
    f_org_o  <= (not(b_i) and a_i) or (not(c_i) and not(b_i));
    f_nand_o <=	not(b_i or not (a_i)) or not(c_i or b_i);
    f_nor_o  <= not(not(not(b_i) and a_i) and not(not(c_i) and not(b_i)));
end architecture dataflow;
```

3. Complete table with logic functions' values:

| **c** | **b** |**a** | **f(c,b,a)** | **f_NAND(c,b,a)** | **f_NOR(c,b,a)** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 | 1 |
| 1 | 0 | 1 | 0 | 0 | 0 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

![image](https://user-images.githubusercontent.com/99410759/154340395-629cbee8-266d-4e17-a0ba-8f0d3a65adac.png)

2. Link to your public EDA Playground example:

 https://www.edaplayground.com/x/KrGi
