# Conceptual Overview

This section briefly touches on all of the important parts of AngularJS using a simple example. For a more in-depth explanation, see the tutorial.

이번 섹션에서는 AngularJS의 중요한 부분 모두를 단순한 예제를 통해 간단히 언급합니다. 좀 더 깊은 설명을 위해서는 이 tutorial 를 봅니다.

<table>
  <tr>
    <td>Concept</td>
    <td>Description</td>
  </tr>
  <tr>
    <td>Template</td>
    <td>HTML with additional markup<br>추가적인 마크업을 가진 HTML</td>
  </tr>
  <tr>
    <td>Directive</td>
    <td>extend HTML with custom attributes and elements
    사용자 정의 속성들과 요소들을 가진 HTML로 확장</td>
  </tr>
  <tr>
    <td>Model</td>
    <td>the data shown to the user in the view and with which the user interacts<br>view에서 사용자에서 보여지고 사용자가 상호작용하는 데이터 </td>
  </tr>
  <tr>
    <td>Scope</td>
    <td>context where the model is stored so that controllers, directives and expressions can access it<br>
    model이 저장되어 controllers, directives 그리고 expressions 들이 접근할 수 있는 컨텍스트</td>
  </tr>
  <tr>
    <td>Expressions</td>
    <td>access variables and functions from the scope<br>
    scope에서 변수들과 함수들에 접근</td>
  </tr>
  <tr>
    <td>Compiler</td>
    <td>parses the template and instantiates directives and expressions<br>
    template을 파서하고, directive와 expression을 객체화</td>
  </tr>
  <tr>
    <td>Filter</td>
    <td>formats the value of an expression for display to the user<br>
    사용자에게 보여주기 위해 expression의 값을 포맷</td>
  </tr>
  <tr>
    <td>View</td>
    <td>what the user sees (the DOM)<br>사용자가 보는 것</td>
  </tr>
  <tr>
    <td>Data Binding</td>
    <td>sync data between the model and the view<br>
    model과 view 사이의 데이터를 동기화</td>
  </tr>
  <tr>
    <td>Controller</td>
    <td>the business logic behind views<br>
    view 뒤에서 일어나는 데이터 처리 (비지니스 로직)</td>
  </tr>
  <tr>
    <td>Dependency Injection</td>
    <td>Creates and wires objects and functions<br>
    객체들과 함수들을 생성하고 연결</td>
  </tr>
  <tr>
    <td>Injector</td>
    <td>dependency injection container<br>
    dependency injection 컨테이너</td>
  </tr>
  <tr>
    <td>Module</td>
    <td>a container for the different parts of an app including controllers, services, filters, directives which configures the Injector<br>
    controller, service, filter, directive 들을 포함하는 앱의 다른 파트들을 위한 컨테이너로 injector의 환경을 설정</td>
  </tr>
  <tr>
    <td>Service</td>
    <td>reusable business logic independent of views<br>
    재사용할 수 있는 view의 독립적인 비지니스 로직</td>
  </tr>
</table>
	
## A first example: Data binding
## 첫번째 예제 : 데이터 바인딩

In the following example we will build a form to calculate the costs of an invoice in different currencies.<br>
아래 예제에서 우리는 청구서 비용을 다른 통화들로 계산하는 하나의 form을 만들어 볼 것입니다.

Let's start with input fields for quantity and cost whose values are multiplied to produce the total of the invoice:<br>
청구서의 합계를 산출하기 위해 값들이 서로 곱해지는 수량과 비용을 위한 input 필드로 시작해 봅시다.
