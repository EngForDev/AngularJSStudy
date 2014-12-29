# Introduction
> Congratulations on taking the plunge!
This AngularJS course is built with the intent of exposing you to the best available resources on each Angular topic. Our desire is to present these topics richly, and from a variety of vantage points, in order to afford you a more complete perspective on them.

# 도입
돌입하시기로 한 것, 축하드린다!

이 코스의 의도는 여러분에게 AngularJs에 대한 각각의 주제에 대해서 가장 좋은 자료들을 접할 기회를 드리는 것이다. 우리가 원하는 것은 AngularJS에 대한 주제들을 풍부하게, 그리고 여러 가지 관점에서 다루는 것이다. 여러분이 이 주제에 대해서 좀 더 완전한 관점을 가질 수 있도록 말이다.

> This course is accompanied by AngularJS Tutorial: Learn to Build Modern Web Apps with MEAN.
이 코스는 

> The learning curve of AngularJS can be described as a hockey stick. Getting started with apps featuring basic functionality is delightfully easy. However, building more complex apps often require understanding Angular's inner workings. Failure to do so will cause development to become awkward and cumbersome.

AngularJs의 학습곡선은 하키채에 비유할 수 있다. 기본적인 기능을 사용해서 앱을 만들기 시작하는 것은 즐거울 정도로 쉽다. 하지만 좀 더 복잡한 앱을 만들려고 하면, 앵귤러의 내부 작동원리에 대한 이해가 필요한 경우가 종종 있다. 내부 작동원리를 잘 이해하지 못하면, 복잡한 앱을 만드는 것이 어렵고 느려질 수 있다. 


> With AngularJS, the "Ready, Fire, Aim" learning methodology of duct taping together a handful of tutorials and a cursory glance through the documentation will lead to confusion and frustration. This curriculum is designed to properly guide you through each of the key Angular concepts thoroughly with a broad exposure to high quality content. With your eventual mastery of AngularJS, you will be able to fluently and efficiently construct large-scale applications.

AngularJS의 경우에는, 튜토리얼 몇 개좀 보고 문서를 좀 살펴보고선, "준비, 조준, 발사"와 같은 학습방식이 별로 적절하지 않을 것이다. 그런 방식으로 접근하면 혼란스럽고 당황스러울 수 있다. 이 커리큘럼의 설계 방향은 여러분이 Augnular의 핵심 개념 각각에 대해서 양질의 자료를 살펴보게 함으로서 제대로 안내하는 것이다. AngularJS를 제대로 마스터한다면, 능숙하게 그리고 효율적으로 큰 규모의 어플리케이션을 개발할 수 있게 될 것이다.  


# Prerequisites


- Moderate knowledge of HTML, CSS, and JavaScript
-	Basic Model-View-Controller (MVC) concepts
-	The Document Object Model (DOM)
-	JavaScript functions, events, and error handling

# 필요한 사전 지식

-	HTML, CSS, JavaScript에 대한 중급 정도의 지식
-	[Model-View-Controller](http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) (MVC) 개념에 대한 기본적인 이해
- The [Document Object Model](http://en.wikipedia.org/wiki/Document_Object_Model) (DOM)
- 자바스크립트의 [함수](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions), [이벤트](https://developer.mozilla.org/en-US/docs/Web/API/Event), [에러처리에 관련 지식](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch)

# Resources

> Since AngularJS is still in its infancy relative to other JavaScript frameworks, the number of encyclopaedic resources on it is still insufficient. Therefore, the curriculum will employ a healthy number of excellent blogs in order to offer a more meaty perspective on respective topics.

# 참고자료

AngularJS는 여타 JavaScript 프레임워크에 비해서는 비교적 신생이기 때문에, 백과사전적인 참고자료는 아직 불충분한 실태이다. 따라서 이 커리큘럼에서는 각 주제에 대해 알찬 관점을 제공하기 위해서 훌륭한 블로그 자료를 많이 활용할 것이다. 

### Required Resources
-	AngularJS - O'Reilly Media (available on Amazon)
-	John Lindquist's egghead.io
-	AngularJS docs

###	Supplemental Resources
-	Ben Nadel blog
-	OneHungryMind
-	year of moo
-	Bruno Scopelliti blog


###	Required Resources
- [AngularJS - O'Reilly Media] (http://shop.oreilly.com/product/0636920028055.do)available on [Amazon](http://www.amazon.com/AngularJS-Brad-Green/dp/1449344852/ref=sr_1_1?ie=UTF8&qid=1372874049&sr=8-1&keywords=angularjs))
-	[John Lindquist's egghead.io](http://www.egghead.io/)
-	[AngularJS docs](http://docs.angularjs.org/)

###	Supplemental Resources
-	[Ben Nadel blog](http://www.bennadel.com/)
-	[OneHungryMind](http://onehungrymind.com/)
-	[year of moo](http://www.yearofmoo.com/)
-	[Bruno Scopelliti blog](http://blog.brunoscopelliti.com/)

# Part 1. Kicking the Tires

# 제1부.타이어 상태 점검하기

> AngularJS is not a library.
> Rather, it is a JavaScript framework that embraces extending HTML into a more expressive and readable format. It allows you to decorate your HTML with special markup that synchronizes with your JavaScript leaving you to write your application logic instead of manually updating views. Whether you're looking to augment existing JavaScript applications or harness the full power of the framework to create rich and interactive SPA's, Angular can help you write cleaner and more efficient code.

AngularJS는 라이브러리가 아니다.

AngularJS는 라이브러라기보다는 JavaScript 프레임워크이다. HTML을 확장해서 조금 더 표현력이 높고 가독성이 높은 형식으로 작성할 수 있게 해주는 프레임워크이다. AngularJS를 사용하면, HTML에다 특별한 마크업을 사용해서 JavaScript와 동기화할 수 있게 해준다. 그 결과, 수동으로 뷰를 갱신해주는 대신에 어플리케이션 로직을 작성해넣을 수 있다. 여러분이 원하는 것이 기존의 JavaScript 어플리케이션을 확장하는 것이든, 아니면 프레임워크의 기능을 총동원해서 풍부하고 인터렉티브한 [SPA](http://en.wikipedia.org/wiki/Single-page_application)를 만드는 것이든, Angular를 사용하면 더욱 명확하고 효율적인 코드를 작성할 수 있다.   
 
## Filling the Tank 
> We've found that the egghead.io videos are the best starting resource available, so every chapter will lead off with them. The transcribed screencasts and source code are provided along with the videos. We encourage you to follow along with them, as they make the video content much more readily digestible.
As good as the egghead videos are, they should serve only as an introductory resource. Excerpts from the O'Reilly AngularJS book and the angularjs.org documentation complement the videos as the broader and more thorough source, and should be treated as the main reference for the course.

## 연료 채우기
기존에 나와 있는 자료 중에 AngularJS를 시작하기에 최적으로, egghead.io 블로그의 동영상 강좌를 택하였다. 그래서 앞으로 각 장에서는 egghead.io의 동영상으로 시작할 것이다. 각 동영상 강좌 밑에는 녹취자료가 나와 있으며, 소스 코드가 제공된다. 이 소스 코드를 하나하나 실제로 따라서 해보기 바란다. 그러면 동영상 강좌를 훨씬 더 수월하게 이해할 수 있을 것이다. 
egghead의 동영강 강좌는 매우 좋기는 하지만, 그 역할은 '도입'에 그쳐야 할 것이다. O'Reilly사에서 출간한 AngularJS책의 발췌분과 angularjs.org의 문서가 동영상 강좌를 잘 보완해 줄 것이다. 이 자료들은 더욱 광범위하고 완전한 자료 소스이며, 이 코스의 주요 참고문헌이다. 

## Adjusting Your Mirrors
> When descending upon an entirely new topic, it is important to frame the topic correctly before diving into the minutia.
Read the following two entries in the AngularJS guide docs, they will give you a good idea of what you're about to get into. Don't worry about picking up on every aspect of the topics they glaze over, all of these will be covered thoroughly in subsequent lessons.

## 백/사이드미러 조정하기

전혀 낯선 주제를 접할 때에는, 세부적인 내용에 뛰어들기 전에 전체 그림을 파악하는 것이 중요하다. 

AngularJS 가이드 중 일부인 다음의 문서 두 개를 읽어보자. 두 문서를 읽으면, 여러분이 앞으로 접할 것이 어떤 것인지 감이 올 것이다. 두 문서에서 다루는 모든 내용의 세부사항을 완전히 이해하지 못하더라도 걱정하지 말자. 이 코스의 다음 장에서, 각 주제에 대해서 각각 자세하게 다룰 것이다. 

 
- [AngularJS Overview](https://code.angularjs.org/1.2.26/docs/guide/concepts)
- [Introduction to AngularJS](https://code.angularjs.org/1.2.26/docs/guide/introduction)


## Revving the Engine
> Before we get on with it, we recommend this post:

- Things I Wish I Were Told About Angular.js


## 엔진 예열하기
출발하기 전에, 아래의 글을 읽기를 권한다. 

- [Angular.js에 대해서 내가 알았더라면 좋았을 것들](http://ruoyusun.com/2013/05/25/things-i-wish-i-were-told-about-angular-js.html)

> It goes over a handful of topics that might be helpful in building the appropriate mental models while consuming the Angular curriculum. Some, probably most, of the terms will bounce right off you until you have gone through that section of the course, but it should provide valuable context when approaching a new topic.

이 포스트는 몇 가지 주제에 대해 다루는데, 이 Angular 커리큘럼 소화에 있어서 필요한 큰 틀을 내부적으로 만들어 두는 데 도움이 될 것이다. 이 글에 나오는 몇 가지 용어, 아마도 거의 대부분,는 대부분 그냥 머리에서 튕겨나올 것이다. 하지만 이 코스의 다음 섹션에서 해당 개념을 다루는 부분을 읽으면 이해가 될 것이다. 그래도 미리 이 글을 읽어두자. 이러한 개념들을 접해두면, 이 개념들이 어떤 맥락에 위치하는 지 파악할 수 있을 것이다.  

> Now it's off to the races!

이제 경주를 시작해 보자!
