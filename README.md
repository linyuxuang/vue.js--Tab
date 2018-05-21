# vue.js--Tab
vue.js 写的选项卡





               <style>
              
                *{
                    margin: 0;
                    padding: 0;
                }
                #app{
                  width: 500px;
                  height: 300px;
                  background-color: darkgrey;
                   margin: 0 auto;
                }
                .xuanxiang{
                    float: left;
                }
                .xuanxiang .lop{
                    cursor: pointer;
                    width: 100px;
                    height: 60px;
                    line-height: 60px;
                    text-align: center;
                    margin-top: 30px;
                    box-sizing: border-box;
                }
                .texts{
                    float: left;
                }
                .texts span{
                  display: block;
                    width: 400px;
                    height: 300px;
                    background-color: chartreuse;
                }
                .cur{
                    background-color: red;
                }
            </style>

              <div id="app">
                  <div class="xuanxiang">
                      <div :class="{cur:lanm=='vue1'}" @click="chum('vue1')" class="lop">选项一</div>
                      <div :class="{cur:lanm=='vue2'}" @click="chum('vue2')" class="lop">选项二</div>
                      <div :class="{cur:lanm=='vue3'}" @click="chum('vue3')" class="lop">选项三</div>
                  </div>
                  <div class="texts">
                      <span v-show="lanm=='vue1'">选项一</span>
                      <span v-show="lanm=='vue2'">选项二</span>
                      <span v-show="lanm=='vue3'">选项三</span>
                  </div>
              </div>
              
              <script>
                  var vm=new Vue({
                      el:"#app",
                      data:{
                          lanm:'vue1'
                      },
                    methods:{
                        chum:function(str){
                           this.lanm=str;
                        }
                    }
                  })
              </script>
