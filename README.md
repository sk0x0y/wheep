# Wheep 모노레포

## 소개

이 저장소는 React Native 애플리케이션과 공유 가능한 디자인 시스템 및 공통 컴포넌트를 효율적으로 개발, 관리, 유지보수하기 위한 통합 모노레포 환경입니다. 개발 생산성 향상, 코드 품질 일관성 확보, 그리고 향후 확장 및 유지보수가 용이한 아키텍처 기반 마련을 목표로 합니다.

## 주요 기술 스택

- **Turborepo**: 모노레포 내의 태스크 오케스트레이션 및 빌드 캐싱을 통해 개발 속도를 최적화합니다.
- **Pnpm**: 효율적인 패키지 관리와 워크스페이스 기능을 제공하여 디스크 공간을 절약하고 설치 속도를 향상시킵니다.
- **React Native**: 모바일 애플리케이션 개발을 위한 크로스 플랫폼 프레임워크입니다.
- **TypeScript**: 코드의 안정성과 개발 생산성을 높이는 타입스크립트 언어를 사용합니다.
- **ESLint**: 코드 품질과 스타일 일관성을 유지하기 위한 린팅 도구입니다 (Google 규칙 기반).
- **Prettier**: 코드 포맷팅을 자동화하여 코드 스타일을 통일합니다.

## 프로젝트 구조

```
.
├── apps/
│   └── mobile/             # React Native 모바일 애플리케이션
├── packages/
│   ├── ui/                 # @wheep/ui: 디자인 시스템 및 공통 UI 컴포넌트
│   ├── lib/                # @wheep/lib: 공통 유틸리티, 헬퍼, API 클라이언트 등
│   └── config/             # @wheep/config: 공유 ESLint, Prettier, TypeScript 설정
├── docs/                   # 프로젝트 문서 (PRD, CONTRIBUTING 등)
├── .eslintrc.js            # 루트 ESLint 설정
├── .prettierrc.js          # 루트 Prettier 설정
├── tsconfig.json           # 루트 TypeScript 설정
├── pnpm-workspace.yaml     # Pnpm 워크스페이스 정의
├── package.json            # 루트 패키지 설정 및 스크립트
└── turbo.json              # Turborepo 설정
```

## 시작하기

### 전제 조건

- Node.js (v18 이상 권장)
- Pnpm (설치: `npm install -g pnpm`)

### 설치

1.  저장소를 클론합니다:
    ```bash
    git clone [저장소 URL]
    cd wheep
    ```
2.  의존성을 설치합니다:
    ```bash
    pnpm install
    ```

### 개발 서버 실행

- **모바일 앱 개발 서버 실행**:
  ```bash
  pnpm dev # 또는 turbo dev
  ```
  (이 명령은 `apps/mobile` 워크스페이스의 개발 서버를 시작합니다. React Native 앱 실행을 위한 추가 설정이 필요할 수 있습니다.)

## 스크립트

루트 `package.json`에 정의된 주요 스크립트입니다. `pnpm <script-name>` 또는 `turbo run <task-name>`으로 실행할 수 있습니다.

- `dev`: 모든 워크스페이스의 개발 서버를 시작합니다.
- `build`: 모든 워크스페이스의 프로젝트를 빌드합니다.
- `lint`: 모든 워크스페이스의 코드를 린팅합니다.
- `format`: 모든 워크스페이스의 코드를 Prettier로 포맷팅합니다.
- `test`: 모든 워크스페이스의 테스트를 실행합니다 (설정 후).

## 워크스페이스

- **`apps/mobile`**: Wheep 모바일 애플리케이션의 소스 코드가 포함됩니다.
- **`packages/ui`**: `@wheep/ui` 패키지로, 재사용 가능한 UI 컴포넌트, 디자인 토큰 및 테마를 제공합니다.
- **`packages/lib`**: `@wheep/lib` 패키지로, 공통 유틸리티 함수, 헬퍼, API 클라이언트 및 타입 정의를 포함합니다.
- **`packages/config`**: `@wheep/config` 패키지로, 모노레포 전체에 적용되는 공유 ESLint, Prettier, TypeScript 설정을 관리합니다.

## 코드 컨벤션

이 프로젝트는 ESLint와 Prettier를 사용하여 코드 스타일과 포맷팅을 일관되게 유지합니다.

- **자동 포맷팅**: `pnpm format` 명령을 실행하여 모든 파일을 Prettier로 포맷팅할 수 있습니다.
- **린팅**: `pnpm lint` 명령을 실행하여 코드 품질 문제를 확인할 수 있습니다.

## 기여

프로젝트 기여에 대한 자세한 내용은 [CONTRIBUTING.md](docs/CONTRIBUTING.md) 파일을 참조하십시오.

## 라이선스

[라이선스 정보]
