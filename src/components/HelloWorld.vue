<template>
  <div class="container">
   <ele-calendar
          lang="en"
          :render-content="renderContent"
          :data="datedef"
          :prop="prop"
    ></ele-calendar>
  </div>
</template>

<script>
import eleCalendar from 'ele-calendar'
import 'ele-calendar/dist/vue-calendar.css'
import './style.scss'
export default {
  name: 'HelloWorld',
  data () {
    return {
      datedef:[
          {"date":"2019-09-30","content":"1212","cid":"aaa"},
          {"date":"2019-09-26","content":null,"cid":null},
      ],
      prop:'date' //对应日期字段名
    }
  },
  components: {
      eleCalendar
  },
  methods: {
    renderContent(h,parmas) {
      console.log(h,parmas)
      const loop = data =>{
        return (
          data.defvalue.column===0||data.defvalue.column===6?
          <div>
            <div style="color:red;">休</div>
            <div class="remark">
              <div><span>{data.defvalue.text}</span></div>
              <div>加班</div>
            </div>
          </div> 
          : 
          <div>
            <div>班</div>
            <div class="remark">
              <div><span>{data.defvalue.text}</span></div>
              <div>调休</div>
            </div>
          </div>
        )
      }
      return (
      <div>
        {loop(parmas)}
      </div>
      );
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
</style>
