<p align="center"><img src="docs/banner.png" alt="노트 먼저 찾아보기: 같은 실수, 내 노트가 먼저 막아 줍니다" width="100%"></p>

<p align="center">
<a href="https://github.com/reedodev/vault-recall/actions/workflows/test.yml"><img src="https://github.com/reedodev/vault-recall/actions/workflows/test.yml/badge.svg" alt="test"></a>
<img src="https://img.shields.io/badge/Claude_Code-skill-2547F4" alt="Claude Code skill">
<img src="https://img.shields.io/badge/license-MIT-black" alt="MIT">
</p>

# 노트 먼저 찾아보기 (vault-recall)

일을 시작하기 전에 옵시디언(마크다운) 보관함에서 이번 작업과 관련된 지난 교훈·실패·해결 기록을 찾아 먼저 읽게 합니다. 한국어는 두 글자 단위로 비교해 조사가 달라도 찾고, 확인된 노트와 최근 노트에 점수를 더 줍니다.

## 설치

**Claude Code 플러그인으로 설치**

```
/plugin marketplace add reedodev/vault-recall
/plugin install vault-recall@vault-recall
```

**폴더만 복사**

```bash
git clone https://github.com/reedodev/vault-recall.git
cp -r vault-recall/skills/vault-recall ~/.claude/skills/
```

필요한 것: Node 18+

## 바로 해 보기

```bash
node skills/vault-recall/scripts/recall.mjs ~/MyVault "유튜브 쇼츠 예약 공개 고정 댓글" --top 5
```

자세한 절차, 옵션, 한계는 [SKILL.md](skills/vault-recall/SKILL.md)에 있습니다. 에이전트가 이 파일을 읽고 그대로 따릅니다.

## 시험

`node tests/run.mjs`가 SKILL.md 형식을 검사하고 예시 파일로 스크립트를 실제로 실행합니다. 푸시할 때마다 GitHub Actions가 같은 시험을 돌립니다(위 test 배지).

## 만든 사람

**리도**, AI 좌충우돌 실습 중인 20년차 엔지니어입니다. 매일 AI에게 일을 맡기다가 막힌 부분을 고쳐 가며 이 스킬을 만들었습니다.
[YouTube @Reedodev](https://www.youtube.com/@Reedodev) · [Threads @reedo.dev](https://www.threads.com/@reedo.dev) · [GitHub @reedodev](https://github.com/reedodev)

같이 만든 다른 스킬: [옵시디언 3D 지식그래프](https://github.com/reedodev/obsidian-brain-3d) · [작업 기록 강의자료](https://github.com/reedodev/work-to-lecture-deck) · [한국어 말투 점검](https://github.com/reedodev/korean-tone-check) · [네이버 황금키워드](https://github.com/reedodev/naver-golden-keywords) · [한글 양식 채우기](https://github.com/reedodev/hwpx-form-fill) · [TTS 끝소리 고치기](https://github.com/reedodev/tts-tail-fix) · [카드뉴스 렌더](https://github.com/reedodev/html-card-render) · [영상 비율 검사](https://github.com/reedodev/social-video-gate) · [유튜브 게시 점검](https://github.com/reedodev/youtube-publish-checklist)

---

## English

Before a task, recall relevant past lessons from an Obsidian/markdown vault: Korean-aware bigram search, status and recency weighting, cached index (8k notes in under a second after the first run).

Install: `/plugin marketplace add reedodev/vault-recall` then `/plugin install vault-recall@vault-recall`, or copy `skills/vault-recall` into `~/.claude/skills/`. See [SKILL.md](skills/vault-recall/SKILL.md) for the full procedure. MIT License; third-party models, fonts and libraries keep their own licenses.
