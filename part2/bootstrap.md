## [Bootstrap](https://docs.angularjs.org/guide/bootstrap)

> This page explains the Angular initialization process and how you can manually initialize Angular if necessary.

이 페이지는 Angular 초기화 과정을 설명하고, 필요한 경우 수동으로 Angular 초기화하는 방법에 대해서 설명합니다.

### Angular `<script>` Tag

> This example shows the recommended path for integrating Angular with what we call automatic initialization.

이 예제는 우리가 자동 초기화라고 부르는 것을 Angular와 통합하기 위한 권장 경로를 보여줍니다.

```html
<!doctype html>
<html xmlns:ng="http://angularjs.org" ng-app>
  <body>
    ...
    <script src="angular.js"></script>
  </body>
</html>
```
> 1. Place the `script` tag at the botton of the page.
> Placing script tags at the end of the page improves app load time because the HTML loading is not blocked by loading of the `angular.js` script.
> You can get the latest bits from http://code.angularjs.org .
> Please don't link your production code to this URL, as it will expose a security hole on your site.
> For experimental development linking to our site is fine.

> * Choose: `angular-[version].js` for a human-readable file, suitablefor development and debugging.
> * Choose: `angular-[version].min.js` for a compressed and obfuscated file, suitable for use in production.

> 2. Place `ng-app` to the root of your application, typically on the `<html>` tag if you want angular to auto-bootstrap your application.

> 3. If you choose to use the old style directive syntax `ng:` then include xml-namespace in `html` to make IE happy. (This is here for historical reasons, and we no longer recommend use of `ng:`.)
