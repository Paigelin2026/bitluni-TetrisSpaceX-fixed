# bitluni-TetrisSpaceX-fixed
Issue: get the data from Serial,I2S driver stack overflow.

DMA buffer is too large

Task stack too small

Fix: Resolved MCU reboot loop after firmware upload

-Switched from "i2s_write_bytes()" to "i2s_write()" with timeout 20ms

-Set "dma_buf_len = 256",increased dma_buf_count from 2 to 4

-Raised Core stack to 65536 bytes

Requiremeents:

1.Arduino IDE 1.8.13 or above

2.MCU ESP-WROOM-32-D/E With 4MB Flash,520kb RAM

3.Set the PSRAM is disabled

1.download the file "CompositeOutput.h" and "TetrisSpaceX.ino"

2.Replace these files in the original project.

3.Upload or press Ctrl + U
