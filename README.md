# Vending-Machine-
`timescale 1ns / 1ps
module vending_machine(
     //Inputs
    input clk,
    input rst,
    input [1:0]in, // 01 = 5 Rs, 10 = 10 Rs
    
    //Outputs
    output reg out,
    output reg[1:0] change);
    
//Variables Declaration
parameter s0 = 2'b00;
parameter s1 = 2'b01;
parameter s2 = 2'b10;

reg[1:0] c_state,n_state;
always@ (posedge clk)
begin
    if(rst == 1)
      begin
        c_state = 0;
        n_state = 0;
        change = 2'b00;
      end
      
    else
    c_state = n_state;
    case(c_state)

        s0: //State 0 : 0 Rs
           if(in == 0)
              begin
                n_state = s0;
                out = 0;
                change = 2'b00;
           end
    
            else if(in == 2'b01)
              begin
                n_state = s1;
                out = 0;
                change = 2'b00;
            end
  
          else if(in == 2'b10)
            begin
              n_state = s2;
              out = 0;
              change = 2'b00;
            end

        #s1: //State 1 : 5 Rs-
            if(in == 0)
              begin
                n_state = s0;
                out = 0;
                change = 2'b01; //Change Returned 5 Rs
              end
    
            else if(in == 2'b01)
              begin
                n_state = s2;
                out = 0;
                change = 2'b00;
              end
    
             else if(in == 2'b10)
                begin
                  n_state = s0;
                  out = 1; // Return Bottle
                  change = 2'b00;
                end
    
        s2: //State 2 : 10 Rs
            if(in == 0)
                begin
                   n_state = s0;
                   out = 0;
                   change = 2'b10;
                end
      
          else if(in == 2'b01)
              begin
                n_state = s0;
                out = 1;
                change = 2'b00;
              end
    
          else if(in == 2'b10)
              begin
                n_state = s0;
                out = 1;
                change = 2'b01; //Change Returned 5 Rs And 1 Bottle
              end
    
      endcase
end
endmodule
