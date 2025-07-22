# STM32F411 Nucleo SPI DMA Communication



High-speed SPI communication using DMA on STM32F411 Nucleo.

## Features
- **SPI Master Mode** (SPI1)
- **16MHz Clock** (32MHz/2 prescaler)
- **Full-Duplex** DMA transfers
- **10-byte Buffers** (tx_buffer/rx_buffer)
- **Zero CPU Overhead** during transfer

## Hardware Setup
| Signal | Nucleo Pin | Connection |
|--------|------------|------------|
| MOSI   | PA7 (D11)  | → Slave MOSI |
| MISO   | PA6 (D12)  | ← Slave MISO |
| SCK    | PA5 (D13)  | → Slave SCK |
| NSS    | PA4 (D10)  | → Slave CS |

## Technical Details
### SPI/DMA Configuration 
```c
SPI Clock: 16MHz (32MHz/2)
Mode: Master (SPI1), Mode 0
DMA Channels:
  - TX: DMA2 Stream2
  - RX: DMA2 Stream0
Buffer Size: 10 bytes
