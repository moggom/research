# ��고서 출력 형식 (Output Format)

## 목적

최종 보고서(REPORT.md)의 구조, 각 섹션의 필수 요소, 분량 기준을 정의하여 보고서 품질과 가독성을 일관되게 유지한다.

---

## 1. 보고서 전체 구조

```
REPORT.md
├── 헤더 (메타 정보)
├── 종별 데이터 가용성 (Pre-Screening)
├── 유전자 기본 정보 (Alias Table)
├── 인접 유전자좌 정보
├── 조사 항목 1~N (Blueprint 순서)
├── Optional 항목
├── 종합 평가 (Summary Assessment)
└── 출처 목록 (References)
```

---

## 2. 헤더 (메타 정보)

보고서 최상단에 아래 정보를 표로 기재한다.

```markdown
| 항목 | 내용 |
|------|------|
| **대상 유전자** | {Gene Symbol} |
| **대상 질병** | {Disease/Indication} |
| **Narrow-down 조직** | {Organ/Tissue} |
| **조사 일자** | {YYYY-MM-DD} |
| **Blueprint 버전** | {버전 또는 파일 경로} |
```

---

## 3. 조사 항목 섹션 표준 구조

각 조사 항목은 아래 구조를 따른다.

```markdown
## {항목 번호}. {항목 제목}

### 요약 (1~3문장)
(이 항목의 핵심 결론을 간결하게 기술)

### 근거 수준
> [Evidence Level] — (판정 근거 1문장)

### 상세 내용

#### {하위 항목 1}
(서술형 내용, 출처 인라인 표기)

#### {하위 항목 2}
...

### 종별 요약 (해당하는 경우)
| 종 | 근거 수준 | 핵심 발견 |
|----|----------|----------|
| Homo sapiens | [Level] | ... |
| NHP | [Level] | ... |
| Rodent | [Level] | ... |
```

---

## 4. 종합 평가 섹션

보고서 말미에 반드시 포함한다.

### 필수 구성 요소

**a. 항목별 등급 요약 테이블**

```markdown
| 평가 항목 | 근거 수준 | 핵심 소견 |
|-----------|----------|----------|
| Mechanism of Action | [Level] | ... |
| Pathway Modulation | [Level] | ... |
| Therapeutic Association | [Level] | ... |
| Efficacy Data | [Level] | ... |
| Severity-Expression Correlation | [Level] | ... |
| Safety Data | [Level] | ... |
```

**b. Go / No-Go / Conditional 판단**

아래 3가지 중 하나를 명시한다.

| 판단 | 기준 |
|------|------|
| **Go** | Strong 증거 2개 이상, Safety 우려 없음 또는 관리 가능 |
| **Conditional** | Moderate 증거 존재, 추가 연구로 확인 가능한 불확실성 |
| **No-Go** | Insufficient/Weak 위주, 또는 Safety에 심각한 우려 |

**c. 판단 근거 서술 (3~5문장)**

Go/No-Go 판단의 핵심 논거를 간결하게 정리한다.

**d. 권고 사항 (해당하는 경우)**

- No-Go 시: 대안 접근법 또는 사전 필요 연구 제안
- Conditional 시: 불확실성 해소를 위한 구체적 실험/조사 제안

---

## 5. 출처 목록

### 구분 기재

출처를 아래 범주로 구분하여 기재한다.

```markdown
## 출처

### 1차 데이터베이스 (Primary Databases)
- [NCBI Gene - {Gene} ({ID})](URL)
- [UniProt - {Accession}](URL)
- ...

### 학술 문헌 (Peer-Reviewed Literature)
- Author et al. "Title." *Journal.* Year. [Link](URL)
- ...

### 데이터 포털 (Data Portals)
- [GTEx - {Gene}](URL)
- [IMPC - {Gene}](URL)
- ...
```

### 출처 표기 규칙

- 본문 내 인라인 출처: `(Author et al., Year)` 또는 `[출처명](URL)` 형태
- 모든 인라인 출처는 말미 출처 목록에도 포함
- URL은 가능한 한 영구 링크(permalink, DOI) 사용

---

## 6. 분량 가이드

| 섹션 | 권장 분량 |
|------|----------|
| 헤더 + Pre-Screening | 20줄 이내 |
| 조사 항목 (데이터 풍부) | 항목당 50~150줄 |
| 조사 항목 (근거 불충분) | 항목당 10~30줄 |
| 종합 평가 | 30~60줄 |
| 출처 목록 | 제한 없음 |

전체 보고서는 **500~1,500줄** 범위를 목표로 하되, 데이터 가용성에 따라 유동적으로 조정한다.
