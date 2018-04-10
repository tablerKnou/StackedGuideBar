# StackedBar

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

* JSON Data

```js
var DATA =
  '                                                     \
          {                                               \
              "title":{                                   \
                  "title":"1분기 지출",                   \
                  "label":["1월","3월","3월","4월"],      \
                  "legend":["자재비","인건비","가공비"]   \
              },                                          \
              "data":[                                    \
                  [10, 60, 10],                           \
                  [90, 90, 40],                           \
                  [70, 40, 70],                           \
                  [40, 30, 50]                            \
              ]                                           \
          }                                               \
      ';
```

* initialize

```js
//parameter : canvas element id
var myChart = new KOSITV.StackedBar("myChart");
myChart.init(DATA);
```

Use options

* guideAlpha: 0.2, //Box Guide Line Alpha value : 0.0 ~1.0
* guideFillYN: "N", //Box Guide Line 을 라인만 표시 or 색상도 표시 여부 : Y(색상표시), N(선만)
* useComment: "Y", //[개발중]User Comment 표시 기능 : Y(Comment 표시), N(표시하지 않음)
* useGuideLine: "Y", //Box Guide Line 표시 여부 : Y(사용), N(표시하지 않음)
* onlyGroupBox: "N" //Box 를 x 축별 누적으로 표시 : Y(누적표시), N(개별 표시)

```js
var options = {
  useGuideLine: "Y",
  guideFillYN: "Y"
};
myChart.init(DATA, options);
```

## Copyright

Copyright 2018 [KOSITV Project](http://www.kositv.com).
