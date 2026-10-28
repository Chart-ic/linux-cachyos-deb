# CachyOS 커널 빌더
내가 쓸려고 수정한 것 | edited for myself
 > 원본 README는 [여기를 참조하세요.](./README_orig.md)

## 주요 변경점 | What's changed?
 - `INSTALL_MOD_STRIP=1` 추가 | Added `INSTALL_MOD_STRIP=1` (Line 381)
   - 해당 옵션이 없을 경우 디버깅 심볼로 인하여 초기 ramdisk 용량이 증가한다 하여 추가하였습니다. [참고](https://unix.stackexchange.com/questions/30345/why-is-my-initial-ramdisk-so-big)

 - 사용 불가능한 패치 수정 | Fixed unavailable patch (Line 442)
   - SCHED_EXT+BORE 스케줄러가 언제부턴가 사망하여 bore+cachy 패치로 수정하였습니다.

 - 커널 다운로드 링크 수정 | Fixed Kernel download link (Line 565~566)
   - 기존 링크는 mainline을 이용하는 것으로 알려져 수동으로 링크를 지정하였습니다. 수동으로 지정되었기 때문에 stable 커널 버전이 올라갈 경우 수정됩니다.(수정되지 않았을 경우 직접 수정해주시길 바라며, mainline을 이용하고 싶으신 경우 수동으로 지정된 구문을 제거한 뒤 윗 줄의 주석을 해제해주시길 바랍니다)
