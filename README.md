# tommyjin — Corne ZMK Keymap

Nice!Nano V2 기반 Corne 키보드 ZMK 펌웨어 설정.

## 하드웨어

- **키보드**: Corne (split 42-key)
- **컨트롤러**: Nice!Nano V2 (좌/우)
- **펌웨어**: ZMK

## 레이어 구성

### Layer 0 — Default (Windows)

```
|  -  |  Q  |  W  |  E  |  R  |  T  |   |  Y  |  U  |  I  |  O  |  P  |  -  |
|  -  |  A  |  S  |  D  |  F  |  G  |   |  H  |  J  |  K  |  L  |  ;  |  -  |
|  -  |  Z  |  X  |  C  |  V  |  B  |   |  N  |  M  |  ,  |  .  | SHF |  -  |
                   |CTRL | SPC | L2  |   | L3  | ENT |RALT |
```

### Layer 1 — Mac

콤보(37+40)로 토글. LGUI(Command)와 Ctrl+Space(입력기 전환)가 엄지에 배치됨.

```
|  -  |  Q  |  W  |  E  |  R  |  T  |   |  Y  |  U  |  I  |  O  |  P  |  -  |
|  -  |  A  |  S  |  D  |  F  |  G  |   |  H  |  J  |  K  |  L  |  ;  |  -  |
|  -  |  Z  |  X  |  C  |  V  |  B  |   |  N  |  M  |  ,  |  .  | SHF |  -  |
                   | GUI | SPC | L2  |   | L3  | ENT |C+SP |
```

### Layer 2 — Numbers & Navigation (L2 홀드)

```
|  -  | ESC |  1  |  2  |  3  |  =  |   |  -  | HOM | UP  | END |  -  |  -  |
|  -  |  `  |  4  |  5  |  6  |  -  |   |  -  | LFT | DWN | RGT |  '  |  -  |
|  -  | TAB |  7  |  8  |  9  |  0  |   |  /  |  \  |  [  |  ]  | trn |  -  |
                   | trn | trn | trn |   | trn | trn | trn |
```

### Layer 3 — F-Keys & System (L3 홀드)

```
|  -  | ESC | F1  | F2  | F3  | F12 |   |C+X  |C+C  |C+V  |  -  |  -  |  -  |
|  -  |  `  | F4  | F5  | F6  | F11 |   |  -  |PSCR |  -  |  -  |  -  |  -  |
|  -  | TAB | F7  | F8  | F9  | F10 |   |C+S+Del|C+A+Del| - | -  |  -  |  -  |
                   |  -  |  -  |  -  |   |  -  |  -  |  -  |
```

### Layer 4 — Mouse (콤보 29+37 홀드)

마우스 이동, 스크롤, 버튼, 볼륨 조절.

```
|  -  |  -  | MB4 | M↑  | MB5 |VOL+ |   |PGUP | MB1 | WH↑ | MB2 | MB3 |  -  |
|  -  |  -  | M←  | M↓  | M→  |VOL- |   |PGDN | WH← | WH↓ | WH→ |  -  |  -  |
|  -  |  -  |  -  |  -  |  -  |  -  |   |  -  |  -  |  -  |  -  |  -  |  -  |
                   | trn | trn |  -  |   |  -  |  -  |  -  |
```

- 이동 속도: 2500 / 스크롤 속도: 20

### Layer 5 — Bluetooth (콤보 30+40 홀드)

```
|  -  |  -  |  -  |  -  |  -  |  -  |   | BT0 | BT1 | BT2 | BT3 |CLRA |  -  |
|  -  |  -  |  -  |  -  |  -  |  -  |   |  -  |  -  |  -  | BLE | USB |  -  |
|  -  |  -  |  -  |  -  |  -  |  -  |   |  -  |  -  |  -  |  -  |  -  |  -  |
                   |  -  |  -  |  -  |   |  -  |  -  |  -  |
```

## 콤보

| 콤보 키 위치 | 출력 | 설명 |
|---|---|---|
| 37 + 38 | Left Alt | Alt |
| 37 + 40 | Toggle Layer 1 | Mac 모드 토글 |
| 29 + 37 | Mo Layer 4 | 마우스 레이어 |
| 9 + 10 | Backspace | 백스페이스 |
| 8 + 9 | Delete | 딜리트 |
| 25 + 26 + 27 | Win + Tab | 창 전환 |
| 26 + 27 + 28 | LWIN | 윈도우 키 |
| 27 + 28 + 29 | Ctrl + Alt | |
| 30 + 40 | Mo Layer 5 | 블루투스 레이어 |

## 펌웨어 설정

- 아이들 타임아웃: 30초
- 슬립 타임아웃: 15분
- BLE 실험적 연결 모드: 활성화
- 포인팅(마우스) 기능: 활성화

## 빌드

GitHub Actions로 자동 빌드. 푸시 시 좌/우 펌웨어 및 `settings_reset` 파일이 생성됨.

- `corne_left-nice_nano_v2-zmk.uf2`
- `corne_right-nice_nano_v2-zmk.uf2`
- `settings_reset-nice_nano_v2-zmk.uf2`
