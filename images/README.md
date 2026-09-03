# Club Card Images

클럽 카드에 표시될 썸네일 이미지입니다.

## 파일명 규칙

`{club_id}.png`

- 온라인 클럽: `0.png`, `1.png`, `2.png`, ... (숫자 id)
- 오프라인 클럽: `a.png`, `b.png`, `c.png`, ... (알파벳 id)

예:
- `0.png` — 주간회고클럽 (id: 0)
- `a.png` — 와인 소사이어티 (id: a)
- `s.png` — 정동백합정원 (id: s)

## 자동 매핑

index.html이 각 클럽 카드를 그릴 때 `./images/{club.id}.png` 를 자동으로 찾아 표시합니다.
파일이 없으면 이미지 영역이 숨겨집니다 (에러 없음).

## 크기 권장

- 가로 1400px × 세로 800px 내외 (권장)
- 파일 크기 500KB 이하 권장

## 옵시디언에서 커스텀 URL 지정

특정 클럽에 외부 URL을 쓰고 싶으면 옵시디언 노트 frontmatter에 image 필드 추가:

```yaml
---
club_id: 0
name: 주간회고클럽
image: "https://example.com/my-image.jpg"
...
---
```

이 값이 있으면 `./images/{id}.png` 대신 이 URL을 사용합니다.
sync-clubs 실행 후 반영됩니다.
