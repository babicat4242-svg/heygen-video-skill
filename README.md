# HeyGen Video Skill

HeyGen용 한국어 영상 제작·프롬프트 스킬입니다. 씨댄스 2.5의 서비스 독립적인 연출 지침을 각색하여 인물 행동, 감정, 카메라, 조명, 오디오, 연속성과 후속 수정을 다룹니다.

## 설치

`heygen-video` 폴더를 개인 Codex 스킬 디렉터리 `~/.codex/skills/`에 복사합니다.

## 사용

`$heygen-video 첨부 이미지를 바탕으로 5초 영상 프롬프트를 만들어줘. 인물 동작을 명확하게 넣고 배경음악은 빼줘.`

프롬프트 작성에는 HeyGen 연결이 필요하지 않습니다. 실제 생성에는 사용 가능한 HeyGen 연동 또는 CLI/웹 세션과 해당 기능 지원이 필요합니다. 참조 제어, 길이, 오디오는 현재 서비스에서 확인합니다.

## 포함 범위

- 이미지 기반 영화·판타지·광고·뮤직비디오 연출
- 관찰 가능한 인물 행동·감정, 카메라와 주체 움직임 분리
- 참조·조명·프레임·오디오 보존 규칙
- NO BGM, 완전 무음, 원본 오디오, 무반주 보컬 구분
- 전체 교체 프롬프트를 통한 길이·동작·음향 수정
- 아바타 발표 대본, 생성 작업 확인, 번역·더빙 준비

씨댄스 전용 API·모델 사양·태그를 HeyGen 기능으로 간주하지 않습니다. 전체 사례 라이브러리의 복제본이 아닙니다. HeyGen 공식 배포 스킬이 아닌 개인 작성 스킬입니다.


## Claude에서 사용

### Claude Code

이 저장소의 `heygen-video` 폴더 전체를 `~/.claude/skills/heygen-video/` 위치에 설치합니다. 결과 경로는 `~/.claude/skills/heygen-video/SKILL.md`여야 합니다. 프로젝트 전용 설치는 `.claude/skills/heygen-video/`을 사용합니다. `references/`도 함께 보존하세요.

호출 예: `/heygen-video 첨부 이미지로 인물 동작이 명확한 영상 프롬프트를 만들어줘. 배경음악은 빼줘.`

### Claude 웹·데스크톱 사용자 스킬

[Claude 업로드용 ZIP](dist/heygen-video-claude.zip)을 다운로드해 사용자 스킬 업로드 기능에서 등록하고 활성화합니다. GitHub 저장소 전체 ZIP 대신 이 파일을 사용하세요. 스킬 루트 폴더 안에 SKILL.md와 참고자료가 들어 있습니다.

자연어 요청 예: “heygen-video 스킬로 첨부 이미지의 영상 프롬프트를 작성해줘.” 실제 생성 연결은 별도로 필요합니다. 계정·조직 설정에 따라 사용자 스킬 업로드 기능이 제공되지 않을 수 있습니다.

Codex에서는 기존 `~/.codex/skills/heygen-video/` 설치와 `$heygen-video` 호출을 그대로 사용합니다. Codex용 `agents/openai.yaml`은 Claude 업로드 ZIP에서 제외했습니다.

공식 설치 근거: [Claude Code Skills](https://code.claude.com/docs/en/skills), [Claude 사용자 스킬](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills).

검증 범위: 패키지 구조·frontmatter·내부 참조를 확인했습니다. Claude 앱에 실제 업로드해 실행하거나 영상 생성을 검증한 것은 아닙니다.
