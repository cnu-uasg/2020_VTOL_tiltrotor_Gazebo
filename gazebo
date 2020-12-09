px4 1.10v

argos 모델은 현재 공력데이터가 들어가지않아 외형만 사용가능(추가예정)
1. ~/Firmware/Tools/sitl_gazebo/models/standard_vtol 에 들어가서 파일만 붙여넣기


2. 기존 build 되어있는 px4_sitl_default 폴더 삭제 후 재빌드 
  make px4_sitl gazebo_standard_vtol

  
=======================================

gazebo model 생성
1. 모델의 형상은 카티아를 통해 생성하며, stl파일을 dae파일로 변경하여 사용해야한다.

2. 형상관련 자료들(.dae)은 meshes 폴더에 넣고, 모델에 관련된 파일(model.config , model.sdf) 생성해야 한다.

3. sdf 파일에는 모델의 관성모멘트, 형상, 크기, 위치 등이 포함되어야한다. 

4. config 파일에는 모델에 대한 설명이 포함되어있다.

#px4에서 새로운 모델을 만들 시, 기존 폴더에 덮어 씌우는 것이 아니라면 make파일 수정해야함. 자세한 위치는 추가예정

1. Tools/sitl_gazebo/models
		+ Model

2. Tools/sitl_gazebo/worlds
		+ world

3. ROMFS/px4fmu_common/mixer-sitl
		+ mixer & Cmakelist

4. ROMFS/px4fmu_common/init.d-posix
		+ Model

5. platforms/posix/cmake/sitl_target.cmake
		+ Model name(line94~99)

======================================

world 생성
1. px4에서 world 는 기본적으로 empty.world가 작동된다. 

2. 하늘 추가하는 코드, empty.world에 넣으면 하늘이 생긴다.
   <scene>
      <sky>
        <clouds>
          <speed>12</speed>
        </clouds>
      </sky>
    </scene>

