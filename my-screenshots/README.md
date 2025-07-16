# my-screenshot  
#section1: run 'picorv32a' design synthesis using OpenLane flow  

#Before opening the picorv32a, double click the terminal and run the following:  
bash <(curl -s https://raw.githubusercontent.com/ZimengXiong/bASICs-openlane-apple-silicon-vm/refs/heads/main/patch-1.sh) 
  
#Then go to launcher, run the following:  
./flow.tcl -interactive  
package require openlane 0.9    
prep -design designs/ci/picorv32a  
run_synthesis  

#To see the number of cells and flip-flops, need to run the code inside the log (apprears after runnig run_synthesis)  
designs/ci/picorv32a/runs/RUN_2025.07.16_13.52.56/logs/synthesis/1-synthesis.log  

#Calculate the flop ratio:
Flop Ratio = Number of D flip flops / Total number of cells
