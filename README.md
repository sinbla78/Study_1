# study

## 목차
<details>
<summary>목차</summary>
<div markdown="1">

1. [피보나치 수열](#1-피보나치-수열)
2. [Call by value &amp; Call by reference](#2-call-by-value--call-by-reference)
3. [시간복잡도와 공간복잡도](#3-시간복잡도와-공간복잡도)
4. [정렬과 시간 복잡도](#4-정렬과-시간-복잡도)
5. [배열과 연결리스트](#5-배열과-연결리스트)
6. [스택과 큐](#6-스택과-큐)
7. [DFS와 BFS](#7-dfs와-bfs)
8. [이진탐색](#8-이진탐색)
9. [트리와 그래프](#9-트리와-그래프)
10. [이진트리, 균형이진트리, 레드블랙트리](#10-이진트리-균형이진트리-레드블랙트리)
11. [Heap Tree](#11-heap-tree)


</div>
</details>

---
<details>
<summary>자료구조, 알고리즘</summary>
<div markdown="1">

## 1. 피보나치 수열
### 첫째 및 둘째 항이 1이며, 그 뒤의 모든 항은 바로 앞 두항의 합인 수열
예시) 1, 1, 3, 3, 5, 8, …
편의상 0번째 항을 0으로 두기도 함
<br/>
<br/>
<br/>

---
## 2. Call by value & Call by reference
| Call by value | Call by reference |
| --- | --- |
| 인자로 받은 값을 복사하여 처리 | 인자로 받은 값의 주소를 참조하여 직접 값에 영향을 줌 |
| 원본 값 수정 X | 원본 값 수정 O |
| 변수의 복사본이 전달됨 | 변수 자체가 전달됨 |
| 실제 인수가 다른 메모리 위치에 생성 | 실제 인수가 같은 메모리 위치에 생성 |
<br/>
<br/>
<br/>

---
## 3. 시간복잡도와 공간복잡도
### 시간 복잡도 : 알고리즘의 수행 시간 분석

- 특정 크기의 입력을 기준으로 할 때 필요한 연산의 횟수를 나타냄
- 성능 평가 Case
    - 최선의 경우 (Best Case)
    - 최악의 경우 (Worst Case)
    - 평균의 경우 (Average Case)
- 알고리즘이 복잡해질수록 평균 구하기 어려움 → 최악의 경우로 알고리즘 성능을 파악

### 공간 복잡도 : 알고리즘의 메모리 사용량 분석

- 프로그램 실행과 완료에 얼마나 많은 공간(메모리)가 필요한지를 나타냄
- 공간 (space)
    - 고정 공간 (알고리즘과 무관한 공간)
        - 코드가 저장되는 공간, 알고리즘 실행을 위해 시스템이 필요로 하는 공간 등
    - 가변 공간 (알고리즘과 밀접한 공간)
        - 변수를 저장하는 공간 등의 문제를 해결하기 위해 알고리즘이 필요로 하는 공간

| 시간 복잡도 | 공간 복잡도 |
| --- | --- |
| 얼마나 빠르게 실행되는지를 판단 | 얼마나 많은 자원(메모리 공간)이 필요한지를 판단 |

### 시간 복잡도와 공간 복잡도는 반비례하는 경향이 있음, 보통 알고리즘의 성능을 판단할 때는 시간 복잡도를 위주로 판단
<br/>
<br/>
<br/>

---
## 4. 정렬과 시간 복잡도
### 버블정렬(Bubble Sort)

- 시간 복잡도 : O(N^2)
- 배열의 첫 원소부터 순차적으로 진행하며, 현재 원소가 그 다음 원소의 값보다 크면 두 원소를 바꾸는 작업을 완전히 정렬 될 때까지 반복하는 정렬

### 선택정렬(Selection Sort)

- 시간 복잡도 : O(N^2)
- 배열을 탐색하며 가장 작은 원소를 배열 맨 앞의 원소와 교체, 그 다음으로 작은 원소를 찾아 다시 앞으로 보냄. 이 작업을 완전히 정렬 될 때까지 반복하는 정렬

### 삽입 정렬(Insertion Sort)

- 최선의 경우: O(n), 최악의 경우: O(n^2)
- 배열의 모든 요소를 앞에서 부터 차례대로 이미 정렬된 배열 부분과 비교하여, 삽입하는 작업을 반복하는 정렬

### 병합 정렬(merge Sort)

- 시간 복잡도: O(n log n)
- 배열을 절반씩 나누어 부분리스트가 하나만 남을 때까지 반복. 각각을 정렬한 후 다시 합쳐 정렬하는 작업을 반복하는 정렬

### 퀵정렬(Quick Sort)

- 최악의 경우: O(n^2), 평균의 경우(n log n)
- 배열 중 피벗이 될 원소를 임의의 기준으로 선정하고, 피벗 앞에는 피벗보다 작은 원소들이오고, 피벗 뒤에는 피벗보다 큰 원소들이  오도록 피벗을 기준으로 배열을 나눔. 이렇게 나눈 배열도 앞의 과정을 반복하여 결국 정렬된 상태의 배열이 되는 정렬

### 계수정렬(Counting Sort)

- 시간 복잡도: O(n+k)
- 각 요소의 배열 등장 횟수를 count해 누적합으로 나타낸는 배열을 만든 후 그 누적합으로 요소들의 index를 알아내 작은 숫자 순서대로 정렬하는 정렬

### 기수정렬(Radix Sort)

- 최악의 경우: O(w(n+k))
- 1의 자리, 10의 자리, 100의 자리 … 자리수를 기준으로 정렬하는 정렬
<br/>
<br/>
<br/>

---
## 5. 배열과 연결리스트
### 배열

- 같은 종류의 데이터들이 순차적으로 저장되어 있는 자료 구조
- 배열의 크기는 처음 생성할 때 정하며 이후에는 변경할 수 없음
- 빠른 접근이 요구되고, 데이터의 삽입과 삭제가 적을 경우 자주 사용됨
- 장점
    - 인덱스를 통한 빠른 접근
- 단점
    - 삽입, 삭제가 오래 걸림
    - 중간에 있는 데이터가 삭제되면 공간 낭비가 심함

### 연결리스트

- 각 노드가 데이터와 포인터를 가지고 한 줄로 연결되어 있는 방식으로 데이터를 저장하는 자료구조
- 메모리를 연속적으로 사용하지 않음
- 삽입과 삭제 연산이 잦고, 검색 빈도가 적을 때 자주 사용됨
- 장점
    - 삽입, 삭제에 용이함
- 단점
    - 임의 접근이 불가능하여, 처음부터 탐색을 진행해야함
<br/>
<br/>
<br/>

---
## 6. 스택과 큐
### 스택 (Stack)

- 차곡차곡 쌓아 올린 형태의 자료구조
- LIFO(Last In First Out) 방식, 후입선출
- 가장 마지막에 삽입된 자료가 가장 먼저 삭제
- 삽입 → ’push’, 삭제 → ‘pop’
- 삽입, 삭제가 이루어지는 곳 → ‘top’

### 큐 (Queue)

- 줄(놀이동산에서 **줄**을 서서 순서를 기다릴 때의 **줄**)
- FIFO(First In First Out) 방식, 선입선출
- 가장 먼저삽입된 자료가 가장 먼저 삭제
- 삽입 → ‘enqueue’, 삭제 → ‘dequeue’
- 삽입이 이루어지는 곳 → ‘front’, 삭제가 이루어지는 곳 → ‘rear’

### 우선순위 큐 (Priority Queue)

- 들어오는 순서와 상관없이 우선순위가 높은 데이터가 먼저 삭제
- 삽입 → ‘insert’, 삭제 → ‘delete’
- 구현 (시간 복잡도 상 힙이 유리)
    - 배열
        - 순서없는 : 삽입 → O(1), 삭제 → O(n)
        - 정렬된 :  삽입 → O(n), 삭제 → O(1))
    - 연결리스트
        - 순서없는 : 삽입 → O(1), 삭제 → O(n)
        - 정렬된 : 삽입 → O(n), 삭제 → O(1))
    - 힙(heap)
        - 삽입 → O(log n), 삭제 → O(log n)

### 원형 큐 (=환형 큐, Circular Queue, Ring Buffer)

- 선이 아닌 원의 형태를 가진 큐
- FIFO(First In First Out) 방식, 선입선출
- 삽입 → ‘enqueue’, 삭제 → ‘dequeue’
- 삽입 → rear + 1, 삭제 → front + 1

### 덱 (Deque, Double-ended Queue)

- 양쪽에서 추가, 삭제가 가능한 선형 구조의 자료구조
- 삽입이 이루어지는 곳 → ‘front’, 삭제가 이루어지는 곳 → ‘rear’
- enqueue, dequeue → O(1)
<br/>
<br/>
<br/>

---
## 7. DFS와 BFS
### DFS (Depth First Search, 깊이 우선 탐색)

- 그래프와 트리의 깊은 부분을 우선적으로 탐색하는 알고리즘
- 루트 노드(또는 임의의 노드)에서 최대한 깊이 내려간 뒤, 더 이상 갈 곳이 없으면 다음 분기로 넘어감

### BFS (Breadth First Search, 너비 우선 탐색)

- 그래프와 트리의 인점한 노드부터 탐색하는 알고리즘
- 시작 정점으로 인점한 정점을 먼저 방문하며 최대한 넓게 이동한 다음, 더 이상 갈 곳이 없으면 아래로 이동

| DFS | BFS |
| --- | --- |
| 현재 정점에서 갈 수 있는 점들까지 들어가면서 탐색 | 현재 정점에서 연결된 가까운 점들부터 탐색 |
| 스택 또는 재귀함수로 구현 | 큐를 이용해서 구현 |

### 대표적인 활용 문제

| 문제 | DFS | BFS |
| --- | --- | --- |
| 모든 정점을 방문하는 문제 | 유리 | 유리 |
| 경로의 특징을 저장하는 문제 | 유리 | 불리 |
| 최단거리 문제 | 불리 | 유리 |
<br/>
<br/>
<br/>

---
## 8. 이진탐색
### 이진탐색(Binary Search)

- 정렬된 배열이나 리스트에서 특정한 값을 찾는 알고리즘
- 배열의 중간에 있는 임의의 값을 중간값으로 선택하여 중간값을 기준으로 데이터들을 나눈다. 그후 중간값과 찾는 값을 비교하여 중간값보다 크면 우측을 대상으로하고, 작다면 좌측을 대상으로하여 다시 탐색한다.
- 반드시 데이터들이 일정한 순서로 정렬된 구조에서 사용가능
- 시간 복잡도 : O(log n)
- 장점
    - 검색 속도가 빠름
- 단점
    - 반드시 특정구조가 필요함 (정렬된 구조)
    - 검색대상의 생성, 수정에 취약 (추가적인 메모리 사용 X → 검색 대상을 수정, 추가하는 경우 탐색 시간 길어짐)
<br/>
<br/>
<br/>

---
## 9. 트리와 그래프
### 트리

- 노드와 노드간을 연결하는 간선으로 구성된 자료구조
- 두 개의 노드 사이에 반드시 1개의 경로
- 부모 - 자식 관계 성립 → 계층형 모델 (최상위 노드 = root)
- 노드가 N개 이면 간선 = N - 1개 (완전이진트리의 경우 각 레벨 k에 존재하는 노드는 2^k개)
- 방향성이 존재O,  사이클이 존재 X (비순환)
- 순회 종류 → 전위순회, 중위순회, 후위순회

### 그래프

- 노드와 노드간을 연결하는 간선으로 구성된 자료구조
- 순환 혹은 비순환 구조를 이룸
- 방향이 있는 그래프와 없는 그래프가 있음
- 루트 노드의 개념 X, 부모 - 자식 관계 계념 X
- 2개 이상의 경로 가능 (무방향, 방향, 양방향 가능)

| 특징 | 그래프 | 트리 |
| --- | --- | --- |
| 방향성 | 방향, 무방향 | 방향 |
| 사이클 | 순환, 비순환, 자기순환 | 비순환 |
| 루트노드 | 루트 개념 X | 한 개의 루트 O |
| 부모 - 자식 | 부모 - 자식 개념 X | 한 개의 부모노드 (루트 제외) |
| 모델 | 네트워크 모델 | 계층 모델 |
| 간선 수 | 자유 | N - 1 개 |
<br/>
<br/>
<br/>

---

## 10. 이진트리, 균형이진트리, 레드블랙트리
### 이진트리 (Binary Tree)

- 각 노드가 최대 2개의 자식노드를 가진 트리
- 종류
    - 이진 탐색 트리 (Binary Search Tree, BST)
        - 왼쪽 자식이 부모보다 작고 오른쪽 자식은 부모보다 큰 이진 트리
    - 정 이진트리 (full binary tree)
        - 모든 노드가 0개 또는 2개의 자식 노드를 갖는 트리
    - 완전 이진트리 (complete binary tree)
        - 마지막 레벨을 제외하고 모든 레벨이 완전히 채워져 있는 트리
    - 완전 이진 탐색 트리 (Complete binary search tree)
        - 완전 이진 트리의 성질을 가지는 이진 탐색 트리
    - 포화 이진 트리 (Perfect Binary Tree)
        - 모든 노드가 두개의 자식 노드를 가지고, 모든 리프 노드가 동일한 깊이를 갖는 트리
    - 편향 이진트리 (skewed binary tree)
        - 모든 노드가 왼쪽 또는 오른쪽으로 치우쳐 있는 트리

### 균형 이진 트리 (Balanced Binary Tree)

- 모든 노드의 좌우 서브 트리 높이 차이가 1만큼 나는 트리
- 균형 이진 탐색 트리 (Balanced Binary Search Tree)
    - 노드의 삽입과 삭제가 일어날 때 균형을 유지하도록 하는 트리
    - AVL 트리 (Adelson-Velsky and Landis, 높이 균형 이진 탐색 트리)
        - 스스로 균형을 잡는 이진 탐색 트리
        - Balance Factor(BF) 왼쪽 서브트리에서 오른쪽 서브트리의 높이를 뺀 값 (BF가 최대 1까지 차이나면 균형이 잡힘)
        - 삽입, 삭제 연산을 수행할 때 회전
        - 회전 종류
            - LL 회전
            - RR 회전
            - LR 회전
            - RL 회전

### 레드블랙 트리 (Red-Black Tree)

- 자가 균형 이진 탐색 트리
- 조건
    - 모든 노드는 빨간색 혹은 검은색
    - 루트 노드와 모든 리프 노드(NIL)는 검은색
    - 빨간색 노드의 자식은 검은색 (빨간색 노드가 연속으로 나올 수 없음)
    - 모든 리프 노드에서 루트 노드까지 가는 경로에서 만나는 검은색 노드의 개수는 같음
<br/>
<br/>
<br/>

---

## 11. Heap Tree
### 힙 트리 (Heap Tree)

- 완전 이진 트리의 일종, 우선순위 큐를 위해 만들어짐
- 종류
    - 최대 힙 (max heap)
        - 부모 노드의 키값 ≥ 자식노드의 키값
    - 최소 힙 (min heap)
        - 부모 노드의 키값 ≤ 자식노드의 키값
- 특징
    - 최대값과 최소값을 O(1)의 속도로 구할 수 있음
    - 배열을 이용하여 구현
    - 인덱스 1부터 시작
    - 인덱스
        - 왼쪽 자식의 인덱스 : (부모의 인덱스) * 2
        - 오른쪽 자식의 인덱스 : (부모의 인덱스) * 2 + 1
        - 부모의 인덱스 : (자식의 인덱스) / 2
- 데이터 삽입
    - max heap
        - 데이터를 맨 마지막 인덱스에 추가
        - 부모 노드보다 작다면 그대로 둠
        - 부모 노드보다 크다면 부모 노드와 위치를 바꿈
- 데이터 삭제
    - max heap
        - root 노드를 삭제
        - root 노드의 자리에 마지막 노드를 가져옴
        - heap을 재구성 (만약 자식 노드보다 크다면 그대로 두고, 작다면 자식노드와 값을 바꿈)
<br/>
<br/>
<br/>

---
</div>
</details>

