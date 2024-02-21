# CloudRIC
Here we provide the datasets characterizing the latency and power consumption figures to decode LDPC-encoded transport blocks.

- CPU_dataset.csv is the dataset for experiments run using Intel FlexRAN 19.04 LDPC library on an Intel Xeon Gold 6240R CPU core @ 2.40GHz <br>
  "nPRB": Number of allocated Physical Resource Blocks
  "SNR_dB": SNR in dB measured at transmitting user
  "MCS": MCS used for uplink transmission
  "Base_Graph": Base Graph type used for LDPC decoding (either 1 or 2)
  "TBS": Information bits of the Transport Block
  "Codeblock_Length": Length in bits of the codeblock(s) composing the Transport Block
  "Number_Codeblocks": Number of codeblocks composing the Transport Block
  "Total_Bits": Total number of bits of the LDPC-encoded Transport Block
  "Bit_Error_Count": Number of bits in error after a maximum of 10 LDPC Decoding iterations
  "Simulation_Index": Index of the generated LDPC-encoded Transport Block
  "Run_Index": Index of the experiment to decode the LDPC-encoded Transport Block
  "Decoding_Throughput_Gbps": Measured decoding throughput in Gbps (total bits / decoding time)
  "Decoding_Time_us": Measured decoding time in us
  "Decoding_Iterations": Number of decoding iterations needed to decode the Transport Block
  "Decoding_Power_W": Measured decoding power in W with PowerTOP v2.11
  "Decoding_Energy_uJ": Measured decoding energy in uJ (decoding time * decoding power)
  "PHY_latency_us": Measured AAL-Broker-UserPlane latency needed to route LDCP-encoded Transport Block data to an LPU queue
  "Total_latency_us": Measured total latency of an LDPC-encoded Transport Block ("Decoding_Time_us" + "PHY_latency_us")



- GPU_dataset.csv is the dataset for experiments run using cuBB SDK Alpha-3 library on an NVIDIA V100 GPU
  "nPRB": Number of allocated Physical Resource Blocks
  "SNR_dB": SNR in dB measured at transmitting user
  "MCS": MCS used for uplink transmission
  "Base_Graph": Base Graph type used for LDPC decoding (either 1 or 2)
  "TBS": Information bits of the Transport Block
  "Codeblock_Length": Length in bits of the codeblock(s) composing the Transport Block
  "Number_Codeblocks": Number of codeblocks composing the Transport Block
  "Total_Bits": Total number of bits of the LDPC-encoded Transport Block
  "Bit_Error_Count": Number of bits in error after a maximum of 10 LDPC Decoding iterations
  "Simulation_Index": Index of the generated LDPC-encoded Transport Block
  "Run_Index": Index of the experiment to decode the LDPC-encoded Transport Block
  "Decoding_Throughput_Gbps": Measured decoding throughput in Gbps (total bits / decoding time)
  "Decoding_Time_us": Measured decoding time in us
  "Decoding_Iterations": Number of decoding iterations needed to decode the Transport Block
  "Decoding_Power_W": Measured decoding power in W from Power Readings (Power Draw) of nvidia-smi command
  "Decoding_Energy_uJ": Measured decoding energy in uJ (decoding time * decoding power)
  "PHY_latency_us": Measured AAL-Broker-UserPlane latency needed to route LDCP-encoded Transport Block data to an LPU queue
  "Total_latency_us": Measured total latency of an LDPC-encoded Transport Block ("Decoding_Time_us" + "PHY_latency_us")


