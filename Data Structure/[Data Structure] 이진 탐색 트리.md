## 이진 탐색 트리 BST(Binary Search Tree)

**이진 탐색 트리의 목적은?**

-> 이진 탐색 + 연결 리스트

- 이진 탐색
  - 탐색에 소요되는 시간 복잡도는 O(logN)
  - 하지만 삽입, 삭제가 불가능.
- 연결 리스트
  - 삽입, 삭제의 시간 복잡도는 O(1)
  -  하지만 탐색하는 시간 복잡도는 O(N)
- 이 두 가지를 합하여 장점을 모두 얻기 위해 고안된 것이 `이진 탐색 트리`
- 즉, 효율적인 탐색 능력을 가지고 자료의 삽입, 삭제도 가능하게 만드는 것이다.



### [특징]

- 이진 트리의 일종으로 이진 탐색 트리에는 데이터를 저장하는 규칙이 있다.

- 이진 탐색 트리의 노드에 저장된 키는 유일하다.
  1. 루트 노드의 키가 왼쪽 서브 트리를 구성하는 어떠한 노드의 키보다 크다.
  2. 루트 노드의 키가 오른쪽 서브 트리를 구성하는 어떠한 노드의 키보다 작다.
  3. 왼쪽과 오른쪽 서브 트리도 이진 탐색 트리이다.
- 탐색의 시간 복잡도는 O(logN)이다. 최악의 경우, 편향 트리가 되어 O(N)이 될 수도 있다.
- 이진 탐색 트리의 순회는 **중위 순회**(in order) 방식이다.(왼쪽 - 루트 - 오른쪽)
- 중위 순회로 **정렬된 순서**를 읽을 수 있다.
- 중복된 노드가 없어야 한다.

**중복이 없어야 하는 이유는??**

검색을 목적으로 하는 자료구조인데, 굳이 중복이 많은 경우에 이 트리를 사용해 검색 속도를 느리게 할 필요가 없다. 트리에 삽입하는 것보다 노드에 count를 가지게 하여 처리하는 것이 훨씬 효율적이다.



[BST 핵심 연산]

- 검색
- 삽입
- 삭제
- 트리 생성
- 트리 삭제



[시간 복잡도]

- 균등 트리 : 노드 개수가 N개일 때, O(logN)
- 편향 트리 : 노드 개수가 N개일 때, O(N)

> 삽입, 검색, 삭제 시간 복잡도는 트리의 Depth에 비례.



삭제의 3가지 case

1. 자식이 없는 단말 노드일 때 -> 그냥 삭제
2. 자식이 1개인 노드일 때 -> 지워진 노드에 자식을 올리기
3. 자식이 2개인 노드일 때 -> 오른쪽 자식 노드에서 가장 작은 값 or 왼쪽 자식 노드에서 가장 큰 값 올리기 



편향된 트리(정렬된 상태 값을 트리로 만들면 한쪽으로 뻗음)는 시간 복잡도가 O(N) 이므로 트리를 사용할 이유가 사라진다. 이를 바로 잡도록 도와주고 개선된 트리는 AVL Tree, RedBlack Tree가 있다.



[이진 트리의 순회 방법]

1. 전위 순회(Pre Order) : 루트 -> 왼쪽 -> 오른쪽
2. 중위 순회(In Order) : 왼쪽 -> 루트 -> 오른쪽
3. 후위 순회(Post Order) : 왼쪽 -> 오른쪽 -> 루트