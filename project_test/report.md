# Bioinformatics 분야에서 Claude를 활용한 최근 연구 문헌 조사

> 작성일: 2026-04-14

---

## 개요

본 보고서는 Bioinformatics(생물정보학) 분야에서 Anthropic의 대규모 언어 모델(LLM)인 Claude를 활용하거나 평가한 최근 학술 문헌을 조사하여 정리한 것이다. 2025년 이후 발표된 주요 논문 3편을 선정하여 소개한다.

---

## 1. BixBench: a Comprehensive Benchmark for LLM-based Agents in Computational Biology

### 서지 정보

| 항목 | 내용 |
|------|------|
| **저자** | Ludovico Mitchener, Jon M Laurent, Alex Andonian, Benjamin Tenmann, Siddharth Narayanan, Geemi P Wellawatte, Andrew White, Lorenzo Sani, Samuel G Rodriques |
| **발표일** | 2025년 2월 28일 (arXiv), 2025년 10월 8일 (v3 개정) |
| **출처** | arXiv:2503.00096 |
| **기관** | FutureHouse, ScienceMachine |
| **링크** | [arXiv](https://arxiv.org/abs/2503.00096) / [GitHub](https://github.com/Future-House/BixBench) |

### 연구 내용

BixBench는 LLM 기반 에이전트의 전산 생물학(computational biology) 수행 능력을 평가하기 위해 설계된 포괄적 벤치마크이다. 53개의 실제 생물학적 데이터 분석 시나리오와 296개의 개방형 질문으로 구성되어 있으며, 생물정보학 데이터셋 탐색, 다단계 분석 수행, 결과 해석 능력을 측정한다.

### Claude 관련 결과

- **Claude 3.5 Sonnet**과 GPT-4o 두 가지 프론티어 모델을 커스텀 에이전트 프레임워크를 통해 평가
- 개방형 답변 방식에서 Claude 3.5 Sonnet은 **17%의 정확도**를 달성 (GPT-4o는 9%)
- 객관식 방식에서는 두 모델 모두 무작위 선택 수준의 성능을 보임
- 현재 프론티어 모델이 엄밀한 생물정보학 분석에는 여전히 상당한 한계가 있음을 시사

### 의의

실제 생물정보학 업무 환경을 반영한 최초의 대규모 벤치마크로서, LLM 에이전트 개발의 방향성을 제시하는 중요한 연구이다. Claude가 GPT-4o 대비 우수한 성능을 보였으나, 절대적 정확도는 아직 낮아 향후 개선이 필요함을 보여준다.

---

## 2. Benchmarking Large Language Models for Genomic Knowledge with GeneTuring

### 서지 정보

| 항목 | 내용 |
|------|------|
| **저자** | Xinyi Shang, Xu Liao, Zhicheng Ji, Wenpin Hou |
| **발표일** | 2025년 9월 23일 |
| **저널** | Briefings in Bioinformatics, Volume 26, Issue 5 |
| **DOI** | 10.1093/bib/bbaf492 |
| **링크** | [Oxford Academic](https://academic.oup.com/bib/article/26/5/bbaf492/8261762) |

### 연구 내용

GeneTuring은 LLM의 유전체학(genomics) 지식을 평가하기 위한 벤치마크로, 16개 유전체학 과제에 걸쳐 1,600개의 큐레이션된 질문으로 구성되어 있다. GPT-4o, Claude 3.5, Gemini Advanced, BioGPT 등 10가지 LLM 구성을 대상으로 총 48,000개의 답변을 수작업으로 평가하였다.

### Claude 관련 결과

- Claude 3.5는 전체 성능에서 **3위**를 기록 (1위: NCBI API를 통합한 커스텀 GPT-4o인 SeqSnap)
- Claude 3.5, GPT-4o, Gemini Advanced는 모든 질문에 대해 일관되게 관련성 있는 답변을 제공
- **아미노산 번역(Amino Acid Translation)** 과제에서는 테스트된 모델 중 최고 성능
- **DNA 정렬(Alignment)** 과제에서는 유전체 데이터베이스 접근 부재로 거의 0%에 가까운 정확도
- 생물정보학 코드 생성에서는 비일관적인 신뢰성을 보임
- AI 환각(hallucination) 현상이 일부 과제에서 관찰됨

### 의의

수천 명의 인간 참가자 대비 LLM의 성능을 체계적으로 비교한 연구로, Claude를 포함한 범용 LLM이 유전체학에서 유망한 가능성을 보이면서도 도메인 특화 정밀도가 부족함을 입증하였다. LLM과 도메인 특화 도구(NCBI API 등)의 통합이 성능 향상의 핵심임을 제시한다.

---

## 3. Out-of-the-box Bioinformatics Capabilities of Large Language Models (LLMs)

### 서지 정보

| 항목 | 내용 |
|------|------|
| **저자** | Varsha Rajesh, Geoffrey H Siwo |
| **발표일** | 2025년 8월 27일 |
| **출처** | bioRxiv (프리프린트) |
| **DOI** | 10.1101/2025.08.22.671610 |
| **PMCID** | PMC12407700 |
| **링크** | [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC12407700/) |

### 연구 내용

교육용 생물정보학 플랫폼인 Rosalind의 104개 문제를 활용하여 범용 LLM(GPT-3.5, Llama-3-70B, GPT-4o)의 생물정보학 문제 해결 능력을 평가한 연구이다. 문제당 110~68,760명의 인간 참가자 응답과 비교 분석하였다.

### 주요 결과

- GPT-3.5가 58%(59/104)로 최고 정확도를 달성
- Llama-3-70B와 GPT-4o는 각각 47%(49/104) 정답
- 전체 문제의 71%가 최소 하나의 LLM에 의해 정답 처리
- **DNA 분석** 과제에서 GPT-3.5는 100% 정확도를 기록
- **유전체 조립(Genome Assembly)** 및 **모티프 탐색(Motif Finding)** 과제에서는 저조한 성능

### Claude와의 관련성

이 연구는 Claude를 직접 평가하지는 않았으나, Claude를 포함한 범용 LLM이 전문적 스크립팅 없이도 생물정보학 문제를 해결할 수 있는 가능성을 논의하며, 향후 Claude 등의 모델로 확장 평가가 필요함을 제안하고 있다. 범용 LLM의 생물정보학 기초 역량에 대한 중요한 기준선(baseline)을 제공한다는 점에서 의의가 있다.

---

## 종합 분석

### 현재 수준

| 벤치마크 | Claude 성능 | 비교 대상 대비 |
|----------|-------------|---------------|
| BixBench (전산 생물학) | 17% 정확도 | GPT-4o(9%) 대비 우수 |
| GeneTuring (유전체학) | 전체 3위 | 아미노산 번역 최고, DNA 정렬 최저 |

### 주요 시사점

1. **강점**: Claude는 생물학적 추론, 텍스트 기반 유전체학 질문, 아미노산 서열 분석 등에서 경쟁력 있는 성능을 보인다.
2. **한계**: 유전체 데이터베이스 접근이 필요한 과제(DNA 정렬 등)와 복잡한 다단계 분석에서는 여전히 한계가 뚜렷하다.
3. **발전 방향**: 2025년 10월 Anthropic이 출시한 Claude for Life Sciences는 PubMed 커넥터, single-cell-rna-qc 스킬, 10x Genomics 커넥터 등을 통해 이러한 한계를 보완하려는 시도이다. 최신 모델인 Sonnet 4.5는 BixBench에서 이전 모델 대비 향상된 성능을 보이고 있다.
4. **통합 접근의 중요성**: GeneTuring 연구가 보여주듯, LLM 단독보다 도메인 특화 도구(NCBI API 등)와의 통합이 성능을 크게 향상시킨다.

---

## 참고 문헌

1. Mitchener, L., Laurent, J.M., Andonian, A., et al. (2025). "BixBench: a Comprehensive Benchmark for LLM-based Agents in Computational Biology." *arXiv:2503.00096*. [https://arxiv.org/abs/2503.00096](https://arxiv.org/abs/2503.00096)
2. Shang, X., Liao, X., Ji, Z., & Hou, W. (2025). "Benchmarking large language models for genomic knowledge with GeneTuring." *Briefings in Bioinformatics*, 26(5), bbaf492. [https://doi.org/10.1093/bib/bbaf492](https://doi.org/10.1093/bib/bbaf492)
3. Rajesh, V. & Siwo, G.H. (2025). "Out-of-the-box bioinformatics capabilities of large language models (LLMs)." *bioRxiv*. [https://doi.org/10.1101/2025.08.22.671610](https://doi.org/10.1101/2025.08.22.671610)
