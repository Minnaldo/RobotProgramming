# 2장. ROS2 기반 로봇 개발에 필요한 정보
## 2.1. 커뮤니티 중심의 개발 문화
:개발은 로봇 운영체제 Robot Operating System(ROS)와 로봇 시뮬레이터 Ignition 이 중심을 이루고 모든 소스코드는 ROS, ROS2, Gazebo, Ignition과 같이 오픈되어 함께 개발되고 있다.
 관련된 문서 또한 위키 형태로 유지 보수되면서 커뮤니티 구성원 모두가 함께 만들어가고 있다.
 - 장점 : 이러한 커뮤니티 중심의 개발 문화는 쉽게 참여할 수 있고 개방적
 - 단점 : ROS 플랫폼과 ROS 커뮤니티를 처음 접하게 되면 낯설고 흩어져 있는 코드와 문서, 자료로 인해 학습하기가 다소 어려움

<br>
## 2.2. 즐겨찾는 ROS 2 정보 및 개발 자료
<br>
1. ROS 커뮤니티 게시판 ( https://discourse.ros.org/ ) <br>
2. ROS 2 문서 ( https://docs.ros.org/ ) <br>
3. ROS 2 디자인 문서 ( http://design.ros2.org/ ) <br>
4. ROS 위키 ( http://wiki.ros.org/ ) <br>
5. ROSCon 페이지 ( https://roscon.ros.org/ ) <br>
6. ROS 2 리포지터리 ( https://github.com/ros2 ) <br>
7. REPs(ROS Enhancement Proposals) ( https://ros.org/reps/rep-0000.html ) <br>
8. ROS 배포판 리포지터리 ( https://github.com/ros/rosdistro ) <br>
9. ROS 2 패키지 배포 현황 ( http://repo.ros2.org/status_page/ ) <br>
10. ROS 질의응답 페이지 ( https://answers.ros.org/questions/ )

<br>
## 2.3. ROS 커뮤니티 게시판
-'ROS Discourse' 
  : ROS 커뮤니티 게시판으로 모든 ROS 정보의 근원지라고 볼 수 있다.
  : ROS 각 버전별 정규 릴리즈 소식, 신규 패키지 소식, ROS TSC(Technical Steering Committe) 소식 및 회의 내용, 정규 워킹 그룹 회의 내용 공개, 각 나라별 ROS 이벤트, 구인/구직 정보, 신규 ROS 프로젝트, 교육 및 가오자 소식, 멀티로봇/MoveIt/Autoware/Drone 등
  
-ROS 2 기반으로 로봇 개발을 생각하고 있다면 ROS Discourse 가입은 필수라고 생각!
  => ROS는 커뮤니티 중심의 플랫폼이기 때문!!!

## 2.5. ROS 2 소스코드
:ROS 2 커뮤니티 게시판, ROS 2 문서와 함꼐 자주 찾는 곳이 있다면 단연 소스코드를 담고 있는 ROS 2 리포지터리 (https://github.com/ros2) 이다.
:ROS 2 기반의 프로젝트를 진행하면서 REPs(ROS Enhancement Proposals) ( https://ros.org/reps/rep-0000.html ) 리스트를 빼놓을 수 없다.

*REP 3 Target Platforms ( https://ros.org/reps/rep-0003.html ) : ROS 1 배포판들의 타깃 운영체제, 사용되는 라이브러리의 종류와 버전, 프로그래밍 언어 버전 등 <br>
*REP 103 Standard Units of Measure and Coordinate Conventions ( https://ros.org/reps/rep-0103.html ) : ROS 에서 사용되는 표준 단위와 좌표 변환 <br>
*REP 141 ROS distribution files (https://ros.org/reps/rep-0141.html ) : ROS 패키지 배포를 위한 패킹, 테스트 및 문서화 프로세스 <br>
*REP 149 Package Manifest Format Three Specification (https://ros.org/reps/rep-0149.html) : package.xml의 세 번째 포맷 규정 <br>
*REP 2000 ROS 2 Releases and Target Platforms (https://ros.org/reps/rep-2000.html) : ROS 2 배포판들의 타깃 운영체제, 라이브러리 버전, 프로그래밍 언어, DDS 등 <br>
*REP 2005 ROS 2 Common Packages (https://ros.org/reps/rep-2005.html) : ROS 2의 기본 패키지 리스트

<br>
-다양한 API 문서가 있지만, 그중에서 가장 기본이 되고 많이 사용되는 RCLCPP 및 RCLPY API 문서는 꼭 링크 주소를 알아두도록 하자. <br>
*RCLCPP API 문서 ( http://docs.ros2.org/foxy/api/rclcpp/index.html ) <br>
*RCLPY API 문서 ( http://docs.ros2.org/foxy/api/rclpy/index.html )

<br>
## 2.6. ROS 2 패키지 배포 현황
:ROS 2는 2014년ㄴ부터 개발이 시작되었고 공개 배포판이 꾸준히 정식 릴리즈되어 어느 정도 안정화 되었지만, 지금도 개발되고 있는 플랫폼인 만큼 릴리즈 계획, 배포 현황, 개발환경의 의존성 등을 유심히 살펴봐야 한다.

<br>
*ROS 1 패키지 배포 현황 ( http://repositories.ros.org/status_page/ ) <br>
*ROS 2 패키지 배포 현황 ( http://repo.ros2.org/status_page/ ) <br>
*ROS 2 Foxy 패키지 배포 현황 ( http://repo.ros2.org/status_page/ros_foxy_default.html )
