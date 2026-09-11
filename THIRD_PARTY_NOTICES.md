# Third-Party Notices

SBCT 빌드에 포함되거나 참조되는 제3자 구성요소와 라이선스.

| Component | Version | License | Use |
|---|---|---|---|
| Python | 3.13 | PSF License | 런타임 |
| NumPy | 2.x | BSD-3-Clause | DSP |
| SciPy | 1.14+ | BSD-3-Clause | DSP, WAV 입출력 |
| PySide6 (Qt for Python) | 6.11+ | LGPL-3.0 | UI |
| sounddevice / PortAudio | 0.5.x | MIT | 스피커 출력·장치 열거 |
| PyInstaller | 6.22 | GPL-2.0 with bootloader exception | 패키징(런타임 포함 안 됨) |

## 참조만 하는 구성요소 (동봉하지 않음)

- **AndroidMic** (teamclouday/AndroidMic, GPL-3.0): 폰 앱은 사용자가 공식 릴리스에서 직접 설치한다. `sbct/androidmic.py`는 공개 프로토콜에 맞춘 독립 구현이며 upstream 코드를 복사하지 않았다. 검토한 커밋: `925b110a82e1c01e1d4fe0ca5e315531bc023907`.
- **Equalizer APO** (GPL-2.0): 사용자가 직접 설치하는 선행 조건이다. 앱은 설치된 EQAPO의 `config.txt`와 `config\SBCT\` 프로필 폴더만 읽고 쓴다. 설치본을 동봉하지 않는다.
- **SECS** (`vendor/secs/SECS.py`): 피크 감쇄·최소위상 아이디어를 참고했다. 코드는 동봉하지 않는다. 배포 시 원문 배포 조건 확인이 필요하다.

PySide6는 LGPL-3.0 동적 링크 조건으로 사용한다. 사용자는 동일 API의 Qt 라이브러리로 교체할 수 있다.
