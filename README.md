# 8BIT_SYNCHRONOUS_UP-DOWN_COUNTER
# AIM: 
To simulate and synthesis 8bit synchronous up-down counter  using vivado. 
# APPARATUS REQUIRED: 
vivado 2023.2 software. 
# PROCEDURE: 
STEP:1 Start the vivado software, Select and Name the New project. 

STEP:2 Select the device family, device, package and speed. 

STEP:3 Select new source in the New Project and select Verilog Module as the Source type. 

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it. 

STEP:5 Select the run simulation and then run Behavioral Simulation in the Source Window and click the check syntax. 

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table. 

STEP:7 compare the output with truth table.
# DIAGRAM:
![image](https://github.com/RESMIRNAIR/8BIT_SYNCHRONOUS_UP-DOWN_COUNTER/assets/154305926/e1af47bf-e77f-446e-9fe0-e0ca3d1a7cfd)
# Here is a diagram showing the circuit in the "up" counting mode
![image](https://github.com/RESMIRNAIR/8BIT_SYNCHRONOUS_UP-DOWN_COUNTER/assets/154305926/8a6dd34b-5226-4d93-9bff-d87ab85aeabc)
# Here, shown in the "down" counting mode
![image](https://github.com/RESMIRNAIR/8BIT_SYNCHRONOUS_UP-DOWN_COUNTER/assets/154305926/9a30ebd6-6692-48d0-b64b-41b896d6de4a)
# PROGRAM:
library IEEE;

use IEEE.STD_LOGIC_1164.ALL;

use IEEE.STD_LOGIC_ARITH.ALL;

use IEEE.STD_LOGIC_UNSIGNED.ALL;

entity updn is

    Port ( clk : in STD_LOGIC;
    
           clr : in STD_LOGIC;
           
           updown : in std_logic;
           
           count : out std_logic_vector (7 downto 0));

end updn;

architecture Behavioral of updn is

signal tmp : std_logic_vector(7 downto 0);


begin

process

begin

wait until clk'event and clk ='1';

if (clr ='1') then

tmp<="00000000";

elsif (updown ='1') then

tmp <= tmp + 1;

else

tmp <= tmp - 1;


end if;

count <= tmp;

end process;

end Behavioral;
# OUTPUT:
![image](https://github.com/padhmapriya06/8BIT_SYNCHRONOUS_UP-DOWN_COUNTER/assets/160568779/32ee3fef-723e-4376-92a7-5cfa91dfb073)

# RESULT:
Thus the 8 bit synchronous up-down counter has been verified successfully.
