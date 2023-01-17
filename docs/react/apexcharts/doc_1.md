---
layout: default
title: 1_APEXCHART
grand_parent: 리액트
parent: APEXCHART
has_children: false
permalink: /docs/react/apexcharts/doc_1
nav_order: 1
---

### **APEXCHART**  


### **설치**  
```powershell
npm install apexcharts --save  
npm install react-apexcharts
```

### **사용방법**   
```js
import React from 'react';

import ApexCharts from 'react-apexcharts'

const LineChart = (props) => {
    const series =  [{
      name: "Desktops",
      data: [10, 41, 35, 51, 49, 62, 69, 91, 148]
  }];

  const options = {
    chart: {
      height: 350,
      type: 'line',
      zoom: {
        enabled: false
      }
    },
    dataLabels: {
      enabled: false
    },
    stroke: {
      curve: 'straight'
    },
    title: {
      text: 'Product Trends by Month',
      align: 'left'
    },
    grid: {
      row: {
        colors: ['#f3f3f3', 'transparent'], // takes an array which will be repeated on columns
        opacity: 0.5
      },
    },
    xaxis: {
      categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep'],
    }
  };

  return (
    <ApexCharts options={options} type="line" series={series} width="50%" />
  );
};

export default LineChart;
```


### **참고**  
> [ApexChart DOCS](https://apexcharts.com/docs/installation){:target="_blank"}