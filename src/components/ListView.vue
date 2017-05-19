<template>
  <div class="list-box">
    <div class="list-bar">
      <h4 class="list-bar-title">播放列表</h4>
      <button class="button-add list-bar-button"></button>
    </div>
    <div class="list-scroller" id="list-scroller">
      <scroller 
        :on-refresh="refresh"
        :on-infinite="infinite">
        <!-- content goes here -->
        <ul class="list" id="list">
          <li class="item">
            <span class="item-index">1</span>
            <a class="item-title">����</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          <li class="item">
            <span class="item-index">2</span>
            <a class="item-title">��������</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          <li class="item">
            <span class="item-index">3</span>
            <a class="item-title">ϲ����</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          <li class="item">
            <span class="item-index">4</span>
            <a class="item-title">����֮��</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          <li class="item">
            <span class="item-index">5</span>
            <a class="item-title">Light Up the Way</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          <li class="item">
            <span class="item-index">6</span>
            <a class="item-title">��������</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          <li class="item">
            <span class="item-index">7</span>
            <a class="item-title">ʮ��</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          <li class="item">
            <span class="item-index">8</span>
            <a class="item-title">���ı���</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          <li class="item">
            <span class="item-index">9</span>
            <a class="item-title">�ж��ٰ���������</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          <li class="item">
            <span class="item-index">10</span>
            <a class="item-title">�Ƹ�������</a>
            <div class="item-check"><input type="checkbox"></div>
          </li>
          
        </ul>
      </scroller>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  mounted () {
    this.$nextTick(() => {
    })
  },
  methods: {
    refresh () {
    },
    infinite () {
    }
  }
}
</script>

<style lang="scss" scoped>
.button-add {
    background: url(../../static/img/plus.png) no-repeat 50% 50%;
    background-size: 14px 14px;
}
.list-box {
    position: relative;
    float: left;
    width: 400px;
    height: 480px;
    overflow: hidden;
    .list-bar {
        position: relative;
        z-index: 2;
        height: 50px;
        background-color: rgba(255,255,255,.95);
        border-bottom: solid 1px rgba(0,0,0,0);
        box-shadow: 0 0 8px rgba(0,0,0,.12);
        .list-bar-title {
            float: left;
            height: 50px;
            margin: 0;
            padding: 0 0 0 66px;
            font: normal 14px/50px 'Microsoft Yahei';
            color: #999;
            background: url(../../static/img/bars.png) no-repeat 18px 50%, url(../../static/img/line_gray.png) repeat-y 50px 0;
            background-size: 14px 14px, 1px 5px;
        }
        .list-bar-button {
            float: right;
            width: 50px;
            height: 50px;
            font-size: 14px;
            border: none;
            border-left: solid 1px #f5f5f5;
            outline: none;
            transition: .3s;
        }
    }
    .list-scroller {
        position: relative;
        height: calc(100% - 50px);
        background-image: url(../../static/img/dark_wood.png);
        overflow: hidden;
        .list {
            background-color: #fff;
            background-image: url(../../static/img/line_gray.png), url(../../static/img/line_gray.png);
            background-repeat: repeat-y;
            background-position: 50px 0, 350px 0;
            background-size: 1px 5px;
            box-shadow: 0 0 5px rgba(0,0,0,.1);
            .item {
                height: 50px;
                line-height: 50px;
                .item-index, .item-check{
                  width: 50px;
                  font-size: 12px;
                  color: #999;
                  text-align: center;
                }
                .item-title{
                  width: calc(100% - 100px);
                  font-size: 14px;
                  color: #666;
                  line-height: 50px;
                  text-indent: 18px;
                }
            }
            .item > *{
                display: block;
                float: left;
                height: 50px;
            }
            .item:nth-child(even){
                background-color: rgba(0,0,0,.025);
            }
        }
    }
}
</style>
