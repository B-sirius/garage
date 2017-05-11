<template>
    <div id="app">
        <div class="container">
            <div class="sidebar"></div>
            <div class="main">
                <header class="header">
                    <div class="title-container">
                        
                    </div>
                </header>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'app'
}
</script>
<style lang="scss">
#app {
    font-family: "Microsoft Yahei", "Helvetica Neue", "Helvetica", "Arial", sans-serif;
    .container {
        display: flex;
        height: 100vh;
        .sidebar {
            width: 60px;
            background: linear-gradient(180deg, #7CCFDF, #80E3CE);
        }
        .main {
            flex-grow: 1;
            overflow: auto;
            box-shadow: 0 0 10px #616161;
            background: #F8F9FB;
            padding: 20px 40px;
            .header {
                height: 120px;
                border-bottom: 1px solid #ddd;
                .title-container {
                    display: flex;
                    flex-direction: column;
                }
                .title {
                    
                }
            }
        }
    }
}
</style>
