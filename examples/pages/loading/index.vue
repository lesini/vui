<style scoped>
    .example{
        display: flex;
        height: 100%;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    button{
        width: 688px;
        height: 86px;
        color: #fff;
        font-size: 36px;
        line-height: 80px;
        text-align: center;
        margin-bottom: 20px;
        outline: 0 none;
        border-radius: 5px;
        background-color: #09bb07;
        border: 1px solid #029400; /*no*/
    }
    button:last-child{
        margin-bottom: 0;
    }
</style>
<template src="./template.html"></template>

<script>
    import Loading from 'components/loading'

    export default {
        data() {
            return {
                visibleLoading: false
            }
        },
        watch: {
            visibleLoading(val) {
                if(val) {
                    setTimeout(() => {this.visibleLoading = false}, 2000)
                }
            }
        },
        components: {
            Loading
        }
    }
</script>
