# 검색 전략 (Search Strategy)

## 목적

조사 대상 유전자에 대해 누락 없이 체계적으로 정보를 수집하기 위한 검색 절차를 정의한다.

---

## 1. 유전자 별칭(Alias) 전수 확인

조사 시작 전, 대상 유전자의 **모든 공식 별칭**을 수집한다. 이후 모든 검색에 별칭을 포함한다.

### 수집 절차

1. NCBI Gene → "Also known as" 필드 확인
2. UniProt → "Gene names" 섹션 확인
3. HGNC → "Previous symbols", "Alias symbols" 확인
4. Ensembl → "Synonyms" 확인

### 적용 방법

- 모든 PubMed/PMC 검색에 별칭을 OR 조건으로 포함
  - 예: `("LIN7C" OR "MALS-3" OR "VELI3" OR "MALS3") AND obesity`
- 데이터베이스마다 인식하는 명칭이 다를 수 있으므로, 각 DB에서 검색 가능한 ID도 정리
  - 예: NCBI Gene ID, Ensembl Gene ID, UniProt Accession

### 산출물

조사 보고서 상단에 아래 형태의 **별칭 테이블**을 포함한다:

| 출처 | ID/Symbol |
|------|-----------|
| HGNC | LIN7C |
| NCBI Gene | 55327 |
| Ensembl | ENSG00000166126 |
| UniProt | Q9NUP9 |
| Aliases | MALS3, VELI3, LIN-7C, MALS-3 |

---

## 2. 인접 유전자좌(Locus) 식별

대상 유전자의 염색체 위치에서 **±500kb 이내의 주요 유전자**를 확인하고, GWAS 해석 시 혼동을 방지한다.

### 절차

1. NCBI Gene 또는 Ensembl에서 대상 유전자의 genomic coordinate 확인
2. UCSC Genome Browser 또는 Ensembl Region View로 인접 유전자 목록 확보
3. 인접 유전자 중 **대상 질병과 기존 연관이 알려진 유전자**를 별도 기록

### 적용 방법

- GWAS 데이터 해석 시, 인접 유전자의 효과와 대상 유전자의 효과를 구분하는 서술을 반드시 포함
- Fine-mapping 또는 colocalization 데이터가 없는 경우, "인접 유전자와의 구분이 불가"로 명시

---

## 3. 항목별 권장 검색 조합

각 조사 항목에 대해 최소한 아래의 검색 조합을 수행한다.

### Mechanism of Action

| 검색 쿼리 패턴 | 대상 DB |
|----------------|---------|
| `{Gene} function biological role` | NCBI Gene, UniProt |
| `{Gene} protein domain interaction` | UniProt, STRING-DB, IntAct |
| `{Gene} pathway` | Reactome, KEGG |
| `{Gene} expression tissue` | GTEx, Human Protein Atlas |

### Therapeutic Indication 연관

| 검색 쿼리 패턴 | 대상 DB |
|----------------|---------|
| `{Gene} {Disease}` | PubMed |
| `{Gene} {Disease} association` | PubMed, GWAS Catalog |
| `{Gene} {관련 경로 키워드}` | PubMed |
| `{Gene} knockout phenotype` | IMPC, PubMed |

### Efficacy / Safety

| 검색 쿼리 패턴 | 대상 DB |
|----------------|---------|
| `{Gene} knockdown siRNA shRNA` | PubMed |
| `{Gene} knockout mouse phenotype` | IMPC, PubMed |
| `{Gene} clinical trial` | ClinicalTrials.gov |
| `{Gene} loss of function variant` | ClinVar, gnomAD |

### GWAS

| 검색 쿼리 패턴 | 대상 DB |
|----------------|---------|
| `{Gene} GWAS {Disease}` | GWAS Catalog, PubMed |
| `{Gene} eQTL {Tissue}` | GTEx |
| `{Locus} BMI` (좌표 기반) | GWAS Catalog |

---

## 4. 검색 기록(Search Log)

각 에이전트는 수행한 검색을 아래 형태로 기록한다. 이 로그는 QA 검토와 재현성 확보에 사용된다.

```markdown
| # | 검색 쿼리 | 대상 DB | 결과 건수 | 유효 결과 유무 |
|---|----------|---------|----------|--------------|
| 1 | "LIN7C" AND obesity | PubMed | 0 | 없음 |
| 2 | "LIN7C" knockout mouse | PubMed | 3 | 있음 |
```
