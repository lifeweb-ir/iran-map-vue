# Iran Map Vue

[![NPM version][npm-version-image]][npm-url] [![NPM downloads][npm-downloads-size-image]][npm-url] [![NPM downloads][npm-downloads-image]][downloads-url] [![MIT License][license-image]][license-url]


![Iran Map Vue](https://unpkg.com/iran-map-vue@1.0.2/iran-map-vue.gif)

Iran svg map... :)

* [Installation](#installation)
* [Usage](#usage)
* [Props](#props)
* [MapData](#mapdata)
* [License](#license)
* [Author](#author)

## Installation

```bash
npm i iran-map-vue
```


## Usage
```js
<template>
    <iran-map-vue
      :click="_clickMap"
      :hover="_hoverMap"
      :data="provinces"
      border-color="#999"
      lake-color="#8dccc9"
      sea-color="#8dccc9"
      width="100%"
    />
</template>

<script>
import IranMapVue from 'iran-map-vue'
export default {
  name: 'DemoIranMap',
  components: { IranMapVue },
  data() {
    return {
      provinces: { Isfahan:{ color: '#3e3ec9'} },
    }
  },
  methods: {
    _hoverMap(item) {
      console.log(item)
    },
    _clickMap(item) {
      console.log(item)
    },
  },
}
</script>
```



## Props
```
{
      data: {
        type: Object,
        default() {
          return {
                Tehran:{
                    color: '#000',
                    stroke: '#333',
                    strokeWidth: '4px',
                    opacity: 0.5,
                    bgColor: '#f00',
                    bubbleColor: '#00f',
                    content : `<span>Tehran</span>`,
                    count: 1000,
                }
            };
        },
      },
      width: {
        type: String,
        default: '400px',
      },
      fontSize: {
        type: String,
        default: '12px',
      },
      borderColor: {
        type: String,
        default: '#333',
      },
      seaColor: {
        type: String,
        default: '#007de5',
      },
      lakeColor: {
        type: String,
        default: '#007de5',
      },
      islandColor: {
        type: String,
        default: '#cfcfcf',
      },
      provinceColor: {
        type: String,
        default: '#e1e1e1',
      },
      bubbleColor: {
        type: String,
        default: '#996666',
      },
      color: {
        type: String,
        default: '#333',
      },
      click: {
        type: Function,
        default: undefined,
      },
      hover: {
        type: Function,
        default: undefined,
      },
      showBgColor: {
        type: Boolean,
        default: true
      },
      showBubble: {
        type: Boolean,
        default: false,
      },
      showCount: {
        type: Boolean,
        default: false,
      },
      showContent: {
        type: Boolean,
        default: false,
      },
      maxCount:{
        type: Number,
        default: 0
      },
      minCount:{
        type: Number,
        default: null
      },
    }
```




## MapData 
```shell script
   // island
  AbuMusa: { ... },
  FarorBig: { ... },
  FarorSmall: { ... },
  Hendorabi: { ... },
  Hengam: { ... },
  Hormoz: { ... },
  Khark: { ... },
  Kish: { ... },
  Lark: { ... },
  Lavan: { ... },
  Qeshm: { ... },
  Siri: { ... },
  TunbBig: { ... },
  TunbSmall: { ... }

  // lake
  Jazmourian: { ...},
  Lake_Qom: { ... },
  Urmia: { ... }

  // province
  Alborz: { ... },
  Ardabil: { ... },
  AzerbaijanEast: { ... },
  AzerbaijanWest: { ... },
  Bushehr: { ... },
  ChaharMahaalBakhtiari: { ... },
  Fars: { ... },
  Gilan: { ... },
  Golestan: { ... },
  Hamadan: { ... },
  Hormozgan: { ... },
  Ilam: { ... },
  Isfahan: { ... },
  Kerman: { ... },
  Kermanshah: { ... },
  KhorasanNorth: { ... },
  KhorasanRazavi: { ... },
  KhorasanSouth: { ... },
  Khuzestan: { ... },
  KohgiluyehBoyerAhmad: { ... },
  Kurdistan: { ... },
  Lorestan: { ... },
  Markazi: { ... },
  Mazandaran: { ... },
  Qazvin: { ... },
  Qom: { ... },
  Semnan: { ... },
  SistanBaluchestan: { ... },
  Tehran: { ... },
  Yazd: { ... },
  Zanjan: { ... },

  // sea
  Caspian: {...},
  PersianGulf: { ... }

```


## License

MIT



### author
> Javad Shariati [jsh1400](https://www.npmjs.com/~jsh1400)

---
> [Lifeweb Company] <lifeweb.webapp@gmail.com>


[license-image]: http://img.shields.io/npm/l/iran-map-vue.svg?style=flat
[license-url]: LICENSE

[npm-url]: https://npmjs.org/package/iran-map-vue
[npm-version-image]: http://img.shields.io/npm/v/iran-map-vue.svg?style=flat
[npm-downloads-image]: http://img.shields.io/npm/dm/iran-map-vue.svg?style=flat
[npm-downloads-size-image]: https://img.shields.io/bundlephobia/minzip/iran-map-vue.svg?style=flat
[downloads-url]: https://npmcharts.com/compare/iran-map-vue?minimal=true


