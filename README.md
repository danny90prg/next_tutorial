# next_tutorial
[참고](https://nextjs.org/learn/dashboard-app/getting-started)

 
# node 설치
 가장 최신 대신 lts 18.20.4
```sh
curl -fsSL https://fnm.vercel.app/install | bash # install fnm(fast node manager)
fnm use --install-if-missing 18 # install node
node -v # 18.20.4
npm -v # 10.7.0

npm install -g pnpm # 패키지 관리자 설치
npx create-next-app@latest nextjs-dashboard --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" --use-pnpm # 앱 생성
cd nextjs-dashboard
```

# directory 구조
 - app
   ㄴ lib
   ㄴ ui
 - public
 - scripts
 - next.config.js
 - ...

# 파일 설명
 - /app/lib/placehodler-data.ts : db 테이블, 시드(초기데이터)
 - /app/lib/definitions.ts : db 반환 유형 수동 정의

# 개발 서버 실행
```sh
pnpm i
pnpm dev
```

# 글로벌 스타일
 - /app/ui
 - global.css : 글로벌 css 규칙 추가

글로벌 스타일 추가
```tsx
// /app/laout.tsx
import '@/app/ui/global.css';
```

## tailwind
 - CSS 프레임워크, TSX 마크업에 직접 추가
 - class 추가시 텍스트 파란색으로 바뀜