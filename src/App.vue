<template>
    <div id="app">
        <div class="container">
            <header class="header">
                <h1 class="title">IT'S SHOW TIME <span class="face">∠( ᐛ 」∠)_ ...</span> </h1>
                <div class="link-container">
                    <ul class="list">
                        <li class="list-item">
                            <a class="blog-link" href="http://b-sirius.me/" target="_blank">SIRIUS'S GARAGE --></a>
                        </li>
                        <li class="list-item">
                            <a class="blog-link" href="https://github.com/B-sirius" target="_blank">GITHUB --></a>
                        </li>
                    </ul>
                </div>
            </header>
            <div class="content">
                <div class="work-container" v-for="work in workList">
                    <img :src="work.bg" class="bg">
                    <div class="work-info">
                        <div class="info-container">
                            <span class="dark">{{work.title}}</span>
                        </div>
                    </div>
                    <a class="link" :href="work.url" target="_blank"></a>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import musicPlayerBg from './assets/music-player.jpg';
import rushBBg from './assets/rushB.jpg';
import colorPickerBg from './assets/color-picker.jpg';

export default {
    data: function() {
        return {
            workList: [{
                title: 'MUSIC-PLAYER',
                bg: musicPlayerBg,
                url: 'http://music.b-sirius.me/'
            }, {
                title: 'RUSHB.JS',
                bg: rushBBg,
                url: 'http://rushb.b-sirius.me/'
            }, {
                title: 'COLOR-PICKER',
                bg: colorPickerBg,
                url: 'http://colorpicker.b-sirius.me/'
            }]
        }
    }
}
</script>
<style lang="scss">
$haxagonURL: "http://7xrkxs.com1.z0.glb.clouddn.com/garage/hexagon.svg";

#app {
    font-family: "Delius Unicase", cursive, "Microsoft Yahei", "Helvetica Neue", "Helvetica", "Arial", sans-serif;
    background: #26252A;
    .container {
        position: relative;
        max-width: 1200px;
        min-height: 100vh;
        margin: auto;
        padding: 40px 20px;
        .header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 50px;
            .link-container {
                display: flex;
                .list {
                    margin: auto;
                    display: flex;
                    flex-direction: column;
                    align-items: flex-end;
                    .list-item {
                        margin-bottom: 5px;
                        &:last-child {
                            margin: 0;
                        }
                        .blog-link {
                            color: #fff;
                            text-decoration: none;
                            font-size: 20px;
                        }
                    }
                }
            }
            .title {
                color: #fff;
                font-size: 64px;
                .face {
                    font-size: 20px;
                    vertical-align: 4px;
                }
            }
        }
        .content {
            display: flex;
            flex-wrap: wrap;
            justify-content: flex-start;
            .work-container {
                position: relative;
                width: 180px;
                height: 300px;
                background: #828282;
                margin-bottom: 60px;
                margin-right: 50px;
                border-radius: 15px;
                overflow: hidden;
                .bg {
                    position: absolute;
                }
                .work-info {
                    display: flex;
                    position: absolute;
                    width: 100%;
                    height: 100%;
                    background: url($haxagonURL) center no-repeat;
                    background-size: 140px 140px;
                    transform: translate3d(0, 0, 0);
                    transition: 0.2s;
                    .info-container {
                        display: flex;
                        flex-direction: column;
                        margin: auto;
                        .dark,
                        .light {
                            font-family: 'BenchNine', sans-serif;
                            font-size: 22px;
                        }
                        .dark {
                            color: #414042;
                        }
                        .light {
                            color: #b1b3b6;
                        }
                    }
                }
                &:hover .work-info {
                    transform: rotateY(90deg);
                }
                .link {
                    position: absolute;
                    width: 100%;
                    height: 100%;
                }
            }
        }
    }
}
</style>
