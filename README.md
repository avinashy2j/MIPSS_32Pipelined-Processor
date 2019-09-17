# MIPSS_32Pipelined-Processor
The implementation of 32-bit MIPS ISA was done using Verliog HDL. This design has 5 stage stage pipelining.
The processor was synthesised on Design Compiler using NanGate 15nm library with following operating condition.
Operating Conditions:
    Operating Condition Name : typical
    Library : NanGate_15nm_OCL
    Process :   1.00
    Temperature :  25.00
    Voltage :   0.80
    Interconnect Model : balanced_tree
    
#Statistics
Initializing gui preferences from file  /remote/.synopsys_dv_prefs.tcl
dc_shell> start_gui
4.1
dc_shell> analyze -library WORK -format verilog {/remote/dc/rtl/mipsTop.v}
Running PRESTO HDLC
Compiling source file /remote/dc/rtl/mipsTop.v
Presto compilation completed successfully.
Loading db file '/remote/dc/models/NanGate_15nm_OCL_typical_conditional_ecsm.db'
dc_shell> elaborate pipe_MIPS32 -architecture verilog -library WORK
Loading db file '/opt/Synopsys/DesignCompiler/O-2018.06-SP5-2/libraries/syn/gtech.db'
Loading db file '/opt/Synopsys/DesignCompiler/O-2018.06-SP5-2/libraries/syn/standard.sldb'
  Loading link library 'NanGate_15nm_OCL'
  Loading link library 'gtech'
Running PRESTO HDLC

Statistics for case statements in always block at line 43 in file
        '/remote/dc/rtl/mipsTop.v'
===============================================
|           Line           |  full/ parallel  |
===============================================
|            56            |    auto/auto     |
===============================================

Statistics for case statements in always block at line 68 in file
        '/remote/dc/rtl/mipsTop.v'
===============================================
|           Line           |  full/ parallel  |
===============================================
|            74            |     no/auto      |
|            76            |    auto/auto     |
|            87            |    auto/auto     |
===============================================

Statistics for case statements in always block at line 108 in file
        '/remote/dc/rtl/mipsTop.v'
===============================================
|           Line           |  full/ parallel  |
===============================================
|           114            |    auto/auto     |
===============================================

Statistics for case statements in always block at line 124 in file
        '/remote/dc/rtl/mipsTop.v'
===============================================
|           Line           |  full/ parallel  |
===============================================
|           127            |     no/auto      |
===============================================

Inferred memory devices in process
        in routine pipe_MIPS32 line 23 in file
                '/remote/dc/rtl/mipsTop.v'.
===============================================================================
|    Register Name    |   Type    | Width | Bus | MB | AR | AS | SR | SS | ST |
===============================================================================
|  BRANCH_TAKEN_reg   | Flip-flop |   1   |  N  | N  | N  | N  | N  | N  | N  |
|    IF_ID_NPC_reg    | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|       PC_reg        | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|    IF_ID_IR_reg     | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
===============================================================================

Inferred memory devices in process
        in routine pipe_MIPS32 line 43 in file
                '/remote/dc/rtl/mipsTop.v'.
===============================================================================
|    Register Name    |   Type    | Width | Bus | MB | AR | AS | SR | SS | ST |
===============================================================================
|    ID_EX_NPC_reg    | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|    ID_EX_Imm_reg    | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|    ID_EX_IR_reg     | Flip-flop |  16   |  Y  | N  | N  | N  | N  | N  | N  |
|     ID_EX_B_reg     | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|     ID_EX_A_reg     | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|   ID_EX_type_reg    | Flip-flop |   3   |  Y  | N  | N  | N  | N  | N  | N  |
===============================================================================

Inferred memory devices in process
        in routine pipe_MIPS32 line 68 in file
                '/remote/dc/rtl/mipsTop.v'.
===============================================================================
|    Register Name    |   Type    | Width | Bus | MB | AR | AS | SR | SS | ST |
===============================================================================
|    EX_MEM_B_reg     | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|  EX_MEM_ALUOut_reg  | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|   EX_MEM_cond_reg   | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|   EX_MEM_type_reg   | Flip-flop |   3   |  Y  | N  | N  | N  | N  | N  | N  |
|    EX_MEM_IR_reg    | Flip-flop |  16   |  Y  | N  | N  | N  | N  | N  | N  |
===============================================================================

Inferred memory devices in process
        in routine pipe_MIPS32 line 108 in file
                '/remote/dc/rtl/mipsTop.v'.
===============================================================================
|    Register Name    |   Type    | Width | Bus | MB | AR | AS | SR | SS | ST |
===============================================================================
|    MEM_WB_IR_reg    | Flip-flop |  10   |  Y  | N  | N  | N  | N  | N  | N  |
|   MEM_WB_LMD_reg    | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
|       Mem_reg       | Flip-flop | 32768 |  Y  | N  | N  | N  | N  | N  | N  |
|   MEM_WB_type_reg   | Flip-flop |   3   |  Y  | N  | N  | N  | N  | N  | N  |
|  MEM_WB_ALUOut_reg  | Flip-flop |  32   |  Y  | N  | N  | N  | N  | N  | N  |
===============================================================================

Inferred memory devices in process
        in routine pipe_MIPS32 line 124 in file
                '/remote/dc/rtl/mipsTop.v'.
===============================================================================
|    Register Name    |   Type    | Width | Bus | MB | AR | AS | SR | SS | ST |
===============================================================================
|     HALTED_reg      | Flip-flop |   1   |  N  | N  | N  | N  | N  | N  | N  |
|       Reg_reg       | Flip-flop | 1024  |  Y  | N  | N  | N  | N  | N  | N  |
===============================================================================
Statistics for MUX_OPs
======================================================
| block name/line  | Inputs | Outputs | # sel inputs |
======================================================
|  pipe_MIPS32/28  |  1024  |   32    |      10      |
|  pipe_MIPS32/35  |  1024  |   32    |      10      |
|  pipe_MIPS32/47  |   32   |   32    |      5       |
|  pipe_MIPS32/50  |   32   |   32    |      5       |
======================================================
Presto compilation completed successfully.
