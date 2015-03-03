
# Conceptual Overview 
> ### [원문 링크] (https://code.angularjs.org/1.2.26/docs/guide/concepts)

> This section briefly touches on all of the important parts of AngularJS using a simple example. For a more in-depth explanation, see the tutorial.

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

> In the following example we will build a form to calculate the costs of an invoice in different currencies.<br>
아래 예제에서 우리는 청구서 비용을 다른 통화들로 계산하는 하나의 form을 만들어 볼 것입니다.

> Let's start with input fields for quantity and cost whose values are multiplied to produce the total of the invoice:<br>
청구서의 합계를 산출하기 위해 값들이 서로 곱해지는 수량과 비용을 위한 input 필드로 시작해 봅시다.

html 소스 코드 [예제링크] (http://plnkr.co/edit/AGC0fcS2oZYWqqqfiaCM?p=preview "plunker 로 이동")


    <div ng-app ng-init="qty=1;cost=2">
     <b>Invoice:</b>
     <div>
        Quantity: <input type="number" ng-model="qty">
      </div>
      <div>
        Costs: <input type="number" ng-model="cost">
      </div>
      <div>
        <b>Total:</b> {{qty * cost | currency}}
      </div>
    </div>

> Try out the Live Preview above, and then let's walk through the example and describe what's going on.
위 실시간 미리보기를 시도해 본 뒤, 예제를 살펴보고 어떻게 돌아가는지 설명하겠습니다.

> This looks like normal HTML, with some new markup. In Angular, a file like this is called a "template". When Angular starts your application, it parses and processes this new markup from the template using the so called "compiler". The loaded, transformed and rendered DOM is then called the "view".

이것은 새로운 markup을 가진 일반적인 HTML로 보이는데, Angular에서 이같은 파일을 templete이라고 합니다. Angular가 application을 실행할 때, 그 template 에 있는 새로운 markup을 소위 compiler 라고 하는 것이  파서하고 처리합니다. 그런 뒤, 로드되고 변형되고  렌더링된 DOM은 view 라고 합니다.

> The first kind of new markup are the so called "directives". They apply special behavior to attributes or elements in the HTML. In the example above we use the ng-app attribute, which is linked to a directive that automatically initializes our application. Angular also defines a directive for the input element that adds extra behavior to the element. The ng-model directive stores/updates the value of the input field into/from a variable.

새로운 markup의 첫번째 종류는 directives 라고 합니다. 그것들은 HTML내의 속성이나 요소에 특별한 행동을 적용합니다. 위 예제에서 자동적으로 application을 초기화하는 directive에 연결된, ng-app 속성을 사용합니다. 또한, Angular는 input 요소에 추가적인 행동을 덧붙이는 해당 요소에 대한  directive 정의합니다. ng-model directive는 변수에 input 값을 저장하고 변수로 부터 input 값을 갱신합니다.

![Data Binding] (https://code.angularjs.org/1.2.26/docs/img/guide/concepts-databinding1.png)

- - - -
**Custom directives to access the DOM:** In Angular, the only place where an application should access the DOM is within directives. This is important because artifacts that access the DOM are hard to test. If you need to access the DOM directly you should write a custom directive for this. The directives guide explains how to do this.

**DOM에 접근하기 위한 사용자 정의 directives:** Angular에서, application이 DOM에 접근할 수 있는 유일한 곳은 directives 안 입니다. 이것은 DOM에 접근하기 위해 임의로 만들어진 코드들을 테스트하기는 힘들기 때문에 중요합니다. 만약 DOM에 직접적으로 접근할 필요가 있다면, 그것에 대한 사용자 정의 directive를 만드는 것이 좋습니다. directives 가이드에서 이것을 만드는 법을 설명합니다.
- - - -

> The second kind of new markup are the double curly braces {{ expression | filter }}: When the compiler encounters this markup, it will replace it with the evaluated value of the markup. An "expression" in a template is a JavaScript-like code snippet that allows to read and write variables. Note that those variables are not global variables. Just like variables in a JavaScript function live in a scope, Angular provides a "scope" for the variables accessible to expressions. The values that are stored in variables on the scope are referred to as the "model" in the rest of the documentation. Applied to the example above, the markup directs Angular to "take the data we got from the input widgets and multiply them together”.

새로운 마크업의 두번째 종류는 두개의 중괄호 {{ expression | filter }}: 입니다. compiler가 이 마크업을 접하면, 그것은 그 마크업의 검토된 값들을 가진 것으로 대체됩니다. template 안에서 expression은 변수들을 읽고 쓸 수 있게 하는 code snippet 같은 자바스크립트입니다. 그 변수들은 전역 변수들이 아님을 알아 둡니다. 단지 자바스크립트 함수 영역내에서 존재하는 변수와 같이, Angular도 expression들에 접근가능한 변수들을 위해 영역(scope)을 제공합니다. 그 영역안에서 변수에 저장된 값들은 그 문서의 expression을 제외한 나머지 부분에서는 model로 기술합니다. 위 예제에 적용된 마크업을 보면, 그것은 Angular에게 “input 위젯으로 부터 얻은 데이터를 가지고 와서 함께 곱해라”고 지시합니다. 

> The example above also contains a "filter". A filter formats the value of an expression for display to the user. In the example above, the filter currency formats a number into an output that looks like money.

위 예제는 또한 filter 를 포함합니다. filter는 사용자에게 표시하기 위한 expression의 값을 포맷합니다. 위 예제에서, 통화 filter는 숫자를 화폐처럼 보이는 결과물로 포맷합니다.

> The important thing in the example is that angular provides live bindings: Whenever the input values change, the value of the expressions are automatically recalculated and the DOM is updated with their values. The concept behind this is "two-way data binding”.

그 예제에서 중요한 것은 angular는 실시간 바인딩을 제공한다는 것입니다: input 값들이 변경될 때마다, expression들의 값은 자동적으로 재계산되어 지고 그 값들을 가진 DOM으로 갱신되어 집니다. 이것에 깔려 있는 개념은 쌍방향 데이터 바인딩입니다.

## Adding UI logic: Controllers	
## UI 추가하기 : Controllers


> Let's add some more logic to the example that allows us to enter and calculate the costs in different currencies and also pay the invoice.

비용을 입력하고 다른 통화로 계산할 수 있으며, 청구서를 지불할 수 있게 하는  그 예제에  좀 더 많은 로직을 추가해 봅시다.

html 소스 코드 [예제링크] (http://plnkr.co/edit/xIr9e93Nie1u1nPuKLlR?p=preview "plunker 로 이동")

    <div ng-app="invoice1" ng-controller="InvoiceController as invoice">
     <b>Invoice:</b>
     <div>
       Quantity: <input type="number" ng-model="invoice.qty" required >
     </div>
     <div>
     	Costs: <input type="number" ng-model="invoice.cost" required >
    	<select ng-model="invoice.inCurr">
      		<option ng-repeat="c in invoice.currencies">{{c}}</option>
    	</select>
     </div>
     <div>
    	<b>Total:</b>
    	<span ng-repeat="c in invoice.currencies">{{invoice.total(c) | currency:c}}</span>
    	<button class="btn" ng-click="invoice.pay()">Pay</button>
     </div>
    </div>
    
 invoice1.js 소스 코드 [예제링크] (http://plnkr.co/edit/xIr9e93Nie1u1nPuKLlR?p=preview "plunker 로 이동")
 
     angular.module('invoice1', [])
      .controller('InvoiceController', function() {
  		this.qty = 1;
		this.cost = 2;
  		this.inCurr = 'EUR';
  		this.currencies = ['USD', 'EUR', 'CNY'];
  		this.usdToForeignRates = {
		    USD: 1,
    		EUR: 0.74,
    		CNY: 6.09
  		};

  		this.total = function total(outCurr) {
    		return this.convertCurrency(this.qty * this.cost, this.inCurr, outCurr);
		};
  		this.convertCurrency = function convertCurrency(amount, inCurr, outCurr) {
    		return amount * this.usdToForeignRates[outCurr] / this.usdToForeignRates[inCurr];
  		};
  		this.pay = function pay() {
    		window.alert("Thanks!");
  		};
	});

> What changed?

무엇이 변했나요?

> First, there is a new JavaScript file that contains a so called "controller". More exactly, the file contains a constructor function that creates the actual controller instance. The purpose of controllers is to expose variables and functionality to expressions and directives.

먼저, 이른바 controller라 일컫는 것을 포함하는 새로운 자바스크립트 파일이 있습니다. 좀 더 정확히는, 그 파일은 실제 controller 인스턴스를 생성하는 생성자 함수를 포함합니다. controller들의 목적은 (함수 내부에 정의하여 감춰둔) 변수들과 기능을 expression들과 directive들에서 접근할 수 있도록 드러내는 것입니다. (생성자 함수로  contoller 개체를 생성한 후에야 비로소 controller 내에 정의된 변수나 함수를 참조 할 수 있습니다.)

> Besides the new file that contains the controller code we also added a ng-controller directive to the HTML. This directive tells angular that the new InvoiceController is responsible for the element with the directive and all of the element's children. The syntax InvoiceController as invoice tells Angular to instantiate the controller and save it in the variable invoice in the current scope.

controller 코드를 포함하는 그 새로운 파일 외에도, 우리는 또한 'ng-controller’ directive 를 HTML에 추가했습니다. 이 directive는 angular에게 새로운 ‘InvoiceController' 는 그 directive 를 가진 요소와 그 요소의 모든 자식들을 책임진다고 말해 줍니다. 구문 ‘InvoiceController as invoice’ 는 Angular 에게 그 controller를 인스턴스화 하고 현재 영역(scope)안의 ‘invoice’ 변수에 저장하라고 말합니다. 

> We also changed all expressions in the page to read and write variables within that controller instance by prefixing them with invoice. . The possible currencies are defined in the controller and added to the template using ng-repeat. As the controller contains a total function we are also able to bind the result of that function to the DOM using {{ invoice.total(...) }}.

우리는 또한  ‘invoice.’ 를 변수들 앞에 붙여 그 controller 인스턴스 내에서 변수들을 읽고 쓰도록 페이지 내 모든 expression들을 변경했습니다. 가능한 통화들은 controller 안에서 정의 되고 ‘ng-repeat’를 사용해 template에 추가 됩니다. 그 controller 는 total 함수를 포함하기 떄문에 우리는 역시 그 함수의 결과를 {{ invoice.total(...) }}를 사용해 DOM 과 연결할 수 있습니다.

> Again, this binding is live, i.e. the DOM will be automatically updated whenever the result of the function changes. The button to pay the invoice uses the directive ngClick. This will evaluate the corresponding expression whenever the button is clicked.

다시 말하자만, 이 바인딩은 실시간입니다. 예로, 그 함수의 값이 변경될 때마다 DOM은 자동적으로 갱신될 것 입니다. 청구서를 지불하기 위한 버튼은  ‘ngClick' directive를 사용합니다. 이것은 그 버튼이 클릭될 때마다 그에 상응하는 expression을 평가할 것 입니다.

> In the new JavaScript file we are also creating a module at which we register the controller. We will talk about modules in the next section.

새로운 자바스크립트 파일안에서, 그 controller를 등록한 곳에서 우리는 또한 module를 만들고 있습니다. 다음 섹션에서 module들에 대해 애기할 것입니다.

> The following graphic shows how everything works together after we introduced the controller:

아래 그림은 모든 것들이 어떻게 함께 작동하는지 보여줍니다.: 

![그림] (https://code.angularjs.org/1.2.26/docs/img/guide/concepts-databinding2.png)
