# LIN7C Transcriptomic Level 감소의 비만(Obesity) 치료 타당성 조사 보고서

**조사 대상 유전자:** LIN7C (lin-7 cell polarity scaffold C)  
**질병/적응증:** Obesity (비만)  
**조직 범위:** Adipose Subcutaneous, Adipose Visceral (Omentum)  
**조사 일자:** 2026-04-22

---

## 목차

1. [Mechanism of Action](#1-mechanism-of-action)
2. [Pathway Modulation](#2-pathway-modulation)
3. [Combined Pathway Modulation](#3-combined-pathway-modulation)
4. [Function in Therapeutic Indication](#4-function-in-therapeutic-indication)
5. [Efficacy Data in Animal Disease Model and/or Patient](#5-efficacy-data-in-animal-disease-model-andor-patient)
6. [Severity of Disease Correlated with Transcriptomic Gene Expression Level](#6-severity-of-disease-correlated-with-transcriptomic-gene-expression-level)
7. [Safety Data by Whole or Tissue-Specific Depletion](#7-safety-data-by-whole-or-tissue-specific-depletion)
8. [Optional: GWAS, Gene Expression in Tissue, Pharmacodynamic Markers](#8-optional-gwas-gene-expression-in-tissue-pharmacodynamic-markers)
9. [종합 평가](#9-종합-평가)

---

## 1. Mechanism of Action

### 1.1 Basic Biological Role of LIN7C Gene/Protein (Overview)

#### 유전자 기본 정보

| 항목 | 내용 |
|------|------|
| **공식 기호** | LIN7C |
| **정식 명칭** | lin-7 cell polarity scaffold C |
| **NCBI Gene ID** | 55327 |
| **UniProt ID** | Q9NUP9 (Homo sapiens) |
| **OMIM** | 612332 |
| **별칭** | MALS3, VELI3, LIN-7C, MALS-3 |
| **염색체 위치** | 11p14.1 |
| **좌표 (GRCh38)** | NC_000011.10 (27494418..27506769, complement) |
| **엑손 수** | 5 |
| **유전자 유형** | Protein coding |
| **RefSeq 상태** | VALIDATED |

> 출처: [NCBI Gene - LIN7C (55327)](https://www.ncbi.nlm.nih.gov/gene/55327), [NCBI GTR](https://www.ncbi.nlm.nih.gov/gtr/genes/55327/)

#### 단백질 구조 및 도메인

LIN7C 단백질은 두 개의 주요 단백질-단백질 상호작용 도메인으로 구성된다:

- **L27 도메인**: CASK, PALS1, PALS2, MPP7, DLG1, DLG2, DLG3 등과의 상호작용을 매개하며, 막 연관 다중단백질 복합체 형성과 LIN7의 세포막 결합에 관여한다.
- **PDZ 도메인**: DLG4, GRIN2B, CDH1, CTNNB1, 이온 채널(KCNJ12/Kir2.2, KCNJ4/Kir2.3, KCNJ2/Kir2.1), 수송체(SLC6A12/BGT-1) 등과 상호작용하며, 수용체의 내포작용(endocytosis)과 재순환을 조절한다.

> 출처: [UniProt - Q9NUP9](https://www.uniprot.org/uniprot/Q9NUP9), [Cell - L27 domain review](https://www.cell.com/trends/biochemical-sciences/abstract/S0968-0004(00)01599-1)

#### 생물학적 기능

LIN7C는 극성 세포(polarized cell)에서 채널과 수용체의 비대칭적 분포를 확립하고 유지하는 데 핵심적인 역할을 수행한다. 주요 기능은 다음과 같다:

1. **세포 극성 유지**: 상피세포의 밀착연접(tight junction) 및 부착연접(adherens junction) 형성에 관여
2. **막 단백질 수송 조절**: 기저측면(basolateral) 막에 EGFR/ERBB1-4, Kir2 채널, GABA 수송체(SLC6A12) 등을 정확한 위치에 배치
3. **BLT2 수용체 수송**: LIN7C 의존적으로 BLT2(Leukotriene B4 receptor type 2)를 골지체에서 세포막으로 수송. LIN7C knockdown 시 BLT2가 골지체에 축적되며 상피 장벽 기능이 저하됨
4. **시냅스 기능**: LIN7/CASK/APBA1 삼자 복합체는 시냅스 소포 방출과 세포 부착을 연결
5. **상피 시트 형태 형성(morphogenesis of epithelial sheet)**

> 출처: [NCBI Gene - LIN7C](https://www.ncbi.nlm.nih.gov/gene/55327), [Hara et al. FASEB J. 2021](https://pubmed.ncbi.nlm.nih.gov/33481310/), [PMC12345355](https://pmc.ncbi.nlm.nih.gov/articles/PMC12345355/)

#### 발현 패턴

NCBI Gene 기준, LIN7C는 **유비쿼터스하게 발현**되며, 갑상선(RPKM 9.8), 간(RPKM 7.0) 및 25개 이상의 조직에서 발현이 확인된다.

> 출처: [NCBI Gene - LIN7C Expression](https://www.ncbi.nlm.nih.gov/gene/55327)

### 1.2 Gene Ontology (GO) 주석

| GO Category | Term |
|-------------|------|
| Molecular Function | L27 domain binding |
| Molecular Function | PDZ domain binding |
| Molecular Function | Cytoskeletal protein binding |
| Molecular Function | Protein-macromolecule adaptor activity |
| Biological Process | Morphogenesis of an epithelial sheet |
| Biological Process | Neurotransmitter secretion |
| Cellular Component | Cell-cell junction |
| Cellular Component | Cytoplasm |
| Cellular Component | Plasma membrane |

> 출처: [NCBI Gene - LIN7C](https://www.ncbi.nlm.nih.gov/gene/55327)

---

## 2. Pathway Modulation

### 2.1 Transcriptomic Level View

#### GTEx 발현 데이터

GTEx Portal에 LIN7C의 조직별 발현 데이터가 등록되어 있으며, adipose subcutaneous 및 adipose visceral (omentum) 조직에서의 발현이 확인된다. 다만, 구체적인 TPM 수치는 GTEx Portal 직접 접근을 통해 확인이 필요하다.

- **GTEx 조직 발현 페이지**: [GTEx - LIN7C](https://gtexportal.org/home/gene/LIN7C)
- **Adipose Subcutaneous**: [GTEx Tissue](https://gtexportal.org/home/tissue/Adipose_Subcutaneous)
- **Adipose Visceral Omentum**: [GTEx Tissue](https://gtexportal.org/home/tissue/Adipose_Visceral_Omentum)

#### eQTL 공동국재화(Colocalization)

소아 BMI GWAS 메타분석에서 GTEx v7 데이터를 이용한 Bayesian 공동국재화 분석 결과, LIN7C는 ADCY3, DNAJC27-AS1, CENPO, ADAM23, TFAP2B와 함께 **6개 유의미한 공동국재화 유전자좌 중 하나**로 확인되었다. 이는 소아 BMI GWAS 신호와 LIN7C의 eQTL 신호가 조직 전반에 걸쳐 공유되는 인과적 변이를 가질 가능성을 시사한다.

> 출처: [Vogelezang et al. PLoS Genet. 2020](https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1008718)

#### 비만 관련 전사체 차등 발현

LIN7C를 직접적으로 지목하여 비만 환자 대비 정상 체중 대조군에서의 차등 발현(differential expression)을 보고한 단독 연구는 현재까지 **확인되지 않음**. 대규모 통합 유전체-전사체 연구(Framingham Heart Study 기반, PMC11188121)에서 BMI 유전자좌와 전사체를 통합 분석하였으나, LIN7C는 해당 논문에서 유의미한 유전자로 보고되지 않았다.

> 근거 수준: **근거 불충분** — LIN7C의 adipose tissue에서의 BMI 관련 차등 발현에 대한 직접적 증거 부재

### 2.2 Proteomic Level View

#### 단백질 복합체

LIN7C는 다음과 같은 주요 단백질 복합체에 참여한다:

**1. MPP7-DLG1-LIN7 삼자 복합체**
- MPP7은 L27 도메인을 통해 LIN7과 결합하고, SH3-GUK 도메인을 통해 DLG1과 결합
- 이 복합체는 DLG1의 안정성과 세포 연접부(cell junction)로의 국재화를 조절
- 상피세포 극성과 밀착연접 형성을 촉진

> 출처: [Stucke et al. J Biol Chem. 2007](https://pubmed.ncbi.nlm.nih.gov/17237226/), [Bose et al. Mol Biol Cell. 2007](https://pmc.ncbi.nlm.nih.gov/articles/PMC1855022/)

**2. CASK-LIN7 복합체**
- CASK는 LIN2의 포유류 상동체로, LIN7과 진화적으로 보존된 상호작용을 수행
- 장 상피세포에서 CASK 삭제 시 LIN7C와 DLG1/Scrib 극성 복합체가 기저측면 막에서 이탈하지만, **세포 극성 자체는 유지됨**
- 이는 LIN7C가 CASK 의존적 풀과 CASK 비의존적 풀(밀착연접)로 이중 분포함을 시사

> 출처: [Gosens et al. Mol Cell Biol. 2009](https://pmc.ncbi.nlm.nih.gov/articles/PMC2770937/)

**3. Crumbs 극성 복합체**
- LIN7C는 Pals1, Patj, Crumbs3와 함께 Crumbs 극성 복합체를 구성
- 주로 신장 집합관과 원위 세뇨관에서 발현
- LIN7C 특이적 녹아웃 마우스에서 Crumbs 복합체 감소 → 신세뇨관 이형성(tubular dysplasia), 신간질 섬유화(interstitial fibrosis), 낭성 변성(cystic degeneration)

> 출처: [PMC12345355](https://pmc.ncbi.nlm.nih.gov/articles/PMC12345355/)

**4. BLT2 수용체 수송**
- LIN7C는 BLT2 수용체의 C-말단 영역과 상호작용하여 골지체에서 측면 세포막으로의 수송을 조절
- LIN7C knockdown 시 BLT2가 골지체에 축적되고 상피 장벽 기능이 저하

> 출처: [Hara et al. FASEB J. 2021](https://faseb.onlinelibrary.wiley.com/doi/10.1096/fj.202002640R)

#### 비만/대사 경로와의 단백질 수준 연관

LIN7C 단백질이 인슐린 신호전달, 지방생성(adipogenesis), 지질 대사 경로에 직접 참여한다는 단백체(proteomic) 수준의 증거는 **확인되지 않음**.

> 근거 수준: **근거 불충분**

### 2.3 Genetic Level View (Epigenetic Perspective)

#### 유전적 변이

- **ClinVar**: LIN7C에 대한 병원성(pathogenic) 또는 병원성 가능성(likely pathogenic) 변이는 현재 ClinVar에 등록되어 있지 않음
- **OMIM (612332)**: LIN7C는 OMIM에 등록되어 있으나, 특정 멘델 유전 질환과의 연관은 보고되지 않음

> 출처: [ClinVar](https://www.ncbi.nlm.nih.gov/clinvar/), [OMIM 612332](https://omim.org/entry/612332)

#### 후성유전적 조절

- **DNA 메틸화**: 구강 편평세포암(OSCC)에서 LIN7C의 CpG 섬 영역 과메틸화(hypermethylation)가 높은 빈도로 검출되었으며, 이는 LIN7C 발현 감소와 강한 상관관계를 보임. LIN7C의 과발현은 면역결핍 모델에서 다장기 전이를 억제하여 종양 억제자로서의 역할을 시사
- **지방 조직에서의 후성유전 조절**: LIN7C 특이적 메틸화 또는 히스톤 변형 데이터는 adipose tissue 맥락에서 **확인되지 않음**

> 출처: [Suda et al. Cancer Res. 2007](https://pubmed.ncbi.nlm.nih.gov/17942893/), [PMC6689875](https://pmc.ncbi.nlm.nih.gov/articles/PMC6689875/)

#### eQTL

- 11p14.1 유전자좌의 lead SNP rs962369는 BDNF 유전자의 인트론 변이로, 성인 BMI 및 허리둘레와 연관된 SNP들과 강한 연쇄불균형(LD, r² = 0.93)에 있음
- 소아 BMI GWAS에서 LIN7C eQTL 신호와의 공동국재화가 확인됨

> 출처: [Warner et al. Obesity. 2021](https://onlinelibrary.wiley.com/doi/full/10.1002/oby.23070), [Vogelezang et al. PLoS Genet. 2020](https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1008718)

---

## 3. Combined Pathway Modulation

### 통합 경로 분석

수집된 개별 경로 정보를 종합하면, LIN7C의 생물학적 역할은 주로 **세포 극성 유지 및 막 단백질 수송 조절**에 집중되어 있으며, 비만/대사 질환과의 직접적 경로 연결은 제한적이다.

#### 확인된 경로 연결점

```
LIN7C ── L27 domain ──→ CASK/MPP7/DLG1 복합체 ──→ 세포 극성/밀착연접
  │
  ├── PDZ domain ──→ 이온 채널(Kir2)/수용체(EGFR) 국재화
  │
  ├── Crumbs complex ──→ 상피 세포 극성 ──→ 신장 세뇨관 발달
  │
  └── BLT2 수송 ──→ 상피 장벽 기능
```

#### 비만과의 잠재적 연결 경로 (간접적)

1. **GWAS 유전자좌 공유**: LIN7C는 11p14.1에 위치하며, BDNF 유전자좌와 근접. BDNF는 식욕 조절 및 에너지 항상성에 중요한 역할을 수행하는 것으로 잘 알려져 있음. 그러나 이 유전자좌의 비만 연관 효과가 LIN7C 자체에 의한 것인지 BDNF에 의한 것인지는 **구분되지 않음**.

2. **eQTL 공동국재화**: 소아 BMI GWAS와 LIN7C eQTL 간의 공동국재화가 보고되었으나, 이는 LIN7C 발현 변화가 BMI에 인과적 영향을 미친다는 직접 증거는 아님.

3. **상피 장벽 기능**: LIN7C knockdown이 상피 장벽 기능을 저하시킨다는 보고가 있으나, 이는 장 상피(intestinal epithelium) 맥락이며, 지방 조직에서의 역할은 **확인되지 않음**.

> **종합 판단**: LIN7C를 비만 치료 표적으로 연결하는 통합 경로는 현재 **명확하게 구축되지 않음**. 확인된 연관은 주로 유전체 수준의 간접 증거(GWAS 공동국재화)에 의존하며, 전사체/단백체 수준에서의 기전적 연결은 부재.

---

## 4. Function in Therapeutic Indication

### LIN7C와 비만(Obesity) 간의 연관/인과 관계

#### 직접 증거

LIN7C의 발현 변화 또는 기능 변화가 비만의 발생, 진행, 또는 치료에 직접적으로 기여한다는 연구는 현재까지 **확인되지 않음**.

PubMed 검색에서 "LIN7C obesity", "LIN7C adipose", "MALS-3 obesity", "VELI3 adipose" 키워드 조합으로 직접적인 기전 연구가 검출되지 않았다.

> 근거 수준: **근거 불충분**

#### 간접 증거

| 증거 유형 | 내용 | 근거 수준 |
|-----------|------|-----------|
| GWAS 공동국재화 | 소아 BMI GWAS에서 LIN7C eQTL과 유의미한 공동국재화 확인 | 약함 (Weak) — 6개 유전자좌 중 하나로 언급, 세부 통계 미제공 |
| 유전자좌 근접성 | 11p14.1에서 BDNF와 근접, BDNF는 식욕/에너지 조절 관여 | 매우 약함 (Very weak) — 인접 유전자 효과와 구분 불가 |
| 대사 질환 연관 변이 | NCBI Gene에 "비만 및 2형 당뇨병 위험 변이와 연관" 기재 | 약함 (Weak) — 원본 연구의 세부 사항 미확인 |

#### 인과 관계 판단

LIN7C transcriptomic level 감소가 비만에 치료적 효과를 가져올 수 있다는 **인과적 근거는 현재 매우 부족**하다. 확인된 연관은 모두 유전체 수준의 간접 증거이며, LIN7C의 알려진 생물학적 기능(세포 극성, 막 수송)과 비만의 핵심 병태생리(지방 축적, 인슐린 저항성, 에너지 불균형) 간의 기전적 연결점은 확립되지 않았다.

---

## 5. Efficacy Data in Animal Disease Model and/or Patient

### 5.1 Homo sapiens (인간)

LIN7C의 발현 감소 또는 억제가 인간 비만 환자에서 치료 효과를 보인 임상 연구 또는 임상 시험은 **확인되지 않음**. ClinicalTrials.gov에서 LIN7C를 표적으로 하는 등록된 임상 시험은 존재하지 않는다.

> 근거 수준: **근거 불충분**

### 5.2 NHP (Macaca mulatta, Macaca fascicularis)

비인간 영장류에서 LIN7C knockdown/knockout과 비만 표현형 간의 관계를 조사한 연구는 **확인되지 않음**.

> 근거 수준: **근거 불충분**

### 5.3 Rodent (Mus musculus, Rattus norvegicus)

#### IMPC (International Mouse Phenotyping Consortium) 데이터

IMPC에 Lin7c (MGI:1330839) 녹아웃 마우스가 등록되어 있으나:
- **유의미한 표현형**: 0개 (0 significant phenotypes)
- **검사된 생리 시스템**: 0/24 (포괄적 표현형 분석 미완료)
- 체중, 대사, 비만 관련 파라미터의 구체적 측정 결과는 **미공개 상태**

> 출처: [IMPC - Lin7c](https://www.mousephenotype.org/data/genes/MGI:1330839)

#### 기존 녹아웃 연구

- Mals1(LIN7A) -/-, Mals2(LIN7B) -/-, Mals1 -/- Mals2 -/- 이중 녹아웃 마우스는 모두 예상 멘델비로 출생하며, 생존 가능하고, 가임하며, 야생형과 구별되지 않음 (OMIM 603380)
- **LIN7C 특이적 녹아웃 마우스**: 신장 세뇨관 이형성, 간질 섬유화, 낭성 변성이 보고되었으나, **비만 관련 표현형은 보고되지 않음**

> 출처: [OMIM 603380](https://www.omim.org/entry/603380), [PMC12345355](https://pmc.ncbi.nlm.nih.gov/articles/PMC12345355/)

#### LIN7C knockdown/siRNA 연구 (비만 맥락)

LIN7C, MALS-3, 또는 VELI3를 siRNA/shRNA/ASO/CRISPR로 knockdown하여 지방 조직 또는 비만 모델에서의 효과를 조사한 연구는 **확인되지 않음**.

> 근거 수준: **근거 불충분**

---

## 6. Severity of Disease Correlated with Transcriptomic Gene Expression Level

### 6.1 Homo sapiens (인간)

LIN7C 전사체 발현 수준과 비만 중증도(BMI, 체지방률, 내장지방량 등) 간의 상관관계를 직접적으로 보고한 연구는 **확인되지 않음**.

GTEx 데이터를 활용한 BMI-유전자 발현 상관 분석(Framingham Heart Study 기반)에서 LIN7C는 유의미한 BMI 연관 전사체로 보고되지 않았다.

> 근거 수준: **근거 불충분**

### 6.2 NHP (Macaca mulatta, Macaca fascicularis)

비인간 영장류 비만 모델에서 LIN7C 발현 수준과 질병 중증도 간의 상관관계를 보고한 연구는 **확인되지 않음**.

대규모 NHP 단일세포 전사체 아틀라스(Macaca fascicularis, 45개 조직, 100만+ 세포)가 존재하나, LIN7C 특이적 분석은 보고되지 않았다.

> 출처: [Han et al. Nature. 2022](https://www.nature.com/articles/s41586-022-04587-3)  
> 근거 수준: **근거 불충분**

### 6.3 Rodent (Mus musculus, Rattus norvegicus)

설치류 고지방 식이(HFD) 모델 또는 유전적 비만 모델에서 LIN7C 발현과 비만 중증도 간의 상관관계를 보고한 연구는 **확인되지 않음**.

> 근거 수준: **근거 불충분**

---

## 7. Safety Data by Whole or Tissue-Specific Depletion

### 7.1 Homo sapiens (인간)

- **ClinVar**: LIN7C 유전자에 대한 병원성 손실기능(loss-of-function) 변이는 현재 등록되어 있지 않음
- **OMIM**: LIN7C 결손과 연관된 인간 유전 질환은 보고되지 않음
- **임상 안전성 데이터**: LIN7C를 표적으로 하는 치료제의 인간 대상 안전성 데이터는 존재하지 않음

> 출처: [ClinVar](https://www.ncbi.nlm.nih.gov/clinvar/), [OMIM 612332](https://omim.org/entry/612332)

### 7.2 NHP (Macaca mulatta, Macaca fascicularis)

비인간 영장류에서 LIN7C 결손 또는 억제에 대한 안전성 데이터는 **확인되지 않음**.

> 근거 수준: **근거 불충분**

### 7.3 Rodent (Mus musculus, Rattus norvegicus)

#### LIN7C 녹아웃 마우스 안전성 우려 사항

| 안전성 항목 | 소견 | 출처 |
|-------------|------|------|
| **신장 독성** | LIN7C KO 마우스에서 신세뇨관 이형성, 간질 섬유화, 낭성 변성 확인. Crumbs 극성 복합체 감소로 인한 신세뇨관 상피세포의 극성 결함이 원인 | [PMC12345355](https://pmc.ncbi.nlm.nih.gov/articles/PMC12345355/) |
| **생존 가능성** | LIN7A/B 단일/이중 KO 마우스는 생존 가능, 가임. LIN7C KO 마우스의 전반적 생존율은 상기 논문에서 보고 | [OMIM 603380](https://www.omim.org/entry/603380) |
| **상피 장벽 기능** | LIN7C knockdown 시 BLT2의 골지체 축적 및 상피 장벽 기능 저하 보고 | [Hara et al. 2021](https://pubmed.ncbi.nlm.nih.gov/33481310/) |
| **장 상피 극성** | CASK 결손 시 LIN7C 국재화 이상 발생하나, 세포 극성 자체는 유지됨 (장 조직) | [Gosens et al. 2009](https://pmc.ncbi.nlm.nih.gov/articles/PMC2770937/) |

#### LIN7 패밀리 중복성(Redundancy)

| 항목 | LIN7A (MALS1) | LIN7B (MALS2) | LIN7C (MALS3) |
|------|---------------|---------------|---------------|
| 단일 KO 마우스 표현형 | 정상 | 정상 | 신장 이형성 |
| 이중 KO (A+B) | 정상, 가임 | - | - |
| 주요 발현 조직 | 사구체, 원위 세뇨관, 뇌 | 직행혈관(vasa recta), 뇌 | 집합관, 원위 세뇨관, 유비쿼터스 |
| 조직 특이적 보상 | 부분적 | 부분적 | 신장에서 비보상적 |

> LIN7A와 LIN7B는 상호 보상이 가능하나, **LIN7C는 신장에서 고유한 기능을 수행하며 다른 동형체에 의한 보상이 불충분**. 따라서 전신적(systemic) LIN7C 억제 시 신장 독성이 주요 안전성 우려 사항이 됨.

> 출처: [OMIM 603380](https://www.omim.org/entry/603380), [PMC12345355](https://pmc.ncbi.nlm.nih.gov/articles/PMC12345355/), [Molec Biol Cell - zebrafish retina](https://pubmed.ncbi.nlm.nih.gov/16109407/)

#### 기타 안전성 고려사항

- **신경 기능**: LIN7C는 시냅스 기능(GRIN2B 국재화, 시냅스 소포 방출)에 관여하므로, 전신 억제 시 신경학적 부작용 가능성을 배제할 수 없음
- **종양 억제 기능**: LIN7C 과메틸화가 OSCC에서 종양 진행/전이와 연관되며, LIN7C 과발현이 전이를 억제하므로, LIN7C 발현 감소는 이론적으로 종양 형성 또는 전이 촉진 위험을 수반할 수 있음

> 출처: [Suda et al. Cancer Res. 2007](https://pubmed.ncbi.nlm.nih.gov/17942893/)

---

## 8. Optional: GWAS, Gene Expression in Tissue, Pharmacodynamic Markers

### 8.1 Genome-Wide Association Studies (GWAS) Data

#### GWAS 연관 보고

| GWAS 연구 | LIN7C 관련 소견 | 출처 |
|-----------|----------------|------|
| 소아 BMI 메타분석 | 6개 유전자좌 중 하나로 eQTL 공동국재화 확인 (ADCY3, DNAJC27-AS1, CENPO, ADAM23, LIN7C, TFAP2B) | [Vogelezang et al. PLoS Genet. 2020](https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1008718) |
| 소아 체지방 GWAS | 11p14.1 lead SNP rs962369 (BDNF 인트론), 성인 BMI/허리둘레 연관 SNP과 강한 LD (r²=0.93) | [Warner et al. Obesity. 2021](https://onlinelibrary.wiley.com/doi/full/10.1002/oby.23070) |
| 중국인 비만/T2D GWAS | LIN7C/BDNF 근처 유전 변이가 비만 및 2형 당뇨병과 연관 | [NCBI Gene 55327](https://www.ncbi.nlm.nih.gov/gene/55327) |

> **주의**: 이 유전자좌의 비만 연관 효과가 LIN7C에 의한 것인지 인접 BDNF에 의한 것인지 **구분이 명확하지 않음**. BDNF는 시상하부에서 식욕 및 에너지 항상성 조절에 잘 확립된 역할을 가지고 있어, 11p14.1 유전자좌의 비만 연관 효과의 상당 부분이 BDNF에 기인할 가능성이 높다.

### 8.2 Gene Expression in Tissue

- **NCBI Gene**: 유비쿼터스 발현, 갑상선 (RPKM 9.8), 간 (RPKM 7.0) 및 25개 이상의 조직
- **GTEx Portal**: LIN7C 조직별 발현 데이터 제공 ([GTEx - LIN7C](https://gtexportal.org/home/gene/LIN7C))
- **Human Protein Atlas**: LIN7C 조직별 단백질 발현 데이터 접근 가능 (OMIM 참조, ENSG00000151591)
- **신장**: 집합관(collecting duct) 및 원위 세뇨관(distal tubule)에서 높은 발현
- **지방 조직**: GTEx에서 발현 확인되나, 구체적 TPM 수치는 Portal 직접 확인 필요

### 8.3 Pharmacodynamic Markers

LIN7C knockdown 효과를 모니터링할 수 있는 약력학적(PD) 바이오마커에 대한 확립된 연구는 **확인되지 않음**.

잠재적 PD 마커 후보 (이론적, 검증 필요):

| 잠재적 마커 | 근거 | 한계 |
|------------|------|------|
| BLT2 세포막 발현 수준 | LIN7C knockdown 시 BLT2 골지체 축적 보고 | 지방 조직에서 미검증 |
| DLG1 국재화 패턴 | LIN7C 복합체 파트너의 위치 변화 | 조직 생검 필요, 비침습적 측정 곤란 |
| Crumbs complex 구성요소 | LIN7C KO 시 Crumbs 복합체 감소 보고 | 신장 특이적 데이터만 존재 |

> 근거 수준: **근거 불충분** — 검증된 PD 마커 부재

---

## 9. 종합 평가

### 타당성 판단 요약

| 평가 항목 | 판정 | 비고 |
|-----------|------|------|
| **기전적 연결 (LIN7C → 비만)** | ❌ 미확립 | 세포 극성/막 수송 기능과 비만 병태생리 간 직접 연결 부재 |
| **유전체 연관 (GWAS)** | ⚠️ 간접적 | 11p14.1 BDNF 인접, eQTL 공동국재화 보고. 그러나 BDNF 효과와 구분 곤란 |
| **전사체 차등 발현** | ❌ 미확인 | 비만 환자에서 LIN7C 차등 발현 직접 보고 없음 |
| **비만 효능 데이터** | ❌ 없음 | 어떤 종에서도 LIN7C 억제의 항비만 효과 보고 없음 |
| **질병 중증도-발현 상관** | ❌ 미확인 | BMI-LIN7C 발현 상관 데이터 없음 |
| **안전성 우려** | ⚠️ 있음 | 신장 독성 (신세뇨관 이형성), 상피 장벽 기능 저하, 종양 억제 기능 상실 가능성 |
| **LIN7 패밀리 중복성** | ⚠️ 제한적 | 신장에서 LIN7C 비보상적, 전신 억제 시 안전성 위험 |

### 결론

현재 수집 가능한 과학적 증거를 종합할 때, **LIN7C transcriptomic level 감소를 통한 비만 치료 전략의 타당성은 매우 낮은 것으로 평가된다.**

**주요 근거:**

1. **기전적 연결 부재**: LIN7C의 확립된 생물학적 기능(세포 극성, 밀착연접, 막 단백질 수송)은 비만의 핵심 병태생리(에너지 불균형, 지방세포 비대/과형성, 인슐린 저항성)와 직접적인 기전적 연결이 확인되지 않는다.

2. **GWAS 증거의 한계**: 11p14.1 유전자좌에서의 BMI 연관은 보고되었으나, 이 유전자좌에는 식욕/에너지 조절에 핵심 역할을 하는 BDNF가 인접하여 LIN7C 자체의 기여를 구분하기 어렵다.

3. **전임상/임상 효능 데이터의 완전한 부재**: 어떤 종에서도 LIN7C 억제가 비만 관련 표현형에 영향을 미친다는 보고가 없다.

4. **안전성 우려**: LIN7C 전신 억제 시 신장 독성(세뇨관 이형성, 간질 섬유화), 상피 장벽 기능 저하, 잠재적 종양 촉진 위험이 있으며, LIN7 패밀리 내 중복성이 신장에서는 제한적이다.

### 권고 사항

- LIN7C를 비만 치료 표적으로 진행하기 전에, 먼저 **지방 조직(특히 피하지방 및 내장지방)에서의 LIN7C 기능적 역할**에 대한 기초 연구가 선행되어야 한다.
- 11p14.1 유전자좌의 비만 연관 효과가 LIN7C에 기인하는지 BDNF에 기인하는지를 **fine-mapping 또는 기능적 실험으로 구분**하는 것이 필요하다.
- 현재 데이터 수준에서는 다른 치료 표적으로의 전환을 권고한다.

---

## 출처 종합

### 1차 출처 (Primary Sources)
- [NCBI Gene - LIN7C (55327)](https://www.ncbi.nlm.nih.gov/gene/55327)
- [UniProt - Q9NUP9 (LIN7C, Human)](https://www.uniprot.org/uniprot/Q9NUP9)
- [OMIM - 612332 (LIN7C)](https://omim.org/entry/612332)
- [OMIM - 603380 (LIN7A)](https://www.omim.org/entry/603380)
- [GTEx Portal - LIN7C](https://gtexportal.org/home/gene/LIN7C)
- [IMPC - Lin7c (MGI:1330839)](https://www.mousephenotype.org/data/genes/MGI:1330839)
- [NCBI GTR - LIN7C](https://www.ncbi.nlm.nih.gov/gtr/genes/55327/)

### 학술 문헌 (Peer-Reviewed Literature)
- Vogelezang et al. "Novel loci for childhood body mass index and shared heritability with adult cardiometabolic traits." *PLoS Genet.* 2020. [DOI](https://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1008718)
- Warner et al. "A Genome-Wide Association Study of Childhood Body Fatness." *Obesity.* 2021. [Link](https://onlinelibrary.wiley.com/doi/full/10.1002/oby.23070)
- Gosens et al. "CASK deletion in intestinal epithelia causes mislocalization of LIN7C and the DLG1/Scrib polarity complex without affecting cell polarity." *Mol Cell Biol.* 2009. [PMC2770937](https://pmc.ncbi.nlm.nih.gov/articles/PMC2770937/)
- Stucke et al. "The stardust family protein MPP7 forms a tripartite complex with LIN7 and DLG1." *J Biol Chem.* 2007. [PubMed](https://pubmed.ncbi.nlm.nih.gov/17237226/)
- Bose et al. "The MAGUK Protein MPP7 Binds to the Polarity Protein hDlg1 and Facilitates Epithelial Tight Junction Formation." *Mol Biol Cell.* 2007. [PMC1855022](https://pmc.ncbi.nlm.nih.gov/articles/PMC1855022/)
- Hara et al. "The c-terminal region of BLT2 restricts its localization to the lateral membrane in a LIN7C-dependent manner." *FASEB J.* 2021. [PubMed](https://pubmed.ncbi.nlm.nih.gov/33481310/)
- Suda et al. "Lin-7C/VELI3/MALS-3: an essential component in metastasis of human squamous cell carcinoma." *Cancer Res.* 2007. [PubMed](https://pubmed.ncbi.nlm.nih.gov/17942893/)
- "The Physiological and Pathological Mechanisms of LIN2, LIN7, LIN10 and Their Tripartite Complex." *PMC.* [PMC12345355](https://pmc.ncbi.nlm.nih.gov/articles/PMC12345355/)
- Massari et al. "LIN7 Mediates the Recruitment of IRSp53 to Tight Junctions." *Traffic.* 2009. [Link](https://onlinelibrary.wiley.com/doi/10.1111/j.1600-0854.2008.00854.x)

### 참고 데이터베이스
- [ClinVar (NCBI)](https://www.ncbi.nlm.nih.gov/clinvar/)
- [GWAS Catalog (EBI)](https://www.ebi.ac.uk/gwas/)
- [GTEx eQTL Browser](https://www.gtexportal.org/home/eqtls/tissue?tissueName=Adipose_Subcutaneous)

---

*본 보고서는 2026년 4월 22일 기준으로 공개된 데이터베이스 및 학술 문헌을 기반으로 작성되었습니다. Blueprint Common Rule에 따라 2차 요약 자료(GeneCards 등)는 사용하지 않았으며, 확인되지 않은 내용에 대해서는 "근거 불충분"으로 명시하였습니다.*
