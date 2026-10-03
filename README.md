# Assignment 05 — JavaScript CRUD Service

## Deployment

- **Vercel URL**:https://2026-ossweek5.vercel.app/

---

## Key Learning

1. **confirm()**: 삭제 전 사용자에게 확인을 요청하는 방법을 배웠다. `confirm()`은 확인을 누르면 `true`, 취소를 누르면 `false`를 반환하여 `if`문으로 분기 처리할 수 있다.
2. **Validation**: 입력값의 필수 여부, 길이, 이메일 형식 등을 `if`문으로 하나씩 검사하는 방법을 배웠다. 조건에 맞지 않으면 `alert()`로 안내하고 `return`으로 함수를 중단한다.
3. **JavaScript Array와 DOM 연동**: 데이터를 JavaScript 배열에서 관리하고, 변경이 생길 때마다 `displayFriends()`를 호출해 화면을 갱신하는 패턴을 익혔다.

---

## CRUD Service

### 구현한 서비스
친구 관리 서비스 (Friend Management)

### 데이터 Field

| Field | 설명 |
|---|---|
| name | 이름 |
| 관계 | 친구 / 가족 등 관계 |
| 전화번호 | 연락처 |
| 이메일 | 이메일 주소 |
| 생일 | 생년월일 |

### 구현 방법

| 기능 | 구현 방법 |
|---|---|
| Create | 폼 입력 후 [추가] 버튼 클릭 → Validation 통과 시 배열에 추가 → 화면 갱신 |
| Read | 페이지 로드 시 `displayFriends()` 호출 → 배열 데이터를 Table로 출력 |
| Update | [수정] 버튼 클릭 → 기존 데이터를 폼에 표시 → 수정 후 [추가] 버튼으로 저장 |
| Delete | [삭제] 버튼 클릭 → `confirm()` 확인 → 배열에서 제거 → 화면 갱신 |

---

## JavaScript

| 기능 | 설명 |
|---|---|
| `querySelector()` | ID로 DOM 요소를 선택할 때 사용 |
| `Array.push()` | 새 데이터를 배열 끝에 추가 |
| `Array.splice()` | 배열에서 특정 위치의 데이터를 삭제 |
| `forEach()` | 배열의 각 항목을 순회하며 HTML 생성 |
| `innerHTML` | 생성한 HTML 문자열을 DOM에 반영 |
| `displayFriends()` | 배열 데이터를 Table로 렌더링하는 함수 |

---

## AI / Search Usage

- **사용한 도구**: 제미나이 (Gemini)
- **어떤 문제를 해결하기 위해 사용했는지**: Validation을 어떻게 구현해야 할지 막막해서 어떤 항목들이 있는지 알아보기 위해 사용했다.
- **실제 코드에 어떻게 적용했는지**: 필수값 확인(`if(!name)`), 길이 확인(`name.length < 2`), 이메일 형식 확인(`email.includes("@")`) 등을 `if`문으로 각각 적용했다.
- **새롭게 이해한 내용**: Validation은 조건마다 `if`문을 따로 작성하고 통과하지 못하면 `return`으로 즉시 중단하는 방식으로 구현한다는 것을 이해했다.

---

## Problem & Solution

**문제**: Validation을 어떻게 구현해야 할지 막막했다. 어떤 조건을 검사해야 하는지, 코드를 어떻게 작성해야 하는지 처음에는 감이 잡히지 않았다.

**해결**: 필수값, 길이, 이메일 형식 등 검사할 항목을 먼저 목록으로 정리하고, 요소 하나하나에 `if`문을 차근차근 적용해 나갔다. 조건에 맞지 않으면 `alert()`로 안내하고 `return`으로 함수를 중단하는 패턴을 반복 적용하면서 자연스럽게 이해하게 됐다.

---

## Reflection

`confirm()`과 Validation을 처음 직접 구현해봤는데, 단순한 `if`문의 조합으로 사용자 입력을 검사하고 피드백을 줄 수 있다는 점이 생각보다 직관적이었다. 특히 Validation은 막막하게 느껴졌지만 조건을 하나씩 나눠서 적용하니 어렵지 않았다. 앞으로 더 복잡한 조건도 적용해보고 싶다.

