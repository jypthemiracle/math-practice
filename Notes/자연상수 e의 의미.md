# 자연상수 e의 의미

## Question

* 자연상수 e는 다음으로 표현된다.

![image-20210203204503612](/home/jypthemiracle/.config/Typora/typora-user-images/image-20210203204503612.png)

* 자연상수 e에 대해 생각하다가, 자연상수에 대한 의미에 대해 생각해보기로 하였다.

## Answer

* 자연상수 e는 자연의 연속적인 성장을 표현하기 위해 고안된 상수이다.
* 100%의 성장률을 가지고 1회 연속 성장할 때 얻게 되는 성장량을 의미한다.
* 마법의 저금통이 하나 있다고 하자. 이 저금통은 1원을 넣을 때 정확히 1년 뒤에 100% 성장하여 2원이 된다.
  * ```1+1=2```

![img](https://raw.githubusercontent.com/angeloyeo/angeloyeo.github.io/master/pics/2019-09-04_natural_number_e/pic1.png)

* 마법의 저금통의 수식을 바꾸어서, 6개월마다 50%씩 성장한다고 가정해보자.
* 6개월 단위로 50%씩 성장시키면 1년 뒤에는 2원이 아니라 2.25원이 된다.
  * ```(1+0.5)X(1+0.5)```
  * ```= 1 X (1 + 0.5) + 0.5 X (1 + 0.5)```
  * 원래의 1원이 1.5원이 되는 과정이 우변의 첫번째 항, 6개월 뒤에 얻어진 0.5원이 0.75원이 되는 과정이 우변의 두 번째 항에서 표현된 것이다.

![img](https://raw.githubusercontent.com/angeloyeo/angeloyeo.github.io/master/pics/2019-09-04_natural_number_e/pic2.png)

* 3번에 나누어서 성장시켜보도록 하자. 4개월에 33.33% 성장하는 저금통을 가정해보자.
  * ```(1 + 1/3)^3```

![img](https://raw.githubusercontent.com/angeloyeo/angeloyeo.github.io/master/pics/2019-09-04_natural_number_e/pic3.png)

* 1년 100%보다 6개월 50%, 6개월 50%보다 4개월 33%가 더 성장률이 높더라.
* 그렇다면, **“무한히 많이 쪼개면 어떻게 될까? 성장량도 무한하게 커질까?”**
  * 일반화를 시켜보면 다음과 같다. 같은 원리를 이용하여 100% 성장을 n번으로 나눠서 성장시키면 다음과 같다.
  * ```(1+1/n)^n```
  * ```lim_n->무한대 (1+1/n)^n = 2.178```

### 성장횟수와 성장률

* 50% 성장률을 가지고 1회 연속 성장한다면 그 값은 어떻게 될까.

  ![image-20210203205529708](/home/jypthemiracle/.config/Typora/typora-user-images/image-20210203205529708.png)

* 100% 성장률을 가지고 2회 연속 성장한다면 그 성장률은 ```e * e = e^2```이다.
* 즉, ```e^x``` 의 식에서 지수 x가 갖는 의미는, ```e^(성장횟수x성장률)``` 이다.
* 따라서 다음과 같이 쓸 수 있다.
  * A라는 성장률을 알고 있고, 이를 ```A=e^(성장횟수x성장률)``` 로 나타낼 수 있다고 가정한다.
  * ```ln(e^(성장횟수x성장률)) = 성장횟수x성장률```

### 자연상수가 밑인 지수함수의 미분

* 우리는 다음을 알고 있다.

  * ```d/dx(e^x)=e^x```
  * ```d/dx(a^x)=a^x(ln(a))```

* ```d/dx(e^x)=e^x``` 가 정말 연속 성장을 의미하나?

  * ```h=1```
    * ```(f(x+1)-f(x))/1=f(x)```
    * ```=f(x+1)=2f(x)```
    * 예시로는 ```f=2^x```가 있다.

  ![img](https://raw.githubusercontent.com/angeloyeo/angeloyeo.github.io/master/pics/2019-09-04_natural_number_e/pic4.png)

  * 즉, 다음번 x에서는 지금의 함수 크기 만큼 키워준다는 뜻이다.

* ```h=0.5```

  * ```(f(x+0.5)-f(x))/0.5=f(x)```
  * ```=f(x+0.5)=1.5f(x)```
  * 다시 말해 매번 아주 작은 스텝에서 매우 조금씩 크게 만들겠다는 것이고 이것은 다시 말하면 연속 성장이다.

### 참고

* https://angeloyeo.github.io/2019/09/04/natural_number_e.html
* https://blog.naver.com/sbssbi69/90164861352
* https://hyner.tistory.com/623

