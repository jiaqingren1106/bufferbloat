Instructions:
    run sudo ./run.sh


Fetch Time for queue size 20
    average: 0.5655
    standard deviation: 0.2819
Fetch Time for queue size 100
    average: 1.1705
    standard deviation: 0.6457


1. 
The link between host2 and switch has a smaller bandwidth than link between host1 and switch. When host 1 sends the index html web page to host 2, the packets will always fill the buffer. Therefore whichever has the longer queue size will experience a longer delay. this can be seen from the average and standard deviation from each queue sizes.

2. 
   transmit queue length on the network interface reported by ifconfig: 1000
   MTU: 1500
   bits in queue when full capacity: 1000*1500*8 = 12000000 bit
   time = 12000000 / (100*10^6) = 0.12 s

3. 
for queue size 20, the RTT graph oscilating between 10 to 50 and the queue graph oscilating between 5 to 20. For queue size 100, the RTT graph oscilating between 50 to 250 and the queue graph oscilating between 20 to 100. the ratio is approximately 2.5 for both queue size. the equation is around RTT = 2.5 * queue size, which is linear. 

4. 
 1. use smaller buffers for router and switches to decrease RTT
 2. Increase the bottlenet bandwidth of the link to increase the draining rate of switches/Routers.
