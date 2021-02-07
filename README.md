# UGM3.1
I2C
 install utility  
  `sudo apt-get install -y i2c-tools`
 
 I2C Address Scan
 
  `i2cdetect -y 1`

## Setting up RTC

 comment following lines from here   `/lib/udev/hwclock-set`
 
 ` if [ -e /run/systemd/system ] ; then   `
    `exit 0`
  `  fi`
  
  Before the next step, one should make sure, one's system time is accurate (e.g. by comparing it to a radio controlled clock nearby).
  Now, one sends one's current system time to the RTC using the command

  `sudo hwclock -w`
  
  From now on, the RTC will keep the time and resynchronize the RPi's system time automatically on startup or manually by entering

  `sudo hwclock -r` 
  
  
 # TEST ADC 4 Channel MCP3428

## Device address is 0x6E

Run the  command 

`python3  MCP3428_a.py`

