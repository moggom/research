# Blueprint: Gene Research

## Project Definition
- **PITCH:** 아래 유전자의 Transcriptomic level 을 감소시켜서 특정 질병, indication에 대한 Therapeutic effect를 기대할 수 있는지에 대한 타당성 조사

## 조사 대상 범위 (필수)
- Gene: {유전자 기호}
- Disease, Indication: {질병/적응증}

## 조사 대상 범위 (narrow-down)
- Organ/Tissue: {조직1}, {조직2}
- Narrow-down은 **제한이 아닌 우선순위**를 의미한다. 상세 확장 절차는 → [narrow-down-fallback.md](rules/narrow-down-fallback.md) 참조

---

## 조사 절차

### Phase 0: 사전 준비

조사 항목 착수 전에 아래 두 작업을 반드시 수행한다.

**0-1. 유전자 별칭 및 인접 유전자좌 확인**
- 대상 유전자의 모든 공식 별칭(alias)을 수집하고, 인접 유전자좌의 주요 유전자를 식별한다.
- 상세 절차 → [search-strategy.md](rules/search-strategy.md) §1, §2

**0-2. 종별 데이터 가용성 사전 스크리닝**
- 각 종(Human, NHP, Rodent)에 대해 데이터 가용성을 빠르게 파악한다.
- 데이터가 전무한 종은 항목별 반복 검색을 생략하고 일괄 처리한다.
- 상세 절차 → [species-screening.md](rules/species-screening.md)

---

### Phase 1: 항목별 조사

## 조사 항목
1. Mechanism of Action
- Basic Biological role of Gene/Protein (Overview)

2. Pathway Modulation: simple search of pathway (fragmented is okay)
- Transcriptomic level view
- Proteomic level view
- Genetic level view (epigenetic perspective)

3. Combined Pathway modulation
- combine fragmented pathway from "2.Pathway Modulation" if possible.

4. Function in Therapeutic Indication
- Association/causal relationship between Gene and Indication

5. Efficacy Data in an Animal Disease Model and/or Patient
- in homo sapiens
- in NHP (macaca mulatta, macaca fascicularis)
- in rodent (mus musculus, rattus norvegicus)

6. Severity of Disease Correlated with the Transcriptomic Gene Expression Level
- in homo sapiens
- in NHP (macaca mulatta, macaca fascicularis)
- in rodent (mus musculus, rattus norvegicus)

7. Safety Data in an Animal and/or Patient by Whole or Tissue-Specific Depletion
- in homo sapiens
- in NHP (macaca mulatta, macaca fascicularis)
- in rodent (mus musculus, rattus norvegicus)

## 조사 항목 (Optional)
- Genome-Wide Association Studies (GWAS) Data
- Gene Expression in Tissue
- Pharmacodynamic Markers

---

### Phase 2: 통합 및 QA

- Manager가 하위 항목을 통합하고, QA가 출처-내용 일치를 검증한다.
- 상세 절차 → [agent-interface.md](rules/agent-interface.md) §2, §4

### Phase 3: 보고서 작성

- 최종 보고서(REPORT.md)를 표준 형식에 맞춰 작성한다.
- 종합 평가에서 Go / No-Go / Conditional 판단을 명시한다.
- 상세 형식 → [output-format.md](rules/output-format.md)

---

## Rules

### 1. Agent Rules

하나의 항목당 하나의 에이전트에게 할당해서 일을 시킬 것. 하위 항목이 있는 경우 각각의 하위 항목을 하나의 에이전트에게 배정을 하고, 그 상위 항목을 통합하는 에이전트또한 배정 해서 하위 항목의 결과가 확인된 다음에 상위 항목의 에이전트가 하위 항목 에이전트의 결과를 받아 통합할 수 있도록 할 것. 그리고 마지막에 QA 에이전트가 항목의 내용을 검토한다.

- 예를 들어 "1. Mechanism of Action" 는 2 + 1 (QA) 개의 에이전트가 사용되고, "2. Pathway Modulation"는 4 + 1 (QA) 개의 에이전트를 사용하는걸 전제한다.

**에이전트 간 산출물 형식, 실행 실패 시 fallback 절차, 역할별 검토 체크리스트** → [agent-interface.md](rules/agent-interface.md)

### 2. Common Rule

#### 2-1. Narrow-Down 우선

자료 조사 중 조사 대상 범위 (narrow-down)에 해당하는 내용이 있는 경우 관련된 내용을 우선시 한다.  
Narrow-down 범위에서 데이터가 부족할 때의 **단계적 확장 절차** → [narrow-down-fallback.md](rules/narrow-down-fallback.md)

#### 2-2. 소스 사용 규칙

- 공식 데이터베이스와 권위 기관 자료를 최우선 사용하고 위키, 블로그, 포럼, 출처 불명 사이트는 제외
- 2차 요약 자료/사이트는 사용하지 않는다. (e.g GeneCards)
- 질병 연관성, 변이 해석, 임상적 의미는 반드시 ClinVar, ClinGen, OMIM, ACMG 등 권위 있는 출처로 교차검증한다.
- 데이터와 자료가 어느 종(Species)에서 얻어진 데이터인지 반드시 확인하고 구분할 것.
- 임상적 의미는 과장하지 말고 근거 수준에 따라 설명하라.
- 정보가 부족한 경우 그 점을 분명히 밝히라.

#### 2-3. 우선 출처

- NCBI Gene, Ensembl, HGNC, UniProt, OMIM
- ClinVar, ClinGen
- GTEx, The Human Protein Atlas
- PubMed, PubMed Central

#### 2-4. 검색 전략

각 조사 항목에 대해 **항목별 권장 검색 조합, 별칭 검색, 검색 로그 기록**을 수행한다.  
상세 → [search-strategy.md](rules/search-strategy.md)

#### 2-5. 증거 등급

모든 조사 결과에 **Strong / Moderate / Weak / Insufficient** 등급을 부여한다.  
등급 정의 및 적용 규칙 → [evidence-grading.md](rules/evidence-grading.md)

### 3. 출처 규칙

- 핵심 사실은 가능한 한 2개 이상의 신뢰도 높은 출처로 교차검증
- 확실하지 않은 내용은 추정하지 말고 "근거 불충분" 또는 "합의 없음"이라고 표시
- "근거 불충분" 판정 시 **최소 검색 요건 및 보고 양식** → [insufficient-evidence.md](rules/insufficient-evidence.md)
- 절대 하지 말 것:
    - 출처 없이 단정
    - 동물실험 결과를 인간에서 확립된 사실처럼 서술
    - 단일 논문 결과를 정설처럼 일반화
    - 임상적 유의성을 과장
    - 최신 여부가 불명확한 정보를 단정적으로 표현

### 4. Agent Rule (Researcher)

- 특정 유전자에 대해 신뢰성 있는 출처를 바탕으로 조사 항목을 조사하고 정리한다.
- 정확성, 출처 품질을 우선한다.
- 확실하지 않은 내용은 추측하지 말고 "근거 불충분" 또는 "명확한 합의 없음"이라고 표시한다.
- 의견을 추가하지 않는다. 해석이 필요한 경우 그 부분을 Manager에게 넘긴다.
- **산출물은 표준 형식에 맞춰 작성한다** → [agent-interface.md](rules/agent-interface.md) §1

### 5. Agent Rule (Manager)

- Researcher의 내용이 Common Rule / Agent Rule (Researcher)에 맞춰서 작성되었는지 검토한다.
- **검토 체크리스트를 사용하여 체계적으로 검토한다** → [agent-interface.md](rules/agent-interface.md) §4
- 다른 Manager에게 보고해야 하는 내용이 있는 경우 Agent Rule (Researcher)을 따라서 조사한다.

### 6. Agent Rule (QA)

- 조사된 내용과 출처가 일치하는지 확인
- 일치하지 않으면 재조사 요청
- **QA 검토 체크리스트 및 불합격 시 절차** → [agent-interface.md](rules/agent-interface.md) §4

---

## Rules 참조 파일 목록

| 파일 | 내용 |
|------|------|
| [rules/search-strategy.md](rules/search-strategy.md) | 별칭 전수 확인, 인접 유전자좌 식별, 항목별 검색 조합, 검색 로그 |
| [rules/evidence-grading.md](rules/evidence-grading.md) | Strong/Moderate/Weak/Insufficient 등급 정의 및 적용 규칙 |
| [rules/insufficient-evidence.md](rules/insufficient-evidence.md) | 최소 검색 요건, 중단 기준, 보고 양식, 에스컬레이션 |
| [rules/agent-interface.md](rules/agent-interface.md) | 산출물 표준 형식, 실패 Fallback, 역할별 체크리스트 |
| [rules/narrow-down-fallback.md](rules/narrow-down-fallback.md) | 범위 확장 3단계 절차, 질병별 확장 조직 매핑 |
| [rules/species-screening.md](rules/species-screening.md) | 종별 데이터 가용성 사전 스크리닝, 간결 보고 절차 |
| [rules/output-format.md](rules/output-format.md) | 보고서 구조, 섹션 표준, Go/No-Go 판단, 분량 가이드 |
