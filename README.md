# react-donut 🍩

Simple and customizable doughnut chart component for react projects.

## Installation

[![NPM version](https://img.shields.io/badge/npm-1.0.3-brightgreen.svg)](https://www.npmjs.com/package/react-donut)

Using npm:

```
npm install react-donut
```

### Codesandbox demo [here](https://codesandbox.io/embed/10p5rkyooj)

## Screenshots
![Donut](https://i.imgur.com/vpxUlBh.png)

## API

### props

<table class="table table-bordered table-striped">
  <thead>
  <tr>
    <th style="width: 60px;">name</th>
    <th style="width: 50px;">type</th>
    <th style="width: 10px;">default</th>
    <th>description</th>
  </tr>
  </thead>
  <tbody>
    <tr>
      <td>chartData</td>
      <td>Array</td>
      <td>Dummy array of objects</td>
      <td>To supply actual data with `name` as name and `data` as total data of that item. This is actually array of objects</td>
    </tr>
    <tr>
      <td>chartWidth</td>
      <td>Number</td>
      <td>400</td>
      <td>Specifies width of Doughnut Chart</td>
    </tr>
    <tr>
      <td>chartHeight</td>
      <td>Number</td>
      <td>400</td>
      <td>Specifies height of Doughnut Chart</td>
    </tr>
    <tr>
      <td>title</td>
      <td>String</td>
      <td>'Usage of browsers'</td>
      <td>Title for chart</td>
    </tr>
    <tr>
      <td>chartRadiusRange</td>
      <td>Array</td>
      <td>["60%", "100%"]</td>
      <td>Radius range of outer and inner crust of donut </td>
    </tr>
   <tr>
      <td>showChartLabel</td>
      <td>Boolean</td>
      <td>true</td>
      <td>To enable visibility for chart label</td>
    </tr>
	   <tr>
      <td>legendAlignment</td>
      <td>String</td>
      <td>'bottom'</td>
      <td>Position for alignment of legend</td>
    </tr>
    <tr>
      <td>chartThemeConfig</td>
      <td>Object</td>
      <td>{}</td>
      <td>Custom chart theme config. Structure as shown below</td>
    </tr>
  </tbody>
</table>

## Config for theme

```ts
ThemeConfig {
    chart?: {
        fontFamily?: string;
        background?: string;
    };
    title?: {
        fontSize?: number;
        fontFamily?: string;
        fontWeight?: string;
        color?: string;
        background?: string;
    };
    yAxis?: {
        title?: TextStyleConfig;
        label?: TextStyleConfig;
        tickColor?: string;
    };
    xAxis?: {
        title?: TextStyleConfig;
        label?: TextStyleConfig;
        tickColor?: string;
    };
    plot?: {
        lineColor?: string;
        background?: string;
        label?: {
            fontSize: number;
            fontFamily: number;
            color: string;
        }
    };
    series?: {
        colors?: string[];
        borderColor?: string;
        selectionColor?: string;
        startColor?: string;
        endColor?: string;
        overColor?: string;
        ranges?: any[];
        borderWidth?: string;
        dot?: SeriesDotOptions;
    };
    legend?: {
        label?: TextStyleConfig;
    };
    tooltip?: any;
    chartExportMenu?: {
        backgroundColor?: string;
        borderRadius?: number;
        borderWidth?: number;
        color?: string
    };
}
```

## Usage

```js
import React from "react";
import ReactDOM from "react-dom";
import Donut from "react-donut";
import "./styles.css";

function App() {
  return (
    <div className="App">
      <h1>Hello CodeSandbox</h1>
      <Donut
        shouldRemainEqual={true}
        doughnutSize="large"
        doughnutparts={4}
        paintShades={{
          c1: "#D1A917",
          c2: "#2C9DC2",
          c3: "#D12A6A",
          c4: "#535353",
          c5: "#AC6946"
        }}
        pievalues={{
          p1: 5,
          p2: 20,
          p3: 25,
          p4: 30,
          p5: 20
        }}
      />
    </div>
  );
}

const rootElement = document.getElementById("root");
ReactDOM.render(<App />, rootElement);
```
