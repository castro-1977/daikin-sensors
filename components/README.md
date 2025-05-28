# daikin-sensors

Componentes personalizados ESPHome para sensores:

- **cm1106**: Sensor de CO₂ via UART
- **pm2105**: Sensor de partículas (PM2.5) via I²C

## Estrutura esperada

```
components/
├── cm1106/
│   ├── __init__.py
│   ├── component.py
│   ├── sensor.cpp
│   ├── sensor.h
│   └── cm1106_device.h
├── pm2105/
│   ├── __init__.py
│   ├── component.py
│   ├── sensor.cpp
│   ├── sensor.h
│   └── pm2105_device.h
```

## Uso com ESPHome

```yaml
external_components:
  - source:
      type: git
      url: https://github.com/castro-1977/daikin-sensors
    components: [cm1106, pm2105]
```

Certifique-se de que os sensores estejam conectados corretamente à placa ESP32 e que o firmware use as definições de `uart` e `i2c` adequadas.
