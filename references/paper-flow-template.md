# Notion paper workspace template

The HQ must follow a recognizable paper structure and contain enough content to draft the manuscript from Notion alone. Adapt section names to the venue and project.

## Opening

### 한눈에 보는 논문

Explain the problem, research question, current answer, and research status in two to four short paragraphs. Do not show paths, IDs, or operational metadata.

## Paper sections

### 제목 후보

Store the current title and meaningful alternatives.

### 초록

Maintain a living abstract with motivation, gap, approach, main result or unmeasured placeholder, and contribution. Never write a result that does not exist.

### 1. 서론

Write the motivation, concrete problem, missing knowledge, research question, approach preview, contribution, and paragraph order.

### 2. 배경 및 관련 연구

Explain the necessary concepts and organize related work by the distinctions the paper needs. Attach literature-check projects to unsupported comparisons or missing citations.

### 3. 연구 질문과 핵심 설명

Define the objects, the suspected mechanism, competing explanations, and falsifiable predictions in plain language before formal notation.

### 4. 연구 설계 및 방법

Describe the model, setting, interventions, controls, evaluation, and validity conditions. Link design-validation or proof projects where needed.

### 5. 실험

Present experiments in argument order, not job order. For each, explain which uncertainty it resolves and link the Research Projects page.

### 6. 결과

Keep planned result sentences, tables, and figures. Mark unmeasured cells explicitly. When results arrive, separate observation from interpretation.

### 7. 논의

State what the findings mean, alternative explanations, relation to prior work, and practical implications.

### 8. 한계

Write scope, threats to validity, missing generalization, and claims the paper will not make.

### 9. 결론

Maintain the strongest defensible answer and the next decisive evidence. The conclusion must agree with current project status.

## Embed research projects in context

Immediately after a statement that needs work, add:

~~~markdown
**이 내용을 뒷받침할 연구 프로젝트:** <mention-page url="PROJECT_PAGE_URL"/> — 무엇을 확인해야 이 문장을 쓸 수 있는지 설명한다.
~~~

For available results, add:

~~~markdown
**현재 확인된 내용:** 사람이 이해할 수 있는 관찰 요약.

**논문에 반영할 내용:** 어느 문장, 표, 그림, 또는 결론이 어떻게 바뀌는지.
~~~

## State uncertainty in the paper

- `아직 실험하지 않았다.`
- `실행 경로만 확인했고 논문 결과는 없다.`
- `현재 근거로는 두 설명을 구분할 수 없다.`
- `이 문장에는 인용 또는 추가 분석이 필요하다.`

Do not hide these states only in a database.

## Research operations

Only after all paper sections, show compact views for:

- 지금 진행할 연구 프로젝트;
- 최근 Daily Progress;
- 다시 검토할 연구 결정.

Keep optional claim and evidence indexes in a collapsed `Agent / Audit Index` section.
