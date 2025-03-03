# 🔥🔥G6 5.0 Beta is Released！🔥🔥

## **💻 Try it Online **

[v5 Site](https://g6-next.antv.antgroup.com/en/) | [Features Demos](https://g6-next.antv.antgroup.com/en/examples)

[Beta Published Content](https://g6-next.antv.antgroup.com/en/manual/beta-publish) | [How to Use the Features](https://g6-next.antv.antgroup.com/manual/en/new-features)

[How to Upgrade](https://g6-next.antv.antgroup.com/en/manual/upgrade)


## **🌌 v5 Screen Shots **

[See the Full Image](https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*qPrmQrdV77gAAAAAAAAAAAAADmJ7AQ/original)

<img src="https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*IUOnSbLisyoAAAAAAAAAAAAADmJ7AQ/original" width=600 height=334 alt='' />

[See the Full Image](https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*1BFvQ4r3P7UAAAAAAAAAAAAADmJ7AQ/original)


<img src="https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*tPPGSokdSYsAAAAAAAAAAAAADmJ7AQ/original" width=600 height=367 alt='' />


# G6: A Graph Visualization Framework in TypeScript

![](https://user-images.githubusercontent.com/6113694/45008751-ea465300-b036-11e8-8e2a-166cbb338ce2.png)

[![travis-ci](https://img.shields.io/travis/antvis/g6/master.svg)](https://travis-ci.org/antvis/g6) [![codecov](https://codecov.io/gh/antvis/G6/branch/master/graph/badge.svg)](https://codecov.io/gh/antvis/G6) ![typescript](https://img.shields.io/badge/language-typescript-red.svg) ![MIT](https://img.shields.io/badge/license-MIT-000000.svg) [![npm package](https://img.shields.io/npm/v/@antv/g6.svg)](https://www.npmjs.com/package/@antv/g6) [![NPM downloads](http://img.shields.io/npm/dm/@antv/g6.svg)](https://npmjs.org/package/@antv/g6) [![Percentage of issues still open](http://isitmaintained.com/badge/open/antvis/g6.svg)](http://isitmaintained.com/project/antvis/g6 'Percentage of issues still open')

[中文 README](README.md)

## What is G6

[G6](https://github.com/antvis/g6) is a graph visualization engine, which provides a set of basic mechanisms, including rendering, layout, analysis, interaction, animation, and other auxiliary tools. G6 aims to simplify the relationships, and help people to obtain the insight of relational data. Developers are able to build graph visualization **analysis** applications or graph visualization **modeling** applications easily.

<img src='https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*_PJ5SZELwq0AAAAAAAAAAAAADmJ7AQ/original' width=550 alt='' />

<img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*zTjwQaXokeQAAAAAAAAAAABkARQnAQ' width=550 alt='' />

<img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*zau8QJcVpDQAAAAAAAAAAABkARQnAQ' height=200 alt='' /><img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*RIlETY_S6IoAAAAAAAAAAABkARQnAQ' height=200 alt='' />

<img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*cDzXR4jIWr8AAAAAAAAAAABkARQnAQ' height=150 alt='' /><img src='https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*HTasSJGC4koAAAAAAAAAAABkARQnAQ' height=150 alt='' />

<img src="https://user-images.githubusercontent.com/6113694/44995293-02858600-afd5-11e8-840c-349e4730d63d.gif" height=150 alt='' /><img src="https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*I9OdTbXJIi0AAAAAAAAAAABkARQnAQ" height=150 alt='' /><img src="https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*xoufSYcjK2AAAAAAAAAAAABkARQnAQ" height=150 alt='' />


## Features

- Abundant Built-in Items: Nodes and edges with free configurations;
- Steerable Interactions: More than 10 basic interaction behaviors ;
- Powerful Layout: More than 10 layout algorithms;
- Convenient Components: Outstanding ability and performance;
- Friendly User Experience: Complete documents for different levels of user requirements. TypeScript supported.

G6 concentrates on the principle of 'good by default'. In addition, the custom mechanism of the item, interation behavior, and layout satisfies the customazation requirements.

<img src='https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*V0a9SoDnLHwAAAAAAAAAAAAADmJ7AQ/original' width=1000 alt='' />

> Abundant Built-in Items

## Installation

```bash
$ npm install @antv/g6
```

## Usage

<img src="https://gw.alipayobjects.com/mdn/rms_f8c6a0/afts/img/A*khbvSrptr0kAAAAAAAAAAABkARQnAQ" width=437 height=148 alt='' />

```js
import G6 from '@antv/g6';

const data = {
  nodes: [
    {
      id: 'node1',
      label: 'Circle1',
      x: 150,
      y: 150,
    },
    {
      id: 'node2',
      label: 'Circle2',
      x: 400,
      y: 150,
    },
  ],
  edges: [
    {
      source: 'node1',
      target: 'node2',
    },
  ],
};

const graph = new G6.Graph({
  container: 'container',
  width: 500,
  height: 500,
  defaultNode: {
    type: 'circle',
    size: [100],
    color: '#5B8FF9',
    style: {
      fill: '#9EC9FF',
      lineWidth: 3,
    },
    labelCfg: {
      style: {
        fill: '#fff',
        fontSize: 20,
      },
    },
  },
  defaultEdge: {
    style: {
      stroke: '#e2e2e2',
    },
  },
});

graph.data(data);
graph.render();
```

[![Edit compassionate-lalande-5lxm7](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/compassionate-lalande-5lxm7?fontsize=14&hidenavigation=1&theme=dark)

For more information of the usage, please refer to [Getting Started](https://g6.antv.antgroup.com/en/manual/getting-started).

## Development

```bash
$ npm install

# lerna bootstrap for multiple packages
$ npm run bootstrap

# build the packages
$ npm run build:all

# if you wanna watch one of the packages, e.g. packages/core
$ cd ./packages/core
$ npm run watch

# run test case
$ npm test

# run test case in watch mode
npm test -- --watch ./tests/unit/algorithm/find-path-spec
DEBUG_MODE=1 npm test -- --watch ./tests/unit/algorithm/find-path-spec
```

## Documents

- <a href='https://g6.antv.antgroup.com/en/manual/tutorial/preface' target='_blank'>Tutorial</a>
- <a href='https://g6.antv.antgroup.com/en/manual/middle/overview' target='_blank'>Middle Guides</a>
- <a href='https://g6.antv.antgroup.com/en/manual/advanced/coordinate-system' target='_blank'>Further Reading</a>
- <a href='https://g6.antv.antgroup.com/en/api/graph' target='_blank'>API Reference</a>

## React project integration

For React project integration, we have an independent product recommendation: [Graphin](https://graphin.antv.vision), which is a toolkit based on G6 and React, that focuses on relational visual analysis. It's simple, efficient, out of the box.

At present, Graphin has good practices in business graph analysis projects. For details, see [《Who uses Graphin》](https://github.com/antvis/Graphin/issues/212)

## Online Analysis Tool：G6VP

If you have a piece of relational data (graph data) and want to quickly visualize it online and analyze it efficiently, then we recommend using the official [G6VP](https://github.com/antvis/G6VP), which supports local File JSON, Excel, and graph data sources such as TuGraph, Neo4J, and GraphScope are also supported. With 60+ built-in analysis assets, graph analysis can be as simple as building blocks. The platform also provides one-click export of SDK, which can be quickly integrated into the business system

![G6VP Image](https://mdn.alipayobjects.com/huamei_qa8qxu/afts/img/A*GOVySaZ1iHYAAAAAAAAAAAAADmJ7AQ/original)

## G6 Communication Group

Welcome to join the **G6 Communication Group** or **G6 Communication Group-2** (DingTalk groups). We also welcome the github issues.

<p>
  <a href="https://mdn.alipayobjects.com/mdn/huamei_qa8qxu/afts/img/A*yCTQR78ipZEAAAAAAAAAAAAADmJ7AQ" >
    <img src='https://mdn.alipayobjects.com/mdn/huamei_qa8qxu/afts/img/A*yCTQR78ipZEAAAAAAAAAAAAADmJ7AQ' style='width:250px;display:inline-block;vertical-align:top;' alt='' />
  </a>
  <a href="https://mdn.alipayobjects.com/mdn/huamei_qa8qxu/afts/img/A*WVxyRpjxrEMAAAAAAAAAAAAADmJ7AQ" >
    <img src='https://mdn.alipayobjects.com/mdn/huamei_qa8qxu/afts/img/A*WVxyRpjxrEMAAAAAAAAAAAAADmJ7AQ' style='width:250px;display:inline-block;vertical-align:top;' alt='' />
  </a>
  <a href="https://graphin.antv.vision/" >
   <img src='https://camo.githubusercontent.com/5e6624abcdde991f9fd89fce4933ad133a48d8fb603d1852c670da329df73ef7/68747470733a2f2f67772e616c697061796f626a656374732e636f6d2f6d646e2f726d735f3430326331612f616674732f696d672f412a2d717a6f54704c672d3163414141414141414141414141414152516e4151' style='width:250px;display:inline-block;vertical-align: top;' alt='' />
  </a>
</p>
## How to Contribute

Please let us know what you are you going to help. Do check out [issues](https://github.com/antvis/g6/issues) for bug reports or suggestions first.

## License

[MIT license](./LICENSE).
