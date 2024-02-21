# CloudRIC

CloudRIC is a system that meets specific reliability targets in 5G FEC processing while sharing pools of heterogeneous processors among DUs, which leads to more cost- and energy-efficient vRANs. The details of the solution are presented in XXX. 
These repository provides a dataset, analyzed therein, with experiments carried out with different 5G LDPC decoding processors: (i) Intel FlexRAN library and two open-source alternative libraries on an Intel Xeon Gold 6240R CPU, and (ii) a proprietary driver on an NVIDIA GPU V100. 

# Dataset
Here we provide the datasets characterizing the latency and power consumption figures to decode LDPC-encoded transport blocks.

- CPU_dataset.csv is the dataset for experiments run using Intel FlexRAN 19.04 LDPC library on an Intel Xeon Gold 6240R CPU core @ 2.40GHz <br>
  "nPRB": Number of allocated Physical Resource Blocks<br>
  "SNR_dB": SNR in dB measured at transmitting user<br>
  "MCS": MCS used for uplink transmission<br>
  "Base_Graph": Base Graph type used for LDPC decoding (either 1 or 2)<br>
  "TBS": Information bits of the Transport Block<br>
  "Codeblock_Length": Length in bits of the codeblock(s) composing the Transport Block<br>
  "Number_Codeblocks": Number of codeblocks composing the Transport Block<br>
  "Total_Bits": Total number of bits of the LDPC-encoded Transport Block<br>
  "Bit_Error_Count": Number of bits in error after a maximum of 10 LDPC Decoding iterations<br>
  "Simulation_Index": Index of the generated LDPC-encoded Transport Block<br>
  "Run_Index": Index of the experiment to decode the LDPC-encoded Transport Block<br>
  "Decoding_Throughput_Gbps": Measured decoding throughput in Gbps (total bits / decoding time)<br>
  "Decoding_Time_us": Measured decoding time in us<br>
  "Decoding_Iterations": Number of decoding iterations needed to decode the Transport Block<br>
  "Decoding_Power_W": Measured decoding power in W with PowerTOP v2.11<br>
  "Decoding_Energy_uJ": Measured decoding energy in uJ (decoding time * decoding power)<br>
  "PHY_latency_us": Measured AAL-Broker-UserPlane latency needed to route LDCP-encoded Transport Block data to an LPU queue<br>
  "Total_latency_us": Measured total latency of an LDPC-encoded Transport Block ("Decoding_Time_us" + "PHY_latency_us")<br>

<br>

- GPU_dataset.csv is the dataset for experiments using a propietary LDPC decoder on an NVIDIA V100 GPU<br>
  "nPRB": Number of allocated Physical Resource Blocks<br>
  "SNR_dB": SNR in dB measured at transmitting user<br>
  "MCS": MCS used for uplink transmission<br>
  "Base_Graph": Base Graph type used for LDPC decoding (either 1 or 2)<br>
  "TBS": Information bits of the Transport Block<br>
  "Codeblock_Length": Length in bits of the codeblock(s) composing the Transport Block<br>
  "Number_Codeblocks": Number of codeblocks composing the Transport Block<br>
  "Total_Bits": Total number of bits of the LDPC-encoded Transport Block<br>
  "Bit_Error_Count": Number of bits in error after a maximum of 10 LDPC Decoding iterations<br>
  "Simulation_Index": Index of the generated LDPC-encoded Transport Block<br>
  "Run_Index": Index of the experiment to decode the LDPC-encoded Transport Block<br>
  "Decoding_Throughput_Gbps": Measured decoding throughput in Gbps (total bits / decoding time)<br>
  "Decoding_Time_us": Measured decoding time in us<br>
  "Decoding_Iterations": Number of decoding iterations needed to decode the Transport Block<br>
  "Decoding_Power_W": Measured decoding power in W from Power Readings (Power Draw) of nvidia-smi command<br>
  "Decoding_Energy_uJ": Measured decoding energy in uJ (decoding time * decoding power)<br>
  "PHY_latency_us": Measured AAL-Broker-UserPlane latency needed to route LDCP-encoded Transport Block data to an LPU queue<br>
  "Total_latency_us": Measured total latency of an LDPC-encoded Transport Block ("Decoding_Time_us" + "PHY_latency_us")<br>


