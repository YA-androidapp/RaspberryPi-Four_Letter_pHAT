# RaspberryPi-Four_Letter_pHAT

```sh
$ curl https://get.pimoroni.com/fourletterphat  | bash
```

```py
import time
import fourletterphat as flp

while True:
    flp.clear()
    str_time = time.strftime("%H%M")
    flp.print_number_str(str_time)
    if int(time.time()) % 2 == 0:
        flp.set_decimal(1, 1)
    else:
        flp.set_decimal(1, 0)

    # flp.set_digit(0, 'A')
    # flp.set_digit(3, 'D')
    # flp.print_str('ABCD')
    # flp.print_str('BCD', justify_right=True)

    # flp.set_decimal(0, True)
    # flp.set_decimal(3, True)
    # flp.print_number_str('-1.23')
    # flp.print_float(-1.2)
    # flp.print_float(-1.2, justify_right=False)

    flp.show()
    time.sleep(0.1)
```
