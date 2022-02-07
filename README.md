# zmk-config

This is my zmk configuration for my corne-like custom keyboard.

## Corne Layout

The following tables map the row and column of each switch to the pin on
the nice!nano. Since the pro micro was made to be arduino compatible,
and the nice!nano's footprint is compatible with the pro micro, the code
uses the arduino pin names as an abstraction.

Key (0, 0) is the top-left key on the laft half. The top-right key on
the right side is (0, 11).

Sources:
- `app/boards/shields/corne/corne.dtsi`
- `app/boards/shields/corne/corne_left.overlay`
- `app/boards/shields/corne/corne_right.overlay`
- `app/boards/arm/nice_nano/arduino_pro_micro_pins.dtsi`

### Rows, Both Halves

| row | arduino | nice!nano |
|-----|---------|-----------|
| 0   | D4      | 022       |
| 1   | D5      | 024       |
| 2   | D6      | 100       |
| 3   | D7      | 011       |

### Columns, Left Half

| column | arduino | nice!nano |
|--------|---------|-----------|
| 0      | A3      | 031       |
| 1      | A2      | 029       |
| 2      | A1      | 020       |
| 3      | A0      | 115       |
| 4      | D15     | 113       |
| 5      | D14     | 111       |

### Columns, Right Half

| column | arduino | nice!nano |
|--------|---------|-----------|
| 6      | D14     | 111       |
| 7      | D15     | 113       |
| 8      | A0      | 115       |
| 9      | A1      | 020       |
| 10     | A2      | 029       |
| 11     | A3      | 031       |

## Formatting The Layers

By adding filler comments with & symbols to match the columns, the
layers can be automatically formatted with tabular.vim with the
following command, either in visual line or normal mode:

```Tabularize / &/l0```


