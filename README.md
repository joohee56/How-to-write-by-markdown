# How-to-write-by-markdown
</br>

# 1. 마크다운에 관하여

1.1 마크다운이란?

Markdown은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있고 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다. 마크다운이 최근 각광받기 시작한 이유는 깃헙(http://github.com) 덕분이다. 깃헙의 저장소 Repository에 관한 정보를 기록하는 README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였다. 마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 된다. (*프로젝트 소개, 소스코드 기록 및 공유*)

즉, 마크다운은 텍스트를 HTML로 변환하는 언어이자 도구이다.   

***
</br>

# 2. 마크다운 사용법(문법)

## 2.1 헤더Headers
* 큰 제목: 문서 제목

```
<마크다운>              <실행 결과>
This is an H1         <h1>This is an H1</h1>
===============
```

This is an H1
===============


</br>

* 작은 제목: 문서 부제목

```
This is an H2
--------------
```

This is an H2
--------------

</br>

* 글머리: 1~6까지만 지원

```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```

# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6

</br>

## 2.2 BlockQuote
이메일에서 사용하는 `>` 블럭인용문자를 이용합니다.
> This is a first blockquote.
> > This is a second blockquote.
> > > This is a third blockquote.
</br>

```
> This is a first blockquote.
> > This is a second blockquote.
> > > This is a third blockquote.
```
</br>
이 안에서는 다른 마크다운 요소를 포함할 수 있습니다.


> ### This is a H3
> * List
>   code

</br>

## 2.3 목록
### 순서있는 목록(번호)   
  
1. 첫 번째
2. 두 번째
3. 세 번째

```
1. 첫 번째
2. 두 번째
3. 세 번째
```
</br>

### 순서없는 목록 (글머리 기호: *, + ,- 지원)

* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑


- 빨강
  - 녹색
    - 파랑

</br>

```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑


- 빨강
  - 녹색
    - 파랑
```

</br>

혼합해서 사용하는 것도 가능합니다.   
* 1단계
  - 2단계
    + 3단계
      + 4단계

```
* 1단계
  - 2단계
    + 3단계
      + 4단계
```
</br>

# 2.4 코드

### 2.4.1 인라인 코드
```백틱(`)``` 을 사용해서 인라인 코드를 작성할 수 있습니다.   
(특수문자(\`) mac 단축키: 한글상태일 때는 ₩(원화 심볼)+Option, 영어 상태일 때는 ₩)

`인라인 코드는 이렇게 작성해요.`

```
`인라인 코드는 이렇게 작성해요.`
```
</br>

### 2.4.2 들여쓰기
4개의 공백 또는 2개의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속됩니다.   
</br>
This is a normal paragraph:    

    This is a code block.    
  
end code block.

</br>

```
This is a normal paragraph:    

    This is a code block.    
  
end code block.
```
</br>

> 한줄 띄어쓰지 않으면 인식이 제대로 되지 않는 문제가 발생합니다.

This is a normal paragraph:
    This is a code block.
end code block.
</br>

```
This is a normal paragraph:
    This is a code block.
end code block.
```
</br>

## 2.4.3 코드블럭
코드블럭은 다음과 같이 2가지 방식을 사용할 수 있습니다.
* `<pre><code> {code} </code></pre>` 이용방식   

```
<pre>
<code>
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }
}
</code>
</pre>
```

<pre>
<code>
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }
}
</code>
</pre>

</br>

* 코드블럭코드("\`\`\`") 을 이용하는 방법</br>

<pre>
</code>
```
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }
}
``` 
</code>
</pre>

```
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }
}
```

</br>

깃헙에서는 코드블럭코드("\`\`\`") 시작점에 사용하는 언어를 선언하여 문법강조(Syntax highlighting)이 가능합니다.

<pre>
</code>
``` java
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }
}
```
</code>
</pre>

``` java
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }
}
```
</br>

## 2.5 수평선 `<hr/r>`
아래 줄은 모두 수평선을 만듭니다. 마크다운 문서를 미리보기로 출력할 때 페이지 나누기 용도로 많이 사용합니다.

```
* * *
***
*****
- - -
----------------------
```

* * *
***
*****
- - -
----------------------

## 2.6 링크
인라인 링크, url 링크, 참조 링크로 나타낼 수 있습니다.

* 참조 링크   
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"

```
[link keyword][id]
[id]: URL "Optional Title here"

Link: [Google][googlelink]
[googlelink]: https://google.com "Go google"
```
* 외부 링크 (인라인 링크) </br>
[Google](https://google.com, "google link")

```
[Title](link)

[Google](https://google.com, "google link")
```
* 자동 연결 (url 링크)   
일반적인 URL 혹은 이메일 주소인 경우 적절한 형식으로 링크를 형성합니다.

외부 링크: <http://example/com/>   
이메일 링크: <address@example.com>

```
<link>

외부 링크: <http://example/com/>   
이메일 링크: <address@example.com>
```
</br>

## 2.7. 강조
*single asterisks*    
_single underscores_

**double asterisks**    
__double underscores__

~~cancelline~~

```
*single asterisks*
_single underscores_

**double asterisks**
__double underscores__

~~cancelline~~
```
</br>

> 문장 중간에 사용할 경우에는 **띄어쓰기** 를 사용하는 것이 좋습니다.    
> `문장 중간에 사용할 경우에는 **띄어쓰기** 를 사용하는 것이 좋습니다.`

</br>

## 2.8. 이미지

* 올리고 싶은 디렉토리 이미지 파일에서 ctrl+c, ctrl+v 
 
```
![이미지 이름](이미지 주소)    
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optinal title")

![img](https://user-images.githubusercontent.com/83942393/121797394-e1a8ef80-cc5a-11eb-8fd6-125535bd631a.jpeg) 
```

![img](https://user-images.githubusercontent.com/83942393/121797394-e1a8ef80-cc5a-11eb-8fd6-125535bd631a.jpeg)


> 사이즈 조절 기능은 없기 때문에 ```<img width="" height=""></img>```를 이용합니다.
```
<img src="/path/img.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img></br>
<img src="/path/img.jpg" width="40%" height="30%" title="% 크기 설정" alt="RubberDuck"></img></br>
```
<img src="https://user-images.githubusercontent.com/83942393/121797394-e1a8ef80-cc5a-11eb-8fd6-125535bd631a.jpeg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img></br>

<img src="https://user-images.githubusercontent.com/83942393/121797394-e1a8ef80-cc5a-11eb-8fd6-125535bd631a.jpeg" width="40%" height="30%" title="% 크기 설정" alt="RubberDuck"></img></br>

</br>

## 2.9 줄바꿈

```
줄 바꿈을 하기 위해서는 문장 마지막에서 3칸 이상 띄어쓰기를 해야 합니다.
문장 마지막에 </br> 입력하는 방법도 있습니다.
```
</br>

## 2.10 테이블
테이블은 `|`로 구분하며, 폰트 스타일을 적용할 수 있습니다. 또한 `-(하이픈)`으로 구분된 곳 각각 왼쪽, 양쪽, 오른쪽에 `:(세미콜론)`을 붙일 경우 순서대로 왼쪽 정렬, 가운데 정렬, 오른쪽 정렬이 가능합니다.

| 드라마 제목 | 주연 배우 | 방영일 |
|:----------|:----------:|----------:|
| **호텔 델루나** | 이지은, 여진구 | ~~2019.07.13. ~ 2019.09.01.~~ |
| 타인은 지옥이다 | 임시완, 이동욱, 이현욱, 이정은 | 2019.08.31. ~ |
| 멜로가 체질 | 천우희, 안재홍, 전여빈, 공명 | 2019.08.09. ~ |

```
| 드라마 제목 | 주연 배우 | 방영일 |
|:----------|:----------:|----------:|
| **호텔 델루나** | 이지은, 여진구 | ~~2019.07.13. ~ 2019.09.01.~~ |
| 타인은 지옥이다 | 임시완, 이동욱, 이현욱, 이정은 | 2019.08.31. ~ |
| 멜로가 체질 | 천우희, 안재홍, 전여빈, 공명 | 2019.08.09. ~ |
```
</br>

## 참고
https://gist.github.com/ihoneymon/652be052a0727ad59601   
https://velog.io/@yuuuye/velog-마크다운MarkDown-작성법
