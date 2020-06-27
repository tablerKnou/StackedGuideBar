# StackedBar (v1.21)

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

* guideAlpha: 0.2, 						//Box Guide Line Alpha value : 0.0 ~1.0
* guideFillYN: "N", 					//Box Guide Line 을 라인만 표시 or 색상도 표시 여부 : Y(색상표시), N(선만)
* useComment: "Y", 						//User Comment 표시 기능 : Y(Comment 표시), N(표시하지 않음)
* useGuideLine: "Y", 					//Box Guide Line 표시 여부 : Y(사용), N(표시하지 않음)
* onlyGroupBox: "N" 					//Box 를 x 축별 누적으로 표시 : Y(누적표시), N(개별 표시)
* legendNameSize:12                     //(v.1.21) Legend Font Size : default 12(pt)
* xAxisNameSize:13                      //(v.1.21) X Axis Font Size : default 12(pt)
* valueFontSize:14                      //(v.1.21) Value Font Size : default 12(pt)
* displayValueComma: "Y"                //(v.1.21) Item별 Value값에 Currency Format 적용(Comma) : Y(Comma표시), N(미표시)
* useDisplayValue: "Y"                  //(v.1.21) Item별 Value값 표시 여부 : Y(사용), N(표시하지 않음)
* useValueUnit: 1000                    //(v.1.21) value의 단위 환산 ex:) ,useValueUnit: 1000 => 1/1000로 변환 
* boxMarginPercent:10                   //(v.1.21) Item Box의 좌/우 여백 비율 : default (10%) 
* valueFontColor:"rgba(0, 0, 0, 1)"     //(v.1.21) value의 색상 RGBA형태의 String사용,  ex: "rgba(0, 0, 0, 1)"
* userColor:["rgba(120, 64, 43, 0.64)","rgba(110, 164, 43, 0.64)"]   //(v.1.01) RGBA 형태의 String 배열 , index 0 = 컬럼 최하단, Alpha(0~1)

```js
var options = {
 guideAlpha: 0.2                            
 ,guideFillYN: "N"                          
 ,useComment: "Y"                           
 ,useGuideLine: "Y"                         
 ,onlyGroupBox: "N"                         
 ,legendNameSize:12                         
 ,xAxisNameSize:13                          
 ,valueFontSize:14                          
 ,displayValueComma: "Y"                    
 ,useDisplayValue: "Y"                      
 ,useValueUnit: 1000                        
 ,boxMarginPercent:10                       
 ,valueFontColor:"rgba(0, 0, 0, 1)"   
 ,userColor:["rgba(120, 64, 43, 0.64)","rgba(110, 164, 43, 0.64)","rgba(180, 184, 103, 0.64)"]   
};
myChart.init(DATA, options);
```

## Copyright

Copyright 2018. techabler@gmail.com [KOSITV Project](http://www.kositv.com).
