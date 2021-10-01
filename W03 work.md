**Object를 구성하는 요소들** Element - Attribute   
1. vertex - weight
2. edge
3. polygon - uv, normal
4. uv
5. normal
6. material

popnet: 파티클 시뮬레이션, dopnet이랑 똑같음   
dopnet node에는 output만 있지만 popnet에는 popsolver, popobject, popsource 등이 있음 

impluse activation: 매 프레임에 포인트를 몇 개씩 발사할 건지(0: 작동x, 1: 작동o)     
impluse count: 갯수     
const. activation: 초당 n개를 만들어내라(0: 작동x, 1: 작동o)   
const. birt race: 갯수     
두 개를 혼합해서 쓰는 경우는 드물고, 둘 중의 하나를 이용하면 됨. 

keying 넣는 방법: 파라미터에 alt 누른 채로 왼클릭, 파라미터 조절 후 다시 alt+왼클릭

Attribute    
P: Position  
v: velocity    
force: force    
age/life: 지속시간     
id: 파티클이 생성될 때 부여받는 고유한 번호. ptnum(point-number)은 새로운 점이 생겨도 범위 내에서 무작위로 번호를 계속 바꾸지만 id는 고유하기 때문에 새로 생김. 겹치지 않음.     
Cd: color Diffuse. point, vertex, edge 등이 가진 색상.   
uv: uv.    
N; Normal    

색마다 데이터 타입이 다름.    
Position, v, force는 (x, y, z)의 vector값.   
cyan은 float 타입.(0.0, 0.8, 1.2, 등) 소수점까지 가질 수 있는 하나의 수치.    
파란색은 int. 0, 1, 2, 3, 4, ..., n 의 정수값.   
