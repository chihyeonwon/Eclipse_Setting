# Eclipse_Setting
[Eclipse] 관련 Setting 정리

## SpringBoot Version과 JRE와 맞지 않을 때
![image](https://github.com/mr-won/Eclipse_Setting/assets/58906858/3a1e4635-6db3-4a5d-b6cb-22188f2c6dce)     
SpringBoot 3.x 버전은 Java 17이상부터 지원한다.    
따라서 build.gradle 파일의 springboot 버전을 2.x 로 다운그레이드하는 방법이 있다.    
2.x로 작성한 후 refresh gradle project를 눌러 sync 작업을 수행한다.    
![image](https://github.com/mr-won/Eclipse_Setting/assets/58906858/49b6e9d4-b95d-434f-9711-4ad171d275c2)     
![image](https://github.com/mr-won/Eclipse_Setting/assets/58906858/4e9a7b66-fbd5-4494-bfbc-8439b19c8f99)     
또는 project 우클릭 properties - Java compiler, Java Build Path의 버전을 11로 맞춘다.
    
Springboot 3.x -> Java 17 +    
Springboot 2.x -> Java 11           

## 자동완성 기능 활성화
![image](https://github.com/mr-won/Eclipse_Setting/assets/58906858/22403cac-aba3-4234-af30-4c4acb6db3eb)    
![image](https://github.com/mr-won/Eclipse_Setting/assets/58906858/80b938af-2a03-493d-9f17-726cd00ea82f)    

Window - preference - content assist     
Auto activation delay는 0으로 하고    
Auto activation triggers for java 입력란 에는 아래 문자열 코드를 전체 복사해서 붙여놓으면 된다.    
     
<=$:{.@qwertyuioplkjhgfdsazxcvbnm_QWERTYUIOPLKJHGFDSAZXCVBNM

## The Eclipse executable launcher was unable to locate its companion shared library.
![image](https://github.com/chihyeonwon/Eclipse_Setting/assets/58906858/1285be52-1701-4369-8df4-9f90d8cf707a)
```
이 오류는 eclipse.ini 파일의 --launcher.library에 org.eclipse.equinox.launcher 파일의 경로가 제대로 되어있지 않아 발생하는 오류이다.
```
![image](https://github.com/chihyeonwon/Eclipse_Setting/assets/58906858/c0015a64-8dc0-4664-8552-9d1e29d5512e)
![image](https://github.com/chihyeonwon/Eclipse_Setting/assets/58906858/5b9adc1e-4445-475b-b8a8-7f2c1a102a21)
```
plugins 폴더에 있는 launcher를 넣어준다.
```

## java was started but returned exit code=1, 13
![image](https://github.com/chihyeonwon/Eclipse_Setting/assets/58906858/8c526873-19f3-48a2-939e-6ad01bdeeb5e)
```
-vmargs보다는 위에 -vm 바로 밑에 jdk version에 맞는 javaw.exe나 /server/jvm.dll 파일의 경로를 넣어준다.
```
