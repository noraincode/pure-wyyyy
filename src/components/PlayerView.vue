<template>
  <div class="player-box">
    <div class="player-core">
      <div class="player-top"></div>
      <div class="player-body">
        <div class="artist-avatar" id="artist-avatar" >
          <div class="disc-center"></div>
        </div>
        <div class="song-info">
          <h2 class="song-title" id="song-title">喜欢你</h2>
          <h4 class="song-meta">
            <span id="artist-name">邓紫棋</span> / 
            <span id="album-name">喜欢你</span>
          </h4>
        </div>
        <div class="progress-wrap">
          <span class="time-current" id="time-current">01:36</span>
          <span class="time-total" id="time-total">03:44</span>
          <div class="progress-bar">
            <div class="progress-bar-indicator"></div>
          </div>
        </div>
      </div>
      <div class="player-controler">
        <button class="player-button button-mode mode-shuffle" id="button-mode"></button>
        <button class="player-button button-prev" id="button-prev"></button>
        <button class="player-button button-play" id="button-play"></button>
        <button class="player-button button-next" id="button-next"></button>
        <button class="player-button button-volumn" id="button-volumn"></button>
      </div>
    </div>
    <div class="album-background" id="album-background">
      <img class="new-album-background" src="../../static/img/singer.jpg">
      <img class="default-album-background" src="../../static/img/default_album.png">
    </div>
  </div>
</template>

<style lang="scss" scoped>
.player-box {
    position: relative;
    float: left;
    width: 400px;
    height: 480px;
    overflow: hidden;
    .player-core {
        position: absolute;
        z-index: 1;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        background-color: rgba(0,0,0,.45);
        .player-top {
            height: 40px;
        }
        .player-body {
            position: relative;
            z-index: 3;
            height: 350px;
            padding-top: 25px;
            .artist-avatar {
                width: 180px;
                height: 180px;
                margin: 0 auto 20px auto;
                border: solid 6px rgba(0,0,0,.3);
                border-radius: 50%;
                background-color: #111;
                background-clip: padding-box;
                background-size: cover;
                background-position: 50% 50%;
                background-image: url(../../static/img/singer.jpg);
                .disc-center {
                    width: 20px;
                    height: 20px;
                    margin: 65px auto;
                    background-color: #111;
                    border: solid 15px #3498DB;
                    border-radius: 50%;
                    box-shadow: inset 0 0 2px rgba(0,0,0,.6), 0 0 1px #000;
                }
            }
            .song-info {
                color: #fff;
                text-align: center;
                .song-title {
                    height: 20px;
                    margin: 0;
                    padding: 0;
                    font-size: 18px;
                    font-weight: normal;
                    line-height: 20px;
                }
                .song-meta {
                    height: 30px;
                    margin: 0;
                    padding: 0;
                    font-size: 14px;
                    font-weight: normal;
                    line-height: 30px;
                }
            }
            .progress-wrap {
                height: 25px;
                margin-top: 63px;
                .time-current, .time-total{
                  display: inline-block;
                  height: 20px;
                  font-size: 12px;
                  line-height: 20px;
                  color: #3498DB;
                }
                .time-current {
                    float: left;
                    margin-left: 10px;
                }
                .time-total {
                    float: right;
                    margin-right: 10px;
                }
                .progress-bar {
                    clear: both;
                    height: 5px;
                    overflow: hidden;
                    transition: .3s;
                    .progress-bar-indicator {
                        width: 44%;
                        height: 5px;
                        background-color: rgba(52,152,219,.2);
                        border-right: solid 1px rgba(52,152,219,.7);
                        transition: .5s;
                    }
                }
            }
        }
        .player-controler {
            height: 65px;
            background-color: rgba(0,0,0,.25);
            .player-button {
                display: block;
                float: left;
                width: 65px;
                height: 64px;
                border: none;
                background-color: transparent;
                background-repeat: no-repeat;
                background-position: 50% 50%;
                cursor: default;
                outline: none;
                opacity: .7;
                transition: .3s;
            }
            .mode-shuffle {
                background-image: url(../../static/img/shuffle.png);
            }
            .button-mode {
                background-size: 18px 18px;
            }
            .button-prev {
                margin-left: 37.5px;
                background-image: url(../../static/img/backward.png);
                background-size: 28px 28px;
            }
            .button-play {
                background-image: url(../../static/img/play.png);
                background-size: 36px 36px;
            }
            .button-next {
                background-image: url(../../static/img/forward.png);
                background-size: 28px 28px;
            }
            .button-volumn {
                float: right;
                background-image: url(../../static/img/volume-medium.png);
                background-size: 18px 18px;
            }
        }
    }
    .album-background {
        position: absolute;
        z-index: 0;
        top: -20px;
        right: -20px;
        bottom: -20px;
        left: -20px;
        background-position: 50% 50%;
        -webkit-filter: blur(10px);
        img {
            position: absolute;
            display: block;
            min-width: 100%;
            min-height: 100%;
        }
        .new-album-background {
            z-index: 1;
        }
        .default-album-background {
            z-index: 0;
        }
    }
}
</style>
