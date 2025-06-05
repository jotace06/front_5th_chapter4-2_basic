## 배포 url

https://front-5th-chapter4-2-basic-blue.vercel.app/

## 개선사항

### index.html

`이미지 최적화`

- WebP 포맷 적용: JPEG → WebP로 변경하여 1,027 KiB 절약
- 반응형 이미지: `<picture>` 태그로 디바이스별 최적화된 이미지 제공
- 지연 로딩: loading="lazy" 추가로 초기 페이지 로드 속도 향상

`리소스 로딩 최적화`

- Hero 이미지 preload: LCP 개선을 위해 중요 이미지 우선 로딩
- 스크립트 defer: 파싱 블로킹 방지로 200ms 절약
- 쿠키 스크립트 비동기화: 메인 스레드 블로킹 최소화

### products.js

`DOM 조작 최적화`

- DocumentFragment 사용: N번의 DOM 조작을 1번으로 줄여 reflow/repaint 최적화
- 이미지 크기 하드코딩 제거: CSS로 관리하도록 변경하여 유연성 확보

### styles.css

`CSS 구조 개선`

- CSS 변수 추가: 색상/크기 일관성 관리 및 유지보수성 향상
- 성능 속성 추가: will-change, contain 속성으로 렌더링 최적화

`애니메이션 최적화`

- Transform 기반 애니메이션: GPU 가속 활용
- Transition 추가: 부드러운 사용자 인터랙션

### 🎯 Lighthouse 점수

<div>
<img width="188" alt="Image" src="https://github.com/user-attachments/assets/b3bead4d-54a7-49d8-8ea2-fc9294738362" />
➡️
<img width="192" alt="Image" src="https://github.com/user-attachments/assets/6336d7ee-1329-464e-9fbf-fdb7e48b88f4" />
</div>
  
 ### 📊 Core Web Vitals (2024)
<div>
<img width="305" alt="Image" src="https://github.com/user-attachments/assets/cf72c92d-57df-4ee8-a996-12579198ce48" />
➡️
<img width="299" alt="Image" src="https://github.com/user-attachments/assets/bbc783ee-dc72-4593-a29e-1747a7613f12" />
</div>
