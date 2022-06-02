# Exercise-07-Multiplexer-and-De-multiplexer
### AIM: To implement 4 X1 multiplexer and 1X4 de multiplexer using verilog and validate its outputs
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## What are Multiplexer and Demultiplexer?
In-network transmission, both the multiplexer and demultiplexer are combinational circuits. A multiplexer selects an input from several inputs then it is transmitted in the form of a single line. An alternative name of the multiplexer is MUX or data selector. A demultiplexer uses one input signal and generates many. So it is known as Demux or data distributor.

## What is a Multiplexer?
The multiplexer is a device that has multiple inputs and single line output. The select lines determine which input is connected to the output, and also increase the amount of data that can be sent over a network within a certain time. It is also called a data selector.

The single-pole multi-position switch is a simple example of a non-electronic circuit of the multiplexer, and it is widely used in many electronic circuits. The multiplexer is used to perform high-speed switching and is constructed by electronic components.

![image](https://user-images.githubusercontent.com/36288975/170912485-73c395c7-23c0-4e78-a53d-a2f0d07d9662.png)
          Figure-01 multiplexer block diagram 

Multiplexers are capable of handling both analog and digital applications. In analog applications, multiplexers are made up of relays and transistor switches, whereas in digital applications, the multiplexers are built from standard logic gates. When the multiplexer is used for digital applications, it is called a digital multiplexer.

4-to-1 Multiplexer
The 4X1 multiplexer comprises 4-input bits, 1- output bit, and 2- control bits. The four input bits are namely 0, D1, D2, and D3, respectively; only one of the input bits is transmitted to the output. The o/p ‘q’ depends on the value of control input AB. The control bit AB decides which of the i/p data bit should transmit the output. The following figure shows the 4X1 multiplexer circuit diagram using AND gates. For example, when the control bits AB =00, then the higher AND gates are allowed while remaining AND gates are restricted. Thus, data input D0 is transmitted to the output ‘q”
![image](https://user-images.githubusercontent.com/36288975/170912568-3598c60a-5035-41f3-b0c4-ccedba13aca5.png)


Figure2 4X1 multiplexer 
If the control input is changed to 11, then all gates are restricted except the bottom AND gate. In this case, D3 is transmitted to the output, and q=D0. If the control input is changed to AB =11, all gates are disabled except the bottom AND gate. In this case, D3 is transmitted to the output, and q = D3. The best example of a 4X1 multiplexer is IC 74153. In this IC, the o/p is the same as the i/p. Another example of a 4X1 multiplexer is IC 45352. In this IC, the o/p is the compliment of the i/p


## What is Demultiplexer?
De-multiplexer is also a device with one input and multiple output lines. It is used to send a signal to one of the many devices. The main difference between a multiplexer and a de-multiplexer is that a multiplexer takes two or more signals and encodes them on a wire, whereas a de-multiplexer does reverse to what the multiplexer does.
![image](https://user-images.githubusercontent.com/36288975/170912606-a30e4b74-1726-4430-b245-2c3c3d9c232d.png)
Figure 3 De-multiplexer 
1-4 Demultiplexer
The 1-to-4 demultiplexer comprises 1- input bit, 4-output bits, and control bits. The 1X4 demultiplexer circuit diagram is shown below.![image](https://user-images.githubusercontent.com/36288975/170912683-00fb746a-1d45-4023-91d1-3a70b841073c.png)

![image](https://user-images.githubusercontent.com/36288975/170912741-7cbd52af-7e0d-4be3-b5c6-6fb9c4eca7c9.png)

Figure4 1X4 De-multiplexer 
The i/p bit is considered as Data D. This data bit is transmitted to the data bit of the o/p lines, which depends on the AB value and the control i/p.

When the control i/p AB = 01, the upper second AND gate is permitted while the remaining AND gates are restricted. Thus, only data bit D is transmitted to the output, and Y1 = Data.

If the data bit D is low, the output Y1 is low. IF data bit D is high, the output Y1 is high. The value of the output Y1 depends upon the value of data bit D, the remaining outputs are in a low state.

If the control input changes to AB = 10, then all the gates are restricted except the third AND gate from the top. Then, data bit D is transmitted only to the output Y2; and, Y2 = Data. . The best example of 1X4 demultiplexer is IC 74155.

 
 
### Procedure
/* write all the steps invloved */



### PROGRAM
~~~
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: u.srinivas 
RegisterNumber:  212221230108

module mux4(s1,s2,io,it,ir,iu,y);
input s1,s2,io,it,ir,iu;
output y;
wire a,b,c,d,e,f;
assign e=~s1;
assign f=~s2;
assign a=io&e&f;
assign b=it&e&s2;
assign c=ir&s1&f;
assign d=iu&s1&s2;
assign y=a|b|c|d;
endmodule
*/
~~~






### RTL LOGIC  



![171138341-1eeefc99-8d0b-483f-9e3e-2e725e17e7c1](https://user-images.githubusercontent.com/93427183/171542301-64a603dd-9cc9-4723-8aaa-022810bccd07.png)





### TIMING DIGRAMS  


![171138383-40edc81e-4e26-49ac-94f2-7e099213e489](https://user-images.githubusercontent.com/93427183/171542315-0e67d1be-e494-4eae-92a9-f3980e70847a.png)


![171138416-8f1c4f99-d66f-428a-92d4-a467fac010a7](https://user-images.githubusercontent.com/93427183/171542327-1d4fcaf1-3c7f-4a50-9f3a-b9c29ce91642.png)

![171138453-bcfd031c-77cb-4ea3-9733-9f94a7120528](https://user-images.githubusercontent.com/93427183/171542337-d047a413-d463-49d9-8923-82a2c1c721b5.png)

![171138482-3dac8c6b-0378-43f3-9e08-401ddf81888b](https://user-images.githubusercontent.com/93427183/171542346-c6e6bc31-01a9-4df0-8218-1b6b58ffb281.png)

### TRUTH TABLE 
![171184283-34e5304c-d2b1-4b68-aaa1-7cb4b8591524](https://user-images.githubusercontent.com/93427183/171542371-51254167-29c2-4a1c-8bfc-a3a472f1690b.jpg)

### program:
~~~
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: u.srinivas
RegisterNumber:  212221230108

PROGRAM:
module dm(s1,s2,i1,i2,i3,i4,y);
input s1,s2,i1,i2,i3,i4;
output y;
wire a,b,c,d,e,f;
assign e=~s1;
assign f=~s2;
assign a=i1&e&f;
assign b=i2&e&s2;
assign c=i3&s1&f;
assign d=i4&s1&s2;
assign y=a|b|c|d;
endmodule
~~~
### RTL : 
![171138991-5e761b81-aa56-4221-9d89-908a12220396](https://user-images.githubusercontent.com/93427183/171543246-b238bbb4-bc8c-401b-9633-570073d92ba3.png)
LOGIC  :
### TIMING DIGRAMS  
![171184556-6e3d5e2c-0b8d-4b23-a5dc-071238e3f9a8](https://user-images.githubusercontent.com/93427183/171543463-5ab3c199-8387-45d3-b35e-45742c1f6cf7.png)
### TRUTH TABLE 
![171184657-372c166d-d88f-4e70-8644-cb47d5092f01](https://user-images.githubusercontent.com/93427183/171543518-1b422dee-10a6-4dcb-b6f9-5679a133a882.png)


### RESULTS 
Thus 4x1 Multiplexer and 1x4 Demultiplexer is been implemented and verified using verilog programming and its output are validated.
