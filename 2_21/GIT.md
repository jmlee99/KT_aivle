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
