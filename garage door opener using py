import serial
import time

# Establish serial connection with Arduino
ser = serial.Serial('COM3', 9600, timeout=1)
time.sleep(2)  # Allow time for Arduino to initialize

def open_door():
    ser.write(b'o')  # Send command to open the door

def close_door():
    ser.write(b'c')  # Send command to close the door

def check_status():
    ser.write(b's')  # Send command to check the door status
    response = ser.readline().decode().strip()
    print(response)

# Example usage
open_door()
time.sleep(5)  # Simulating door movement
check_status()
time.sleep(5)  # Simulating door movement
close_door()
time.sleep(5)  # Simulating door movement
check_status()

# Close serial connection
ser.close()
