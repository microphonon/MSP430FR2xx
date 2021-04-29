# Demo code using LPM4 of the MSP430 with I2C
 <p>When the MSP430 is a slave on the I2C bus it can be placed in low-power mode LPM4. Upon receipt of its address from the master, the slave wakes up and data exchange can commence. No example code was found in MSP430Ware, which led to the development of the demo code in this repository. Two MSP430 Launchpads are used, with the FR5969 serving as master and FR2355 as slave. Configurations will vary depending on the family, so the specific users guide should be consulted for correct configuration.
  
  <p><b>Demo 1:</b> Master reads a single byte of data from from a slave (Address 0x77). If the master reads data byte = 0x03, flash green LED.
 Otherwise flash red LED. Corresponding LEDs also toggle on the slave. Slave is held in LPM4 and polled at rate set by the VLO timer on master, which also supplies the I2C clock via SMCLK. There is no clock enabled on slave. For sake of clarity and illustration, no data is sent to slave.
