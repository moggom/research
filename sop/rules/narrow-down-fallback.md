# Narrow-Down 범위 확장 절차 (Narrow-Down Fallback)

## 목적

"조사 대상 범위 (narrow-down)"에서 유효한 데이터가 확보되지 않을 때, 단계적으로 검색 범위를 확장하는 절차를 정의한다.

---

## 1. Narrow-Down의 의미 명확화

Blueprint의 "조사 대상 범위 (narrow-down)"은 **제한이 아닌 우선순위**를 의미한다.

- **1순위**: Narrow-down으로 지정된 조직/기관의 데이터를 우선 검색하고 보고
- **2순위**: 1순위에서 데이터가 부족한 경우, 관련 조직으로 확장
- **3순위**: 2순위에서도 부족한 경우, 조직 비특이적(전신) 데이터 포함

---

## 2. 단계적 확장 절차

### Step 1: 지정 조직 검색 (Primary Scope)

Blueprint에 명시된 narrow-down 조직에서 검색을 수행한다.

```
예: adipose_subcutaneous, adipose_visceral_omentum
```

- 해당 조직 특이적 데이터가 **1건 이상** 존재하면 → 해당 데이터를 우선 보고
- 해당 조직 데이터가 **0건**이면 → Step 2로 진행

### Step 2: 관련 조직으로 확장 (Extended Scope)

대상 질병과 생물학적으로 관련된 조직으로 검색을 확장한다.

확장 조직의 선정 기준:
- 대상 질병의 병태생리에 직접 관여하는 조직
- 대상 유전자가 높은 발현을 보이는 조직
- 대상 조직과 발생학적/기능적으로 연관된 조직

```
예 (Obesity의 경우):
  Step 1: adipose_subcutaneous, adipose_visceral_omentum
  Step 2: liver, skeletal_muscle, pancreas, hypothalamus
```

- 확장 조직에서 데이터가 **1건 이상** 존재하면 → Step 1 결과와 구분하여 보고
- 확장 조직에서도 **0건**이면 → Step 3로 진행

### Step 3: 조직 비특이적 검색 (General Scope)

조직 제한 없이 전체 맥락에서 검색을 수행한다.

- 이 단계의 결과는 "조직 비특이적 데이터"로 명시하여 보고
- Narrow-down 조직에서의 적용 가능성에 대해 추론하지 않고 사실만 보고

---

## 3. 보고 형식

범위 확장이 발생한 경우, 보고서에 아래와 같이 명시한다.

```markdown
### [항목명]

#### Primary Scope (adipose_subcutaneous, adipose_visceral_omentum)
> 해당 조직에서의 직접 데이터: 없음

#### Extended Scope (liver, skeletal_muscle, hypothalamus)
> (확장 조직에서 발견된 데이터 기술)
> **주의**: 이 데이터는 지정 조직(adipose)이 아닌 {조직명}에서 얻어진 결과임

#### General Scope
> (조직 비특이적 데이터 기술)
> **주의**: 조직 특이적 맥락 없이 해석에 주의 필요
```

---

## 4. 확장 조직 매핑 (질병별 참고)

자주 사용되는 질병에 대해 Step 2 확장 조직을 사전 정의한다.

| 질병 | Primary (예시) | Extended |
|------|---------------|----------|
| Obesity | adipose (SC, visceral) | liver, skeletal_muscle, pancreas, hypothalamus, intestine |
| Type 2 Diabetes | pancreatic_islet | liver, skeletal_muscle, adipose, kidney |
| NAFLD/NASH | liver | adipose, intestine, portal_vein |
| Cardiovascular | heart, coronary_artery | aorta, liver, adipose, kidney |
| Neurodegeneration | brain (region-specific) | spinal_cord, CSF, peripheral_nerve |

이 매핑은 참고용이며, 대상 유전자의 발현 패턴에 따라 조정할 수 있다.
