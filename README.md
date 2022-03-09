# Swarm-Programming-of-3-Tello-QuadCorpter-Drones

Hi, here is the Drone swarm with tello quadcorpter drones
All tello quadcorpter drones have the IP address (192.168.10.1, 8889), you can change the second tello's address to, say 192.168.10.2 ?
Note: i will be using multiple USB wifi adapters to connect to all the drones i have.

EDIT: It is possible to create a drone swarm using multiple Wifi usb adapters. 

Below is the code i used for swarm programming:

import socket
import time

sock1 = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
sock1.setsockopt(socket.SOL_SOCKET, 25, 'wlx200db00023cd'.encode())

sock2 = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
sock2.setsockopt(socket.SOL_SOCKET, 25, 'wlx3c330008210d'.encode())

sock3 = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
sock3.setsockopt(socket.SOL_SOCKET, 25, 'wlx200db02ef60c'.encode())

sock1.sendto('command'.encode(), 0, ('192.168.10.1', 8889))
sock2.sendto('command'.encode(), 0, ('192.168.10.1', 8889))
sock3.sendto('command'.encode(), 0, ('192.168.10.1', 8889))

sock1.sendto('takeoff'.encode(), 0, ('192.168.10.1', 8889))
sock2.sendto('takeoff'.encode(), 0, ('192.168.10.1', 8889))
sock3.sendto('takeoff'.encode(), 0, ('192.168.10.1', 8889))

import socket
import time

sock1 = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
sock1.setsockopt(socket.SOL_SOCKET, 25, 'wlx200db00023cd'.encode())

sock2 = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
sock2.setsockopt(socket.SOL_SOCKET, 25, 'wlx3c330008210d'.encode())

sock3 = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
sock3.setsockopt(socket.SOL_SOCKET, 25, 'wlx200db02ef60c'.encode())

sock1.sendto('command'.encode(), 0, ('192.168.10.1', 8889))
sock2.sendto('command'.encode(), 0, ('192.168.10.1', 8889))
sock3.sendto('command'.encode(), 0, ('192.168.10.1', 8889))

sock1.sendto('land'.encode(), 0, ('192.168.10.1', 8889))
sock2.sendto('land'.encode(), 0, ('192.168.10.1', 8889))
sock3.sendto('land'.encode(), 0, ('192.168.10.1', 8889))


To run a python file type "python (name of file).py" into the terminal or try "sudo python (name of file).py". Let me know if it works. Im on Ubuntu Linux 16.04.
