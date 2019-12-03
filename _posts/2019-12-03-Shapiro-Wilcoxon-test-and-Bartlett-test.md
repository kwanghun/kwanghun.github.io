__수업 시간에 위의 내용 중 `shapiro.test`와 `bartlett.test`의 해석을 반대로 하였기 때문에 바로잡겠습니다.__

-------

* Shapiro-Wilcoxon test는 자료의 정규성 검정하는 것이다.
* 이 정규성 검정 방법에서 귀무 가설과 대립 가설은 다음과 같다.
    * 귀무가설(H<sub>0</sub>): 자료가 정규 분포를 갖는다.
    * 대립가설(H<sub>1</sub>): 자료가 정규 분포를 갖지 않는다.
* 따라서 R의 `shapiro.test` 결과는 다음과 같이 해석해야 한다.
    * p-value \\(\ge\\) 0.05: 자료가 정규 분포를 갖는다.
    * p-value \\(\lt\\) 0.05: 자료가 정규 분포를 갖는다고 할 수 없다.

-------

* Bartlett's test는 자료의 등분산성을 검정하는 것이다.
* 이 등분산성 검정 방법에서 귀무 가설과 대립 가설은 다음과 같다.
    * 귀무가설(H<sub>0</sub>): 모든 표본집단의 분산이 같다 (등분산).
    * 대립가설(H<sub>1</sub>): 적어도 한 표본집단의 분산이 다르다.
* 따라서 R의 `bartlett.test` 결과는 다음과 같이 해석해야 한다.
    * p-value \\(\ge\\) 0.05: 모든 표본 집단의 분산이 같다고 할 수 있다. (등분산)
    * p-value \\(\lt\\) 0.05: 등분산성을 충족시키지 못함.

-------

There are critical errors on the explanation of Shapiro-Wilcoxon and Bartlett's test. 

The null hypothesis of Shapiro-Wilcoxon test is that data are distributed normally, so if the p-value is less than 0.05, we can reject the null hypothesis and conclude that the data are not distributed normally.   

The null hypothesis of Bartlett's test is all samples have the equal variance, so if the p-value is less than 0.05, we can reject the null hypothesis and conclude that at least one of the sample has different variance than others.   
A
You can find further details about the Shapiro-Wilcoxon test on [an article from the Wikipedia](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test) and the Bartlett's test on [and article from the Wikipedia](https://en.wikipedia.org/wiki/Bartlett%27s_test).


