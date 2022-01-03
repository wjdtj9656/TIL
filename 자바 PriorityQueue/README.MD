PrioirtyQueue란?
우선순위 큐를 의미합니다.

일반적인 큐는 값에 순서가 없지만, 우선순위는 값을 오름차순, 내림차순을 이용합니다.

사용이유
저는 정렬된 큐를 사용하고 싶을때 사용합니다.

	BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
	BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
	
	PriorityQueue<Integer> pq = new PriorityQueue<>();
	//큐에 값더하기
	pq.add(5);
	pq.add(7);
	//큐 초기화
	pq.clear();
	pq.add(3);
	pq.add(1);
	pq.add(-5);
	
	//제일 앞에 있는 큐 꺼내기[-5, 1, 3]
	bw.write(String.valueOf(pq.poll())+"\n");
	
	//제일 앞에 있는 큐 꺼내진 않고 확인만 하기[1, 3]		
	bw.write(String.valueOf(pq.peek())+"\n");
	//큐에 해당값 있는지 확인(true, false 반환) [1,3]
	bw.write(String.valueOf(pq.contains(1))+"\n");
	
	bw.write(String.valueOf(pq));
	bw.flush();
	bw.close();
}
}

p.s 역순 우선순위 큐를 사용하고 싶으면
PriorityQueue pq = new PriorityQueue<>(Collections.reverseOrder());

를 사용합니다.