# CSDC5 Firmware Packages

In order to prevent cluttering of the main repository, all third-party
software that's used on the satellite goes into this repo, which is
used as a submodule in the firmware repo.

# Directory

Currently, the following libraries are present:

## CMSIS

CMSIS defines the registers for all the core peripherals, as well as
all of ST's peripherals, but it provides no drivers for use with them.

```
cmsis/
├── cmsis_compiler.h
├── cmsis_gcc.h
├── core_cm7.h
├── stm32h743xx.h
├── stm32h7xx.h
└── system_stm32h7xx.h
```

## STM32 HAL

The default drivers for use with the STM32H7 series, written by ST.
In some cases, they will have to be modified for use with a
multitasking OS.

```
hal
├── Inc
│   ├── Legacy
│   │   └── stm32_hal_legacy.h
│   ├── stm32h7xx_hal_adc_ex.h
│   ├── stm32h7xx_hal_adc.h
│   ├── stm32h7xx_hal_cec.h
│   ├── stm32h7xx_hal_comp.h
│   ├── stm32h7xx_hal_conf_template.h
│   ├── stm32h7xx_hal_cortex.h
│   ├── stm32h7xx_hal_crc_ex.h
│   ├── stm32h7xx_hal_crc.h
│   ├── stm32h7xx_hal_cryp_ex.h
│   ├── stm32h7xx_hal_cryp.h
│   ├── stm32h7xx_hal_dac_ex.h
│   ├── stm32h7xx_hal_dac.h
│   ├── stm32h7xx_hal_dcmi.h
│   ├── stm32h7xx_hal_def.h
│   ├── stm32h7xx_hal_dfsdm.h
│   ├── stm32h7xx_hal_dma2d.h
│   ├── stm32h7xx_hal_dma_ex.h
│   ├── stm32h7xx_hal_dma.h
│   ├── stm32h7xx_hal_eth_ex.h
│   ├── stm32h7xx_hal_eth.h
│   ├── stm32h7xx_hal_fdcan.h
│   ├── stm32h7xx_hal_flash_ex.h
│   ├── stm32h7xx_hal_flash.h
│   ├── stm32h7xx_hal_gpio_ex.h
│   ├── stm32h7xx_hal_gpio.h
│   ├── stm32h7xx_hal.h
│   ├── stm32h7xx_hal_hash_ex.h
│   ├── stm32h7xx_hal_hash.h
│   ├── stm32h7xx_hal_hcd.h
│   ├── stm32h7xx_hal_hrtim.h
│   ├── stm32h7xx_hal_hsem.h
│   ├── stm32h7xx_hal_i2c_ex.h
│   ├── stm32h7xx_hal_i2c.h
│   ├── stm32h7xx_hal_i2s_ex.h
│   ├── stm32h7xx_hal_i2s.h
│   ├── stm32h7xx_hal_irda_ex.h
│   ├── stm32h7xx_hal_irda.h
│   ├── stm32h7xx_hal_iwdg.h
│   ├── stm32h7xx_hal_jpeg.h
│   ├── stm32h7xx_hal_lptim.h
│   ├── stm32h7xx_hal_ltdc.h
│   ├── stm32h7xx_hal_mdios.h
│   ├── stm32h7xx_hal_mdma.h
│   ├── stm32h7xx_hal_mmc_ex.h
│   ├── stm32h7xx_hal_mmc.h
│   ├── stm32h7xx_hal_nand.h
│   ├── stm32h7xx_hal_nor.h
│   ├── stm32h7xx_hal_opamp_ex.h
│   ├── stm32h7xx_hal_opamp.h
│   ├── stm32h7xx_hal_pcd_ex.h
│   ├── stm32h7xx_hal_pcd.h
│   ├── stm32h7xx_hal_pwr_ex.h
│   ├── stm32h7xx_hal_pwr.h
│   ├── stm32h7xx_hal_qspi.h
│   ├── stm32h7xx_hal_rcc_ex.h
│   ├── stm32h7xx_hal_rcc.h
│   ├── stm32h7xx_hal_rng.h
│   ├── stm32h7xx_hal_rtc_ex.h
│   ├── stm32h7xx_hal_rtc.h
│   ├── stm32h7xx_hal_sai_ex.h
│   ├── stm32h7xx_hal_sai.h
│   ├── stm32h7xx_hal_sd_ex.h
│   ├── stm32h7xx_hal_sd.h
│   ├── stm32h7xx_hal_sdram.h
│   ├── stm32h7xx_hal_smartcard_ex.h
│   ├── stm32h7xx_hal_smartcard.h
│   ├── stm32h7xx_hal_smbus.h
│   ├── stm32h7xx_hal_spdifrx.h
│   ├── stm32h7xx_hal_spi_ex.h
│   ├── stm32h7xx_hal_spi.h
│   ├── stm32h7xx_hal_sram.h
│   ├── stm32h7xx_hal_swpmi.h
│   ├── stm32h7xx_hal_tim_ex.h
│   ├── stm32h7xx_hal_tim.h
│   ├── stm32h7xx_hal_uart_ex.h
│   ├── stm32h7xx_hal_uart.h
│   ├── stm32h7xx_hal_usart_ex.h
│   ├── stm32h7xx_hal_usart.h
│   ├── stm32h7xx_hal_wwdg.h
│   ├── stm32h7xx_ll_delayblock.h
│   ├── stm32h7xx_ll_fmc.h
│   ├── stm32h7xx_ll_sdmmc.h
│   └── stm32h7xx_ll_usb.h
└── Src
    ├── stm32h7xx_hal_adc.c
    ├── stm32h7xx_hal_adc_ex.c
    ├── stm32h7xx_hal.c
    ├── stm32h7xx_hal_cec.c
    ├── stm32h7xx_hal_comp.c
    ├── stm32h7xx_hal_cortex.c
    ├── stm32h7xx_hal_crc.c
    ├── stm32h7xx_hal_crc_ex.c
    ├── stm32h7xx_hal_cryp.c
    ├── stm32h7xx_hal_cryp_ex.c
    ├── stm32h7xx_hal_dac.c
    ├── stm32h7xx_hal_dac_ex.c
    ├── stm32h7xx_hal_dcmi.c
    ├── stm32h7xx_hal_dfsdm.c
    ├── stm32h7xx_hal_dma2d.c
    ├── stm32h7xx_hal_dma.c
    ├── stm32h7xx_hal_dma_ex.c
    ├── stm32h7xx_hal_eth.c
    ├── stm32h7xx_hal_eth_ex.c
    ├── stm32h7xx_hal_fdcan.c
    ├── stm32h7xx_hal_flash.c
    ├── stm32h7xx_hal_flash_ex.c
    ├── stm32h7xx_hal_gpio.c
    ├── stm32h7xx_hal_hash.c
    ├── stm32h7xx_hal_hash_ex.c
    ├── stm32h7xx_hal_hcd.c
    ├── stm32h7xx_hal_hrtim.c
    ├── stm32h7xx_hal_hsem.c
    ├── stm32h7xx_hal_i2c.c
    ├── stm32h7xx_hal_i2c_ex.c
    ├── stm32h7xx_hal_i2s.c
    ├── stm32h7xx_hal_i2s_ex.c
    ├── stm32h7xx_hal_irda.c
    ├── stm32h7xx_hal_iwdg.c
    ├── stm32h7xx_hal_jpeg.c
    ├── stm32h7xx_hal_lptim.c
    ├── stm32h7xx_hal_ltdc.c
    ├── stm32h7xx_hal_mdios.c
    ├── stm32h7xx_hal_mdma.c
    ├── stm32h7xx_hal_mmc.c
    ├── stm32h7xx_hal_mmc_ex.c
    ├── stm32h7xx_hal_nand.c
    ├── stm32h7xx_hal_nor.c
    ├── stm32h7xx_hal_opamp.c
    ├── stm32h7xx_hal_opamp_ex.c
    ├── stm32h7xx_hal_pcd.c
    ├── stm32h7xx_hal_pcd_ex.c
    ├── stm32h7xx_hal_pwr.c
    ├── stm32h7xx_hal_pwr_ex.c
    ├── stm32h7xx_hal_qspi.c
    ├── stm32h7xx_hal_rcc.c
    ├── stm32h7xx_hal_rcc_ex.c
    ├── stm32h7xx_hal_rng.c
    ├── stm32h7xx_hal_rtc.c
    ├── stm32h7xx_hal_rtc_ex.c
    ├── stm32h7xx_hal_sai.c
    ├── stm32h7xx_hal_sai_ex.c
    ├── stm32h7xx_hal_sd.c
    ├── stm32h7xx_hal_sd_ex.c
    ├── stm32h7xx_hal_sdram.c
    ├── stm32h7xx_hal_smartcard.c
    ├── stm32h7xx_hal_smartcard_ex.c
    ├── stm32h7xx_hal_smbus.c
    ├── stm32h7xx_hal_spdifrx.c
    ├── stm32h7xx_hal_spi.c
    ├── stm32h7xx_hal_spi_ex.c
    ├── stm32h7xx_hal_sram.c
    ├── stm32h7xx_hal_swpmi.c
    ├── stm32h7xx_hal_tim.c
    ├── stm32h7xx_hal_tim_ex.c
    ├── stm32h7xx_hal_uart.c
    ├── stm32h7xx_hal_uart_ex.c
    ├── stm32h7xx_hal_usart.c
    ├── stm32h7xx_hal_wwdg.c
    ├── stm32h7xx_ll_delayblock.c
    ├── stm32h7xx_ll_fmc.c
    ├── stm32h7xx_ll_sdmmc.c
    └── stm32h7xx_ll_usb.c
```
