# Sorting Algorithms - Bubble, Selection, Insertion, Merge

비교를 통해서 정렬하는데, 정렬(메서드의 호출)의 횟수에 따라 시간복잡도가 증가한다.

### Bubble Sort

- 인접한 값끼리 비교 & Swap
- 큰 값이 끝으로 정렬
- (무작위 콜렉션에서)성능이 가장 안좋은 편

> 한차례 순차적으로 비교를 마친 후, 이것을 반복한다. Swap이 일어나지 않을 때까지 반복하면 정렬 완료.
> 
- n - 1 회
- Best case: O(n)
- Worst case: O(n^2)

![2022-04-04_10-51-04.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5312dbd4-4871-45d4-acf3-ddff7537f615/2022-04-04_10-51-04.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220404%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220404T160754Z&X-Amz-Expires=86400&X-Amz-Signature=e7363dbea2cf05c0ef0d2e8ada4f29ccdd10c76626539a9258de2a281b38772f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%222022-04-04_10-51-04.png%22&x-id=GetObject)

### Selection Sort

- Bubble Sort와 유사
- 가장 낮은 수를 선택하여, 적절한 위치로 Swap

![2022-04-04_10-50-34.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4891e6dd-63e6-4123-950b-ceac809b3e06/2022-04-04_10-50-34.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220404%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220404T160832Z&X-Amz-Expires=86400&X-Amz-Signature=a60ac06472def90bf77e7e1a0d454690aa6c05985b63c6fad5bbc710f0c728f8&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%222022-04-04_10-50-34.png%22&x-id=GetObject)

### Insertion Sort

- 셋 중에는 가장 성능이 좋음
- 요소를 순회하며, 해당 요소의 이전(왼쪽) 요소와 비교하고, 왼쪽에 더 낮은 수가 올 때까지 계속 이동
위 작업을 반복.
- Bubble Sort처럼 전체를 여러번 순회하지 않음.

![2022-04-04_10-58-22.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/3d676f03-7ace-45c5-bcbc-21a309c0504f/2022-04-04_10-58-22.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220404%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220404T160851Z&X-Amz-Expires=86400&X-Amz-Signature=4ee1c72b8aa6dbb1f68c213c0ed352676d23800e6871c999c1f41b6e65fffef6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%222022-04-04_10-58-22.png%22&x-id=GetObject)

---

### Merge Sort

- 시간복잡도: O(n log n)
- 공간복잡도: O(n log n) // 원래 위치에서 요소를 mutate하는게 아닌, 새로운 메모리 공간을 할당받는다
- 전체 요소를 더이상 나눌 수 없을 때까지 반으로 쪼갠다.
- 인접한 두 그룹끼리 올바른 순서대로 정렬하여 병합한다. 
이를 반복하여 하나의 그룹으로 다시 합쳐지도록 한다.

### 구현

![2022-04-04_11-28-40.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/eb2250b7-0320-4430-af5d-b9b835d308b5/2022-04-04_11-28-40.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220404%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220404T160914Z&X-Amz-Expires=86400&X-Amz-Signature=cfc6ef612d3dc39b8049c79ba6c7532933ea2347ab0d42db37ddec65f11f970f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%222022-04-04_11-28-40.png%22&x-id=GetObject)

![2022-04-04_11-25-04.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ed7ca00f-a1a7-4f39-9209-f154761863c9/2022-04-04_11-25-04.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220404%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220404T160917Z&X-Amz-Expires=86400&X-Amz-Signature=6ec3f6c42483a568cd03f8659e949ed107b0884ae79143815072d8f5e11ec8c2&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%222022-04-04_11-25-04.png%22&x-id=GetObject)

![2022-04-04_11-28-12.png](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/1e182cd7-e191-4f5c-a90c-1418718bbb42/2022-04-04_11-28-12.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220404%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220404T160920Z&X-Amz-Expires=86400&X-Amz-Signature=ff539b953a3b0a0945b12e76259c5246662dbefb383fd0660255b538a2be13e8&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%222022-04-04_11-28-12.png%22&x-id=GetObject)

1. 배열의 중간지점 인덱스를 구하여 middle에 저장한다.
2. middle을 포함하지 않는 left 배열을 생성한다.
    1. 재귀적으로 
    ~ 더이상 나눠지지 않을 때 까지 이렇게 반으로 나누는 것을 반복한다.
    2. 나눠진 배열을 순서에 맞게 정렬하여 다시 합친 후 반환한다. ~
    3. 최종적으로 left는 정렬된 배열이 저장된다.
3. middle을 포함한 right배열을 생성한다.
    1. 2 - a,b,c 가 right에서도 이루어져, 정렬된 배열이 저장된다.
4. left와 right를 merge하여 반환한다.
