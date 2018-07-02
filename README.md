# StackedBar

The guide line for Stacked bar chart

## Basic Usage

### HTML

```html
<div id="canvasArea">
    <canvas id="myChart" width="1000" height="600"></canvas>
</div>

<script type="text/javascript" language="javascript" src="stackedBarGuide.js"></script>
```

### JavaScript (jQuery)

* JSON Data

```js
var DATA =
                '                                        \
                {                                               \
                    "title":{                                  \
                        "title":"Quarter Spending",                    \
                        "label":["Estimate price","Market price","Proposer price","Proposer"],       \
                        "legend":["Material","Labor","Processing"]     \
                    },                                         \
                    "data":[                                    \
                        [10, 60, 10],                           \
                        [90, 90, 40],                           \
                        [80, 70, 40],                           \
                        [70, 40, 70]                           \
                    ],                                           \
                    "comment":"Comment is in here"       \
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
* useComment: "Y", //User Comment 표시 기능 : Y(Comment 표시), N(표시하지 않음)
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
