#### 2024-07-15~16
  - 프로젝트 계획 수립
    - MAP: DMAP
    - NAV: Jetson / Turtlebot4
    - LLM: finetuning
    - MAN: Manipulator + Vision
    - RL: navigation & manipulation module
    - ~8/14 MAP+NAV+MAN / MAP+RL(NAV+MAN)
    - ~9/6 LLM+MAP+NAV+MAN / LLM+MAP+RL(NAV+MAN)
    
#### 2024-07-17~19
  - DMAP 패키징
    - ROS2 환경
    - dmap_node 작성

#### 2024-07-22~23
  - DMAP 패키징
    - map_server, goal_server 작성
    - 저성능 PC에서 사용하기 위해 inference 부분 중 torch로 제작된 부분을 numpy로 변경

#### 2024-07-24
  - DMAP 패키징
    - ~~tracer에서 실험해 본 결과 localization이 안되는 것을 확인~~(Done)
      - ~~map.pgm, map.yaml 파일 저장 시 오류로 추정~~(Done)
      - map_server 수정
  - exp_20240724

#### 2024-07-25~26
  - DMAP 패키징
    - tracer에서 localization 이슈 해결
      - nav2 launch를 안하였음
    - Jetson Orin Nano(Tracer Mini) 실험 결과 torch load없이 사용 가능을 확인
      - 추후 Raspberry Pi(Turtlebot)에서 실험 예정

TODO: 
  - keyframe selection 적용
    
#### TODO
- **Short Term**
  - voxel update (이미지 품질을 확인하는 과정이 필요)
  - Exploration
  - Ablation study (KFS, IQE)
  - ~~Point에 image embedding mapping~~(Done with query)
  - ~~HW 보완 Camera 높이 올리기, more cameras, PC에 직접 연결, 화각~~(Done)
  - Backend Operation (Queue)
  - Lifelong mapping (맵 저장 및 로드, feature 저장 및 로드)
  - TensorRT
- **Long Term**
  - 오검출 교차검증 필요, 알고리즘 보완해야함
  - AI Powered search
  - data diet
  - filtering points with multi camera view
  - GUI, search, sort
