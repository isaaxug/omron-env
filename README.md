# 2jcieev01-raspi-demo

## できること

絶対圧センサーのデモ

## install

```bash
sh build.sh
```

## demo

### library demo

```bash
$ sh baro.sh
  100059.7,  32.320, a462ee, 66b246, retun code: 0
  100060.1,  32.320, a4630b, 66b2d4, retun code: 0
  100059.9,  32.320, a462f2, 66b231, retun code: 0
  100060.6,  32.310, a4633c, 66b3f9, retun code: 0
  100057.9,  32.340, a46246, 66ae7d, retun code: 0
  100056.2,  32.340, a46220, 66aee4, retun code: 0
```

* 気圧(Pa)
* 気温(degC)
* RAW Pressure
* RAW Temperature
* return code

### ambient demo

#### install

```bash
pip3 install git+https://github.com/AmbientDataInc/ambient-python-lib.git
```

#### run

Create a new channel.
<https://ambidata.io/ch/channels.html>

```bash
AMBIENT_CHANNEL_ID=00000 AMBIENT_WRITE_KEY=aaaaaaaa python3 demo.py
```

### ambient demo with isaax

#### install

```
sudo pip3 install git+https://github.com/AmbientDataInc/ambient-python-lib.git
```

#### clustor settings

post-update

```bash
#!/bin/sh
sh build.sh
```

ユーザー変数

|名|変数タイプ|値|
|---|---|---|
|`AMBIENT_CHANNEL_ID`|数値||
|`AMBIENT_WRITE_KEY`|文字列||
