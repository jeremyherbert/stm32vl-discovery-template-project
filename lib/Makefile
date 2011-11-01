vpath %c $(DEVICE) $(CORE) $(PERIPH)/src $(UTIL)
CFLAGS+= -I. -I$(DEVICE) -I$(CORE) -I$(PERIPH)/inc -I$(UTIL) 

SRCS = STM32vldiscovery.c
SRCS+= system_stm32f10x.c
SRCS+= core_cm3.c
SRCS+=  stm32f10x_dbgmcu.c	stm32f10x_pwr.c \
        misc.c			stm32f10x_dma.c		stm32f10x_rcc.c \
	stm32f10x_adc.c		stm32f10x_exti.c	stm32f10x_rtc.c \
	stm32f10x_bkp.c		stm32f10x_flash.c	stm32f10x_sdio.c \
	stm32f10x_can.c		stm32f10x_fsmc.c	stm32f10x_spi.c \
	stm32f10x_cec.c		stm32f10x_gpio.c	stm32f10x_tim.c \
	stm32f10x_crc.c		stm32f10x_i2c.c		stm32f10x_usart.c \
	stm32f10x_dac.c		stm32f10x_iwdg.c	stm32f10x_wwdg.c

OBJS= $(SRCS:.c=.o)

all: libst32.a

libst32.a: $(OBJS)
	$(AR) rcs $@ $(OBJS)

clean:
	rm -f $(OBJS) libst32.a