# spi_slave
SPI slave for Vaaman 
- All the wires should be of identical lengths. 
- You will need a dummy SPI device in your Linux kernel (e.g., `/dev/spidev1.0`, here 1 is bus and 0 is device).
### Pin assignments:

| Pin    | CPU Pin | FPGA Pin |
|---------|-------------|---------------|
|`sclk`  |7              |H13 - 7    |
|`mosi`|29       |E9 - 29|
|`miso`|31|L15 - 31|
|`cs_n`|33|L18 - 33|

### Potential Reasons for Failure ** :
1. `sclk` is too high. (Checked at 12 MHz, doesn't work for higher frequencies than that, for now).
2. Wire Issue (hardware).

** *If it fails.*
