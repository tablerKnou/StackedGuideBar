# StackedGuideBar

The guide line for Stacked bar chart

## Basic Usage

### HTML

```html
<div id="canvasArea">
    <canvas id="myChart" width="1000" height="600"></canvas>
</div>

<script src="https://code.jquery.com/jquery-1.12.4.min.js" integrity="sha256-ZosEbRLbNQzLpnKIkEdrPv7lOy9C27hHQ+Xp8a4MxAQ=" crossorigin="anonymous"></script>
<script type="text/javascript" language="javascript" src="stackedBarGuide.js"></script>
```

### JavaScript (jQuery)

```js
/*
    javascript Library : KOSITV.StackedBar
    - Param : canvas element id
*/

//StackedBar guide chart without options
var myChart = new KOSITV.StackedBar("myChart");
myChart.init(DATA);

//Use options
/*
var options = {
    guideAlpha: 0.2,                //Box Guide Line Alpha value : 0.0 ~1.0
    guideFillYN: "N",               //Box Guide Line을 라인만 표시 or 색상도 표시 여부 : Y(색상표시), N(선만)
    useComment: "Y",                //[개발중]User Comment 표시 기능 : Y(Comment 표시), N(표시하지 않음)
    useGuideLine: "Y",              //Box Guide Line 표시 여부 : Y(사용), N(표시하지 않음)
    onlyGroupBox: "N"               //Box를 x축별 누적으로 표시 : Y(누적표시), N(개별 표시)
};
*/
var options = {
  useGuideLine: "Y",
  guideFillYN: "Y"
};
myChart.init(DATA, options);
```

## Copyright

Copyright 2018 [KOSITV Project](http://www.kositv.com).
