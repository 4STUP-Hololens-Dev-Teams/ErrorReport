## AR UAV Path Simulator Development with MS Hololens 2 

Dankook University <br>Kim Hee Ju <br>Lee Jin Ho <br>Park Seo Yoon<br>Jeong Jun seo <br>



<br><br>



| Title       | Contents                                  |
| ----------- | ----------------------------------------- |
| Device      | Microsoft Hololens 2                      |
| Environment | Unity 3D, UWP(Universal Windows Platform) |
| Language    | C#                                        |



### Error Report

------

#### Build Error 01

- Unity3d 상에서 제대로 빌드 및 실행이 되는 것을 확인.

* Hololens2에 빌드 후  `Build Error`  발생

<img src="https://user-images.githubusercontent.com/19165180/117533337-312a4900-b027-11eb-8004-9d1e883b5d07.jpg" alt="error img 01" style="zoom:67%;" />



**[Solution]** 

* Hololens를 재시동 하였음.





#### **Build Error 02**

* Unity3d-Hololens Build까지 성공하였으나 경로를 찾지 못하였다는 안내가 뜸
* Local `txt file`이 홀로렌즈에 함께 빌드되지 않은 상황으로 확인
* Debug Log를 통해 *error*를 확인

```
could not find a part of the path
C:/Data/User/DefaultAccount/AppData/Local/Development/Files/Template3dvs.release_arm64.mobile/.assets/text/path.txt
```



**[Solution]** 

* Unity 최상위폴더 중 Assets 하위에 Resources 폴더를 생성
* 해당 폴더에 txt파일을 삽입
* 이후 Resources 관련 함수를 호출







