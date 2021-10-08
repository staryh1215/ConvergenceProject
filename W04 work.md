1. geo - sphere랑 box 노드 만들어주기
2. boolean 노드 생성 후 sphere(A) 랑 box(B) 연결
3. box에 transform 노드 연결해서 위치, 크기, 각도 변경
3-1. Pivot Transform에서 $CEX, $CEY, $CEZ 입력하면 중심 축 물체 가운데로 이동
4. boolean 노드로 보면서 박스 위치 이동시켜 구랑 겹쳐주면 겹치는 부분 사라짐
5. boolean 노드에서 OutputPrimitiveGroups 탭 중 AinsideB, BinsideA 선택
6. blast 노드 생성 후 boolean에 연결
7. blast에서 Group - binsidea 선택, Delete Non Selected 체크
8. box 노드로 이동, Division 체크 후 Primitive Type - Polygon Mesh로 선택
9. Avis Divisions 조정
10. box 노드 - Transform(Scale) 노드 밑, transform(POS, ROT) 노드 위에 mountain 노드 생성 후 연결
11. mountain node에서 Height, Element Size, Offset, Time 조정해가면서 애니메이션 주기 
12. 프레임 이동 후 Time 탭에 $F 입력하면 프레임마다 변화 (너무 빠르다 싶으면 $F*0.5, 등 곱셈 변화 주기)
13. Noise Type 마음에 드는 대로 선택 [Noise Type](https://www.sidefx.com/docs/houdini/nodes/vop/unifiednoise.html)
14. 스케일, 회전, 위치 값 조정하면서 애니메이션 주기
14-1. 프레임마다 조정하면서 alt 키로 키 적용할 수 있지만 $F 활용하는 편이 간편함
14-2. $F 입력한 곳에 shift 누른 채로 클릭하면 애니메이션 수정 가능. 
15. sphere도 Frequency 값 조정해서 쪼개주고, 밑에 subdivide 노드 생성 후 연결
16. Null 노드 두 개 생성해서 각각 boolean, blast 밑에 이어준 후 IN_GEO, IN_PARTICLE_EMITTER로 이름 변경
17. PopNetwork 노드 생성 후 IN_PARTICLE_EMITTER에 첫 번째로 연결 

40분부터 이어서 보기 
