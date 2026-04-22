# 종별 사전 스크리닝 (Species Pre-Screening)

## 목적

본 조사의 종별(Human, NHP, Rodent) 데이터 가용성을 조사 초기에 빠르게 파악하여, 데이터가 전무한 종에 대해 불필요한 반복 검색을 방지한다.

---

## 1. 사전 스크리닝 절차

모든 조사 항목에 앞서, 대상 유전자에 대한 **종별 데이터 가용성 스크리닝**을 1회 수행한다.

### 스크리닝 검색 (종당 2~3회)

| 종 | 스크리닝 검색 | 대상 DB |
|----|-------------|---------|
| **Homo sapiens** | `{Gene} human` | PubMed (최근 10년) |
| | `{Gene}` | ClinVar, OMIM |
| **NHP** | `{Gene} macaque OR primate OR NHP` | PubMed |
| | `{Gene} {NHP 종명}` | NCBI Gene (ortholog 확인) |
| **Rodent** | `{Gene} mouse OR rat` | PubMed |
| | `{Mouse ortholog symbol}` | IMPC |

### 판정 기준

| 결과 | 판정 | 후속 조치 |
|------|------|----------|
| 직접 관련 논문 3건 이상 | **Data Available** | 전체 조사 항목에서 해당 종 포함 |
| 직접 관련 논문 1~2건 | **Limited Data** | 조사 포함하되, 데이터 제한을 사전 고지 |
| 직접 관련 논문 0건, ortholog 정보만 존재 | **Ortholog Only** | Ortholog 기본 정보만 기재, 항목별 반복 검색 생략 |
| 관련 정보 전무 | **No Data** | 일괄 "해당 종 데이터 미존재"로 보고, 항목별 반복 검색 생략 |

---

## 2. 스크리닝 결과 산출물

스크리닝 결과는 보고서 상단 또는 별도 섹션에 아래 형태로 포함한다.

```markdown
## 종별 데이터 가용성 (Pre-Screening)

| 종 | Ortholog | Gene ID | 데이터 가용성 | PubMed 검색 결과 |
|----|----------|---------|-------------|-----------------|
| Homo sapiens | LIN7C | 55327 | Limited Data | 직접 관련 2��� |
| Macaca fascicularis | LIN7C | (ID) | No Data | 0건 |
| Macaca mulatta | Lin7c | (ID) | Ortholog Only | ortholog 정보만 |
| Mus musculus | Lin7c | 22343 | Limited Data | KO 표현형 1건 |
| Rattus norvegicus | Lin7c | (ID) | Ortholog Only | ortholog 정보만 |
```

---

## 3. "No Data" 종의 간결 보고

사전 스크리닝에서 "No Data"로 판정된 종은, 각 조사 항목에서 개별적으로 반복 검색하지 않고 아래와 같이 일괄 처리한다.

```markdown
### X.X NHP (Macaca mulatta, Macaca fascicularis)

> 사전 스크리닝(종별 데이터 가용성 참조)에서 해당 종의 LIN7C 관련 연구가
> 확인되지 않아 항목별 상세 조사를 생략함.
> 근거 수준: [Insufficient] — 해당 종 데이터 미존재
```

이를 통해 보고서에서 동일한 "근거 불충분" 서술이 매 항목마다 반복되는 것을 방지한다.

---

## 4. Ortholog 기본 정보 기재 사항

"Ortholog Only" 판정 시, 아래 정보만 1회 기재한다.

| 항목 | 내용 |
|------|------|
| Ortholog symbol | (해당 종의 유전자 기호) |
| NCBI Gene ID | (해당 종의 Gene ID) |
| Sequence identity (%) | (인간 대비 아미노산 서열 동일성) |
| Synteny 보존 여부 | (Yes/No) |
| 주요 발현 조직 (해당 종) | (확인 가능한 경우) |
