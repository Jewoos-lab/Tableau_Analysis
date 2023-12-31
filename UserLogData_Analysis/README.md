

<div align="center">
  <h1>📝 Tableau 활용 개인 프로젝트<br><br>
   ✍ 2021년 사용자 로그데이터를 활용한 마케팅 분석</h1>
</div>

<h4> 💭 Language : Python <br><br>
     🛠  Tool : Google Colab, Tableau <br><br>
     📅 진행기간 : 2023.07.24 ~ 2023.07.28</h4>
  
<br>

# 💡 분석 기획
* 쇼핑몰 유료 검색 켐페인 데이터 활용<br>

* Python을 사용하여 분석에 필요한 컬럼 생성 및 누락된 값 확인, 중복 데이터 확인, 데이터 유형 변경 등 전처리 시행<br>

* 전처리된 데이터를 기반으로 Tableau를 사용하여 시각화 진행<br>

* <strong>총 비용 / 총 수익 / 총 손익 / 평균 전환율 / 평균 클릭률 값</strong>을 기반으로 켐페인 기간동안<br> <strong>총 비용 및 수익 추세 / 클릭수 및 노출수 추세 / CPM, CPC, CPA의 동향 / 그룹당 전환수 / 전반적인 노출수 실적 / 전체 CPM 실적 / 전반적인 클릭률 성과 / 전체 CPA 실적 / 전체 총비용 성능 / 수전체 수익 실적 / 전반적인 ROI 성과 / ROAS</strong> 등을 분석<br>

* 쇼핑몰 유료 검색 켐페인 데이터를 Tableau로 나타낸 시각화를 기반으로 데이터 분석하여 새로운 인사이트 도출<br><br>

<br>

# 🔥 목표
* 마케팅 관리자를 위한 대시보드를 만들어 마케팅 부서가 사용된 지표를 기반으로 수행된 캠페인 광고의 결과를 분석하는데 도움이 됨

* 마케팅 관리자가 가장 효과적인 성과를 제공하는 광고를 분석하고 최적화할 수 있는 광고를 결정하는 데 도움이 되도록 기간별 광고 비교가 포함된 데이터 시각화 진행

<br><br>


# 🔎 데이터 수집
|데이터셋|출처|
|------|:------:|
|쇼핑몰 유료 검색 캠페인 데이터|Kaggle|

<br><br>

# 🔎 컬럼명
|컬럼|컬럼명|
|------|:------|
|AD Group|광고의 카테고리|
|Devices|클릭할 때 이용한 장치|
|Match Type|성별|
|Month|캠페인의 월|
|Clicks|클릭수|
|Conv Rate|전환율 (광고를 클릭한 후 제품을 구매하는 방문자의 비율)|
|Conversions|전환 (방문자의 구매 행동)|
|Cost|비용 (회사에서 광고 그룹에 발생한 비용)|
|CPC|클릭당 비용 (특정 광고의 비용을 클릭으로 나눈 값)|
|CTR|클릭률 (조회한 광고 수와 비교한 클릭수 (클릭수 / 노출수))|
|Impressions|인상 (광고의 디지털 조회수 또는 참여수를 정량화하기 위해 디지털 마케팅에서 사용되는 메트릭)|
|P&L|손익 (광고그룹에서 파상된 수익/손실 (수익 - 비용))|
|Revenue|수익 (광고로 인해 발생한 총 수익)|
|Sale Amount|판매량|

<br><br>

# 🔎 파생 변수 생성
|파생 변수|생성 이유|
|------|:------|
|Month(copy)|날짜를 월로 나타내기 위해 컬럼 생성|
|CPA (발생한 비용을 총 전환수로 나눈값)|광고 효과의 실질적인 파악을 위해 컬럼 생성|
|CPM (1000회 노출로 발생한 비용)|인지도와 참여도를 높여 가시성을 향상시키기 위해 컬럼 생성|
|ROAS (수익을 총 비용으로 나눈값)|총 비용 대비 수익 비율을 분석하기 위해 컬럼 생성|
|ROI (손익을 총 비용으로 나눈값)|총 비용 대비 손익 비율을 분석하기 위해 컬럼 생성|
|Select Label (특정 라벨 선택)|특정 라벨을 선택을 위한 컬럼 생성|
|Select Measure Logic (특정 컬럼 선택)|특정 컬럼 선택을 위한 컬럼 생성|

<br><br>

# 📊 데이터 분석 및 인사이트
## 1) 캠페인 기간동안 총 클릭 수

<br>

<h3 align="center"><img width="304" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/70240882-f611-4bf4-8bd8-a0c0aab0600e">
</h3>

<br>

* 전체적으로 총 클릭 수는 924,503회였으며, 11월에 가장 많은 클릭 수를 기록했으며 총 380,920회의 클릭이 있었음

* 가장 적은 클릭 수는 10월이었으며, 총 116,711회의 클릭이 있었음

<br><br>

## 2) 캠페인 기간동안 발생한 총 비용

<br>

<h3 align="center"><img width="308" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/d6b38047-4d94-4158-974a-42ed266ff39b">
</h3>

<br>

* 캠페인 기간 동안 발생한 총 비용은 $635,372였으며, 11월에 가장 높은 비용으로 $280,753이 소요

* 가장 적은 비용은 9월에 발생하였으며, 총 $71,597이 사용됨

<br><br>

## 3) 캠페인 기간 동안 총 수익 

<br>

<h3 align="center"><img width="305" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/7eab01fe-c4e9-4666-9e9b-efbf7365c276">
</h3>

<br>

* 캠페인 기간 동안 총 수익은 $561,960이었으며, 11월에 가장 높은 수익으로 $252,833을 기록

* 가장 적은 수익은 9월에 발생하였으며, 총 $59,093임

<br><br>

## 4) 캠페인 기간 동안 벌어들인 총 손익

<br>

<h3 align="center"><img width="307" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/cf90a4f7-e043-4092-b4fa-adc601b34902">
</h3>

<br>

* 캠페인 기간 동안 총 P&L(손익 계산서)은 $73,409의 손실
  
* 이 회사는 전체적으로는 10월에 $1,046의 이익을 창출했지만, 캠페인 기간 동안 가장 큰 손실은 7월에 -$21,923이었음
  
* 이는 총 수익이 회사가 발생한 총 캠페인 비용보다 낮기 때문
  
* 11월에 매우 높은 수익을 올렸지만, 여전히 총 수익은 회사가 발생한 총 캠페인 비용보다 낮았음
  
* 따라서 이 문제는 더 깊이 분석해야 할 필요가 있고, 추가적인 조치나 전략적 개선이 필요할 수 있음

<br><br>

## 5) 캠페인 기간 동안의 평균 전환율 

<br>

<h3 align="center"><img width="286" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/7b68d05b-bc02-4c44-9f3e-3a2896e9489c">
</h3>

<br>

* 평균 전환율은 7.97%를 나타냄
 
* 10월에 가장 높은 전환율은 8.7%였고, 8월에 가장 낮은 전환율은 7.05%였음
 
* 또한, 평균 전환율은 3.75%라는 기준선보다 높음

<br><br>

## 6) 캠페인 기간 동안 클릭률 

<br>

<h3 align="center"><img width="303" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/b958bdfa-c452-4419-8bbf-a70a2da4812f">
</h3>

<br>

* 캠페인 기간 동안의 CTR(클릭률)은 27.21%로, 이미 CTR 기준선인 3.17%를 월등히 초과
 
* 특히 9월에 가장 높은 CTR인 28.53%를 기록
 
* 9월은 캠페인 비용과 총 수익이 감소한 달이지만, 캠페인 기간 동안 가장 높은 평균 CTR을 보여줌
 
* 가장 낮은 CTR은 8월에 27.37%를 기록
 
* 이는 광고가 사용자들에게 "클릭"을 유도하는 데 성공했음을 보여줌
 
* 하지만 전환과 판매를 증가시키기 위해 어떤 부분을 개선해야 하는지를 파악하기 위해 추가적인 분석 필요

<br><br>

## 7) 캠페인 기간 동안의 총 비용 및 수익 추세 

<br>

<h3 align="center"><img width="512" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/25ef4212-7d83-4536-8183-5b7b772057a1">
</h3>

<br>

* 시각화를 통해 캠페인 기간 동안의 데이터를 살펴보면, 8월부터 9월로 이동할 때까지 총 비용이 감소하고 그에 따라 얻은 수익도 감소함
  
* 그러나 10월은 캠페인 비용이 9.03% 증가했지만, 해당 달에는 수익이 비용을 초과하여 이익이 발생함
  
* 실제로 수익은 34.2% 증가하였고, 11월에는 비용이 매우 크게 증가했지만, 수익은 여전히 사용한 비용보다 낮았음

<br><br>

## 8) 캠페인 기간 동안의 클릭수 및 노출수 추세

<br>

<h3 align="center"><img width="495" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/37de02df-ca47-49ae-937a-933dff0c812a">
</h3>

<br>

* 시각화를 통해 살펴보면, 7월부터 8월까지 인상 및 클릭 수가 감소하는 추세를 보임

* 이는 캠페인 비용이 감소하여 만들어진 캠페인의 품질에 영향을 미친 것으로 보여짐

* 10월에는 캠페인 비용이 증가하면서 인상과 클릭 수도 증가함

* 11월에는 인상 수와 총 클릭 수 간에 큰 차이가 있음

* 이는 11월에 만들어진 광고가 우리의 타겟 시장의 관심을 끌지 못하여 "클릭"하지 않았을 가능성이 있음

* 따라서 11월에 제작된 캠페인에 대해 추가적인 분석이 필요함

<br><br>

## 9) 캠페인 기간 동안 CPM, CPC, CPA의 동향

<br>

<h3 align="center"><img width="486" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/30b843be-a71e-4459-aa7f-730ee4f2c8b7">
</h3>

<br>

* 평균 CPC는 캠페인 기간 동안 $0.8이었고, 이는 $2.69인 기준값보다 낮았음

* 그러나 캠페인 기간 동안, CPC 값은 $0.8로 일정하게 유지되었음

* 평균 CPA는 캠페인 기간 동안 변동이 있었고, 가장 낮은 CPA는 10월에 $6.7이었고, 가장 높은 CPA는 7월에 $8.9였음

* CPM은 7월부터 9월까지 증가했고, 10월에는 감소하였으며, 11월에는 가장 낮은 $196.7이었음

* 가장 높은 CPM은 9월에 $234.4이었음

* 7월의 높은 CPA와 9월의 높은 CPM은 개선할 필요가 있음

<br><br>

## 10) "Devices"와 "Math Type" 기준으로 볼 때, 가장 높은 총 전환이 발생하는 광고 그룹

<br>

<h3 align="center"><img width="497" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/772add4a-60b9-4e8a-8055-a07190a5b0f9">
</h3>

<br>

* 광고 그룹을 기준으로 보면, "coupons," "promos," 그리고 "discounts"와 관련된 광고들이 모바일 기기를 통해 가장 높은 총 전환을 기록함
  
* 광고 그룹 "coupon"이 넓은 매치 키워드로 보았을 때, 모바일 기기를 통해 가장 많은 총 전환을 기록했습니다. 그 뒤를 이어 "promos"와 "discounts"가 따름

<br>

<h3 align="center"><img width="497" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/a0cc2e8c-5033-48f3-a163-20b43a71678c">

</h3>

* 정확한 매치 키워드로 보았을 때, 가장 높은 총 전환을 기록한 광고 그룹은 "promos"이며, 그 뒤를 이어 "coupons"가 따랐음, 모바일 기기가 가장 많이 사용됨

* 구문 매치 키워드로 보았을 때, 가장 높은 총 전환은 "promos" 광고 그룹이며, 그 뒤를 이어 "coupons"와 "offers"가 따랐음, 대부분의 기기는 데스크톱을 통해 사용되었음

<br><br>

## 11) 광고 그룹, 기기 및 일치 유형을 기반으로 하는 전체 전환/의사 결정 지표

<br>

<h3 align="center"><img src= "https://github.com/LHG-Git/Ecommerce_Paid_Search_Marketing_Analysis/assets/100845169/cbdfe7b8-eb4f-4b96-9d3d-8745a4b9d426"></h3>

<br>

* 전반적으로, 모바일 기기에서 가장 높은 인상(노출)을 기록했습니다.
  
* 총 노출 수는 1,916,806회이며, 매치 유형은 넓은 매치 키워드로 1,755,536회이고, 광고 그룹은 쿠폰, 프로모션 및 할인과 관련된 것임

<br>

<h3 align="center"><img width="719" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/2af69e3e-8432-43f9-af11-e13326ac4a8c">

/h3>

* 전체적으로, 가장 높은 CTR(클릭률)은 광고 그룹 쿠폰이 35.75%, 프로모션은 35.45%, 그리고 할인은 27.45%로 모바일 기기에서 나타났으며, 넓은 매치 키워드와의 일치율이 1:1인 경우 CTR은 38.7%입니다. 캠페인 월별로 볼 때, 가장 높은 CTR은 9월에 있었음

<br><br>

<h3 align="center"><img src= "https://github.com/LHG-Git/Ecommerce_Paid_Search_Marketing_Analysis/assets/100845169/ea5ebae0-b154-4ce2-aa1c-3938fe5ea4da"></h3>

* 가장 낮은 CPA(클릭당 비용)는 광고 그룹 "Black Friday/Cyber Monday"에서 $1.13이었으며, 그 뒤를 이어 "free shipping"이 $3.31이고, "promo"가 $6.72였음
  
* 또한, 가장 낮은 CPA는 넓은 매치 키워드를 통한 광고 그룹에서 $6.67이었고, 데스크톱 기기를 통해 이루어진 광고에서 발생했음
  
* 캠페인 월별로 볼 때, 가장 낮은 CPA는 11월에 있었음

<br><br>

# 📋 결론
* 5개월간의 평균 전환율을 기준으로 보면, 전환율 값은 기준선인 7.97%를 초과하고 있습니다.

* 캠페인 기간 동안의 CTR(클릭률) 값을 기준으로 보면, 평균 CTR은 기준값인 27.21%보다 높습니다.

* 캠페인 기간 동안의 CPC(클릭당 비용) 값을 기준으로 보면, 평균 CPC는 $0.8보다 낮습니다.

* 전반적으로, 총 P&L을 기준으로 보면, 회사는 $73,409의 손실을 겪었습니다. 이는 캠페인 성과를 평가한 결과, 해당 지표가 업계 평균 기준값을 초과하고 있기 때문에 재평가가 필요하다는 것을 의미합니다. 따라서 회사는 제품 가격 전략을 재평가해야 할 필요가 있습니다.

* 12월에 회사가 인지 단계에 초점을 맞추고자 한다면, 광고 그룹 "Sale"을 사용할 수 있습니다. 월간 추이를 보면, 광고 그룹 "Sale"이 넓은 매치 키워드를 사용하여 가장 낮은 CPM 값을 가지고 있습니다.
  
* 12월에 회사가 고려 단계에 초점을 맞추고자 한다면, 광고 그룹 "promos"와 "free shipping"을 사용할 수 있습니다.
  
* 12월에 회사가 전환/결정 단계에 초점을 맞추고자 한다면, 광고 그룹 "free shipping"을 사용할 수 있습니다.

<br><br>

# 📈 최종 대시보드
<h3 align="center"><img width="472" alt="image" src="https://github.com/Jewoos-lab/Tableau_Analysis/assets/86662870/0ba3b4e6-8638-49f4-973a-b37abbc4fadb">

</h3>

[태블로 바로가기] : https://public.tableau.com/app/profile/heegu.lee/viz/PaidSearchMarketingDashboard_16900438709420/Dashboard
