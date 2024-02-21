# GIT란
- **GIT은 버전관리를 하는 시스템이다.**
- HEAD는 현재의 시간을 가리키는 것이고, main(master)은 마지막 시간을 가리키는 것이다.

> Check-out은 HEAD를 바꾼다.
> Reset은 HEAD가 가리키는 Branch(main이나 master)를 바꾼다.

- **GIT은 어떠한 버전도 (미래도 과거도) 버리지 않는다.**
> 즉, GIT으로 한 어떠한 버전도 다시 불러올 수 있다.
- **시간상 HEAD가 Ver1을 Branch로 가리키고 Ver2에 코드를 수정했다면 Ver2에 있던 것은 없어진다.**
> 하지만, Ver2의 Commit id를 알고 있다면
> git reset -- hard {Commit id}로 Ver2를 HEAD가 가리키는 main으로 바꾸면 돌아온다.
> GIT는 절대 버전을 없애지 않는다. 복사해서 붙여놓고 Commit id 이름만 바꿀 뿐이다.
> Commit id를 잊어버린 경우 [수업](https://opentutorials.org/course/2708/15304) 확인

- **checkout, reset마다 Commit id를 기억하는건 비효울적이다. ==> Creative Branch**
> 이제 Branch명이 Commit id를 대신한다.
> Branch가 두개 이상이 되었을때 부턴 Branch가 나눠지기 때문에 Branch log를 잘 보고 코드를 작성해야한다.
> 실험적인 코드는 Branch에 main code는 main에 짜는 것이다.

![image](https://github.com/jmlee99/KT_aivle/assets/98507134/97bdd48e-99ab-42b4-9382-9f35c98fd93f)


- **병합(main이 Branch를 병합할꺼냐 / Branch가 main을 병합할꺼냐 방향을 잘 선택 중요)**
> 이렇게 병합하게 되면 parents는 main과 Branch둘 다 parents다.

![image](https://github.com/jmlee99/KT_aivle/assets/98507134/a3049579-2878-4d52-9a51-165b68144b2f)


> 하나의 파일을 동시에 수정할 떈 conflict발생

![image](https://github.com/jmlee99/KT_aivle/assets/98507134/2592429c-4363-48de-b00a-dbf500360401)


> 위의 사진을 보면 마지막 merge에서 4번째는 둘 다 수정 했기 때문에 빈칸으로 남겨두고 사용자가 바꿀 수 있게 해준다.

> Branch는 아래와 같다.
![image](https://github.com/jmlee99/KT_aivle/assets/98507134/dc264119-b5f2-4603-b93b-cdf2b26b9e4f)

> 또한, conflict가 발생하면 VSC에서는 전문 Editer를 사용하여 conflict부분을 수정 가능하다.


![image](https://github.com/jmlee99/KT_aivle/assets/98507134/e695d203-ee11-4026-a950-6829ed030823)

> 버전을 백업하는 방법은 github를 사용하면 된다. 마지막에 어디까지 백업되었는지 확인(사진상 맨위의 origin)

![image](https://github.com/jmlee99/KT_aivle/assets/98507134/d8fe70de-602f-444c-b4ee-0186aef6c614)

> 이렇게 되면 L2는 L1보다 1개의 Commit가 앞선다는 뜻은 아직 L1까지만 백업되고 L2는 백업이 되지 않았다는 뜻이다.

![image](https://github.com/jmlee99/KT_aivle/assets/98507134/8c0d711b-7bbc-4218-945f-560cec51ecc1)

> 여기서 Push가 이루어지면 다음과 같이 표시된다.

![image](https://github.com/jmlee99/KT_aivle/assets/98507134/fe35ca22-9369-4dd2-abe7-0abae1633305)



# 협업
- **이때 사용하는 것이 Clone이다.**
- 새 에디터에서 Clone Repository ==> 원격 Repository의 주소를 추가한다.
- 작업이 끝나면 다시 Push를 해서 origin을 현재 작업한 작업물까지 백업시킨다.
