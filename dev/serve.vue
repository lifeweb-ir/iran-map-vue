<script>
  import Vue from 'vue';
  import IranMapVue from '../src/IranMapVue.vue';

  const color1 = '#f00'
  const color2 = '#00f'
  const color3 = '#0f0'
  export default Vue.extend({
    name: 'ServeDev',
    data() {
      return {
        data: {
          Tehran: {
            bgColor: color1,
            bubbleColor: color1,
            count: 70,
            content: '😡',
            color: '#000',
            opacity: 0.6
          },
          Fars: {
            bgColor: color1,
            bubbleColor: color2,
            count: 70,
            content: '😍',
            color: '#000',
            opacity: 0.8
          },
          Isfahan: {
            bgColor: color1,
            count: 80,
            bubbleColor: color2,
            content: '😍',
            color: '#000',
            opacity: 0.7
          },
          Kerman: {
            bgColor: color1,
            bubbleColor: color2,
            count: 65,
            content: '😍',
            color: '#000',
            opacity: 0.6
          },
          Lorestan: {
            bgColor: color1,
            bubbleColor: color2,
            count: 60,
            content: '😍',
            color: '#000',
            opacity: 0.5
          },
          Semnan: {
            bgColor: color1,
            bubbleColor: color2,
            count: 55,
            content: '😍',
            color: '#000',
            opacity: 0.4
          },
          Yazd: {
            bgColor: color1,
            bubbleColor: color2,
            count: 50,
            content: '😍',
            color: '#000',
            opacity: 0.9
          },
        },
        type: 'data1',
      };
    },
    components: {
      IranMapVue,
    },
  });
</script>

<template>
    <div id="app" style="
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;">
        <div>
            <button @click="type = 'data1'" >bubble</button>
            <button @click="type = 'data2'" >content</button>
            <button @click="type = 'data3'" >count</button>
            <button @click="type = 'data4'" >default</button>
        </div>
        <div style="display: inline-block; border: 1px solid #000; padding: 20px; margin: 20px ">
            <iran-map-vue
                    font-size="18px"
                    width="600px"
                    :data="data"
                    :show-bubble="type === 'data1'"
                    :show-content="type === 'data2'"
                    :show-count="type === 'data3'"
                    :show-bg-color="type === 'data4'"
            />
        </div>
    </div>
</template>
