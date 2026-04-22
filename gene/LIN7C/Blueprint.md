# Blueprint: Gene Research

## Project Definition
- **PITCH:** 아래 유전자의 Transcriptomic level 을 감소시켜서 특정 질병, indication에 대한 Therapeutic effect를 기대할 수 있는지에 대한 타당성 조사

## 조사 대상 범위 (필수)
- Gene: LIN7C
- Disease, Indication: Obesity

## 조사 대상 범위 (narrow-down)
- Organ/Tissue: adipose_subcutaneous, adipose_Visceral_Omentum

## 조사 항목
1. Mechanism of Action
- Basic Biological role of Gene/Protein (Overview)

2. Pathway Modulation: simple search of pathway (fragmented is okay)
- Transcriptomic level view
- Proteomic level view
- Genetic level view (epigenitic perspective)

3. Combined Pathway modulation
- combine fragmented pathway from "2.Pathway Modulation" if possible.

4. Function in Therapeutic Indication
- Association/causal relationship between Gene and Indication

3. Efficacy Data in an Animal Disease Model and/or Patient
- in homo sapiens
- in NHP (macaca fascicularis, macaca fascicularis)
- in rodent (mus musculus, rattus norvegicus)

4. Severity of Disease Correlated with the Transcriptomic Gene Expression Level
- in homo sapiens
- in NHP (macaca fascicularis, macaca fascicularis)
- in rodent (mus musculus, rattus norvegicus)

5. Safety Data in an Animal and/or Patient by Whole or Tissue-Specific Depletion
- in homo sapiens
- in NHP (macaca fascicularis, macaca fascicularis)
- in rodent (mus musculus, rattus norvegicus)

## 조사 항목 (Optional)
- Genome-Wide Association Studies (GWAS) Data
- Gene Expression in Tissue
- Pharmacodynamic Markers

## Agent Rules
1. 하나의 항목당 하나의 에이전트에게 할당해서 일을 시킬 것. 하위 항목이 있는 경우 각각의 하위 항목을 하나의 에이전트에게 배정을 하고, 그 상위 항목을 통합하는 에이전트또한 배정 해서 하위 항목의 결과가 확인된 다음에 상위 항목의 에이전트가 하위 항목 에이전트의 결과를 받아 통합할 수 있도록 할 것. 그리고 마지막에 QA 에이전트가 항목의 내용을 검토한다.
    - 예를 들어 "1. Mechanism of Action" 는 2 + 1 (QA) 개의 에이전트가 사용되고, "2. Pathway Modulation: simple search of pathway (fragmented is okay)"는 4 + 1 (QA) 개의 에이전트를 사용하는걸 전재한다.

2. Common Rule
    - 자료 조사 중 조사 대상 범위 (narrow-down)에 해당하는 내용이 있는 경우 관련된 내용을 우선시 한다.
    - 소스 사용 규칙
        - 공식 데이터베이스와 권위 기관 자료를 최우선 사용하고 위키, 블로그, 포럼, 출처 불명 사이트는 제외
        - 2차 요약 자료/사이트는 사용하지 않는다. (e.g GeneCards)
        - 질병 연관성, 변이 해석, 임상적 의미는 반드시 ClinVar, ClinGen, OMIM, ACMG 등 권위 있는 출처로 교차검증한다.
        - 데이터 와 자료가 어느 종 (Species) 에서 얻어진 데이터인지 반드시 확인 하고 구분할 것.
        - 임상적 의미는 과장하지 말고 근거 수준에 따라 설명하라.
        - 정보가 부족한 경우 그 점을 분명히 밝히라.

    - 우선 출처
        - NCBI Gene, Ensembl, HGNC, UniProt, OMIM
        - ClinVar, ClinGen
        - GTEx, The Human Protein Atlas
        - PubMed, PubMed Central

    3. 출처 규칙
    - 핵심 사실은 가능한 한 2개 이상의 신뢰도 높은 출처로 교차검증
    - 확실하지 않은 내용은 추정하지 말고 "근거 불충분" 또는 "합의 없음"이라고 표시
    - 절대 하지 말 것:
        - 출처 없이 단정
        - 동물실험 결과를 인간에서 확립된 사실처럼 서술
        - 단일 논문 결과를 정설처럼 일반화
        - 임상적 유의성을 과장
        - 최신 여부가 불명확한 정보를 단정적으로 표현

3. Agent rule (Researcher)
    - 특정 유전자에 대해 신뢰성 있는 출처를 바탕으로 조사 항목을 조사하고 정리한다.
    - 정확성, 출처 품질을 우선한다.
    - 확실하지 않은 내용은 추측하지 말고 "근거 불충분" 또는 "명확한 합의 없음"이라고 표시한다.
    - 의견을 추가하지 않는다. 해석이 필요한 경우 그 부분을 Manager 에게 넘긴다.

4. Agent rule (Manager)
    - Researcher의 내용이 Common Rule / Agent rule (Researcher) 에 맞춰서 작성되었는지 검토한다.
    - 다른 Maneger 에게 보고해야 하는 내용이 있는 경우 Agent rule (Researcher) 을 따라서 조사한다.

5. Agent rule (QA)
    - 조사된 내용과 출처가 일치하는지 확인
    - 일치하지 않으면 재조사 요청
