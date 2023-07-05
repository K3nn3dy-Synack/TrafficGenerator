Traffic Generator - Usage Guide
The Traffic Generator is a command-line tool that allows you to generate traffic to perform fault finding, connectivity testing, and measure network performance. It supports two modes of operation: sending network packets or making web (curl) requests.

Prerequisites
Before using the Traffic Generator, ensure that you have the following:

Python 3 installed on your system.
The required Python packages installed. You can install them by running the following command:
Copy code
pip install netifaces requests scapy tqdm
Running the Traffic Generator
To run the Traffic Generator, follow these steps:

Open a terminal or command prompt.

Navigate to the directory where you have saved the trafficgenerator.py file.

Run the following command:

csharp
Copy code
python trafficgenerator.py <destination_ip> [--interface <interface_name>] [--port <destination_port>] [--count <packet_count>] [--web]
Replace <destination_ip> with the IP address of the destination you want to send traffic to.

Optional arguments:

--interface <interface_name>: Specify the network interface name to use for sending traffic. If not provided, the default interface will be used.
--port <destination_port>: Specify the destination port. The default is port 80.
--count <packet_count>: Specify the number of packets or requests to send. The default is 10.
--web: Use this flag to enable web requests instead of network packets.
Examples
Here are some examples of how to use the Traffic Generator:

Send network packets:

Copy code
python trafficgenerator.py 192.168.1.100
Send web requests:

css
Copy code
python trafficgenerator.py 192.168.1.100 --web
Specify a custom port and packet count:

css
Copy code
python trafficgenerator.py 192.168.1.100 --port 8080 --count 20
Specify a network interface:

kotlin
Copy code
python trafficgenerator.py 192.168.1.100 --interface eth0
Output
The Traffic Generator provides detailed output during the traffic generation process:

For network packets: It displays the timestamp when each packet is sent.

For web requests: It shows the response status code for each request. If the response is 200 (OK), it will be displayed in green; otherwise, it will be displayed in red.

At the end of the execution, the Traffic Generator summarizes the total number of packets sent or requests made.

Conclusion
The Traffic Generator tool is a versatile and efficient way to generate traffic for fault finding, connectivity testing, and network performance measurement. By following the usage guide, you can easily configure and run the Traffic Generator to meet your testing needs.
