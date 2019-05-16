# 백준 알고리즘 풀이

## A. 순열 / 조합 **(완전탐색, 백트래킹 기초)**
  **Ex) N과 M**

  #### 1. 순열(nPr)
   - n명 중에 r명을 **순서를 고려**하여 뽑는 경우의 수
   - 15649, 15654, 15663
   
  #### 2. 조합(nCr)
   - n명 중에 r명을 **순서를 고려하지 않고** 뽑는 경우의 수
   - 15650, 15655, 15664
   
  #### 3. 중복순열(nπr)
   - n명 중에 r명을 **순서를 고려**하고 **중복을 허용**하여 뽑는 경우의 수
   - 15651, 15656, 15665
   
  #### 4. 중복조합(nHr)
   - n명 중에 r명을 **순서를 고려하지 않고 중복을 허용**하여 뽑는 경우의 수
   - 15652, 15657, 15666
   
  #### 구현법
   - 재귀로 구현
   - c++ STL의 Next_Permutation
  
  ```c
  //1부터 4까지 저장할 벡터 선언
	vector<int> v(4);

	//1부터 4까지 벡터에 저장
	for(int i=0; i<4; i++){
		v[i] = i+1;
	}

	// next_permutation을 통해서 다음 순열 구하기
	do{
		for(int i=0; i<4; i++){
			cout << v[i] << " ";
		}

		cout << '\n';

	}while(next_permutation(v.begin(),v.end()));
  ```



## B. DFS / BFS **(완전탐색)**

  #### 1. DFS(Depth-First Search)
   - 시작점으로부터 한 방향으로 갈 수 있을 때까지 탐색하다가, **더이상 탐색 할 노드가 없을 때 다시 돌아와** 다음 노드도 같은 방식으로 탐색을 진행하는 방식
   - 스택, **재귀함수**로 구현
  
  
  #### 2. BFS(Breadth-First Search)
   - 하나의 정점으로부터 시작하여 차례대로 모든 정점들을 한 번씩 방문하는 것. 시작 정점으로부터 가까운 정점을 먼저 방문하고 멀리 떨어져 있는 정점을 나중에 방문하는 순회 방법이다.
   - **큐**로 구현
   - 방문했던 곳을 재 방문 하지않기위해, 따로 **배열을 만들어서 visit 여부를 체크.**

  #### 단계별로 풀어보기
  
  - 1. 토마토(7576) : DFS/BFS를 통한 완전탐색
  - 2. 토마토(7569) : DFS/BFS를 통한 완전탐색 + 3차원 배열
  - 3. 미로 탐색(2178) : BFS를 통한 완전탐색(최단거리)
  - 4. 바이러스(2606) : BFS를 통한 완전탐색
  - 5. 단지번호붙이기(2667) : BFS를 통한 완전탐색




## C. DP **(동적 프로그래밍)**

  #### DP(Dynamic Programming)
  
   - **작은 문제의 답을 조합해서 큰 문제의 답**을 푼다.
   - 최적화 기법 중 하나로 재귀(recursion)를 이용하여 최적화 솔루션을 얻어내는 방식
    
   - 1. 피보나치 수(2747) : DP를 이용하여 다음 값 출력
   - 2. 점프(1890) : DP + 구현
   - 3. 퇴사(14501) : DP + 구현
    



## D. Simulation **(구현)**

  #### Simulation
  
   - 알고리즘을 풀 때 요구되는 조건과 과정이 제시되어 그 과정을 거쳐 나온 결과를 추론하는 문제
   - 주어진 조건을 코드로 구현하는 과정
   - **구현은 양치기로 다양한 문제를 많이 풀어보는 것이 가장 중요하다!!!!!**
    
   - 1. 리모컨(1107) : 조건에 알맞게 원하는 채널로 이동하는 프로그래밍
   - 2. Puyo Puyo(11559) : 테트리스 게임과 유사. 벽돌이 제거되었을 때, 위의 벽돌을 내리는 방법을 프로그래밍
   - 3. Maze(16985) : 3차원 미로를 BFS와 DFS를 통해 구현하는 프로그래밍
    
    
    
    
    

# 삼성 알고리즘 기출

