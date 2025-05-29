# 시스템 패턴 (System Patterns)

- **모노레포 아키텍처**: Turborepo (태스크 오케스트레이션, 캐싱), Pnpm Workspaces (패키지 관리, 호이스팅). React Native 앱 (`apps/mobile`) 통합.
- **패키지 구조**: FSD `shared` 레이어와 연계된 `ui`, `lib`, `config` 패키지. React Native 앱 (`apps/mobile`)에 FSD 아키텍처 적용 (`src/{app,pages,widgets,features,entities}`).
- **2-depth 임포트**: `exports` 필드를 활용한 패키지 내부 모듈화. `@whip/ui/design-system`과 같은 패턴으로 React Native 컴포넌트 및 유틸리티 모듈 관리.
- **Git 전략**: GitHub Flow (1인 개발 환경 최적화). `main` 브랜치는 항상 배포 가능한 상태를 유지하며, 빠른 배포를 위해 `main` 브랜치에 직접 커밋을 푸시하는 것을 허용합니다. 각 커밋은 작고 명확한 단위로 구성합니다.
