# aducm405x dfp meson file

# internal incdirs and srcsfiles

ad405x_incdirs 	= []
ad405x_srcs		= []

# include files
ad405x_incdirs 	+= include_directories('ARM_CMSIS/Include')
ad405x_incdirs 	+= include_directories('Drivers/Include')
ad405x_incdirs 	+= include_directories('Drivers/Include/config')
ad405x_incdirs 	+= include_directories('Drivers/Include/sys')

# source files

ad405x_srcs		+= ['Drivers/Source/system_ADuCM4050.c']
#ad405x_srcs		+= ['Drivers/Source/common.c']
ad405x_srcs		+= ['Drivers/Source/GCC/startup_ADuCM4050.c']
ad405x_srcs		+= ['Drivers/Source/GCC/reset_ADuCM4050.S']

# driver source files

ad405x_srcs		+= ['Drivers/Source/drivers/pwr/adi_pwr.c']

foreach feature : feature_list
    ad405x_srcs += ['Drivers/Source/drivers/@0@/adi_@0@.c'.format(feature)]
endforeach

#ad405x_srcs		+= ['Drivers/Source/drivers/adc/adi_adc.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/beep/adi_beep.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/crc/adi_crc.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/crypto/adi_crypto.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/dma/adi_dma.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/flash/adi_flash.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/gpio/adi_gpio.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/i2c/adi_i2c.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/pwr/adi_pwr.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/rng/adi_rng.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/rtc/adi_rtc.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/spi/adi_spi.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/sport/adi_sport.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/tmr/adi_tmr.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/uart/adi_uart.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/wdt/adi_wdt.c']
#ad405x_srcs		+= ['Drivers/Source/drivers/xint/adi_xint.c']


srcs    += files(ad405x_srcs)
incdirs += ad405x_incdirs

c_args  += ['-D__ADUCM4050__',
            '-DADI_DEBUG',
            #'-D_RTE_',
            ]
            
mcu_linksct = ['Drivers/Source/GCC/ADuCM4050.ld']


