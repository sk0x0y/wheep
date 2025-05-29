# 시스템 패턴 (System Patterns)

- **모노레포 아키텍처**: Turborepo (태스크 오케스트레이션, 캐싱), Pnpm Workspaces (패키지 관리, 호이스팅).
- **패키지 구조**: FSD `shared` 레이어와 연계된 `ui`, `lib`, `config` 패키지.
- **2-depth 임포트**: `exports` 필드를 활용한 패키지 내부 모듈화.
