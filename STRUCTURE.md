# STRUCTURE · baliwaxing-sample

```
baliwaxing-sample/
├─ index.html              단일 파일 (CSS·JS 인라인)
├─ wrangler.toml           name = baliwaxing-sample → baliwaxing-sample.lgt3232.workers.dev
├─ .assetsignore           img/·문서·index_*.html·bl-logo.png 배포 제외
├─ bl-montserrat.woff2     영문 · 숫자 (Montserrat 500–900, 라틴만)
├─ bl-pretendard.woff2     한글 · 본문 (Pretendard 400–800, 사용 글자만 → 글자 추가 시 재생성)
├─ bl-logo.webp            로고 투명 (헤더 · 푸터)
├─ bl-wax/care/lounge.webp 히어로 크로스페이드 (care는 공간 섹션에도)
├─ bl-ba-*.webp            시술 기록 6장 (brow 2 · hair 2 · nape 2)
├─ bl-cert/stick.webp      공간 섹션
├─ favicon.png / og-bali.jpg
├─ img/                    다올 제공 원본 117장 (배포 제외)
└─ CHANGELOG.md / STRUCTURE.md
```

## 섹션 순서
헤더 → 히어로(`#pics`) → `.facts`(노랑 숫자 띠) → `#why` → `#results`(회색 면) → `#price` → `#space`(회색 면) → `#visit` → 검정 푸터 + 모바일 `.quick` 하단 바.

## 가격 수정
`#price .tbl` 표: 한 줄 = `<tr><td>시술</td><td>여자</td><td>남자</td></tr>`. 성별 구분 없는 가격은 `<td class="span" colspan="2">`. 첫만남 이벤트는 `.first .row`.

## 영업시간 수정 (3곳)
`#visit .hours` · 푸터 문장 · head JSON-LD.

## 색 규칙
노랑 `--y`는 면 · `mark` 형광펜 · 버튼에만. 흰 바탕 위 글자색으로 쓰지 않음.

## 폰트 재생성
`pyftsubset … --name-IDs='*' --name-languages='*' --name-legacy` (LESSONS §24). 둘 다 Variable을 instancer로 굵기 범위 자른 뒤 서브셋.
