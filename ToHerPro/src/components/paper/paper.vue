<template>
    <q-layout>
        <div class="layout-view">
            <section class="paper">
                <article class="head"></article>
                <p contenteditable="true" @click="clearPlaceHolder(name)">{{name}}{{name == "" ? "" : ":"}}</p>
                <article>
                    <small contenteditable="true" @input="onDivInput($event)">{{content}}</small>
                </article>
            </section>
        </div>
    </q-layout>
</template>
<script>
    export default{
        data () {
            return {
                name: "我爱的人",
                content: "你要对他/她说的话..."
            }
        },
        methods: {
            clearPlaceHolder (e) {
                if(e !== ""){
                    this.name = "";
                }
            },
            onDivInput: function(e) {
                this.myHtmlCode = e.target.innerHTML;
                console.log('Text: %o', this.myHtmlCode );
            },
        }
    }
</script>
<style scoped>
.layout-view { 
	background: -webkit-linear-gradient(top, rgb(136,199,201) 58%, rgb(202,232,235) 100%);
	background: -moz-linear-gradient(top, rgb(136,199,201) 58%, rgb(202,232,235) 100%);
	background: -ms-linear-gradient(top, rgb(136,199,201) 58%, rgb(202,232,235) 100%);
	background: -o-linear-gradient(top, rgb(136,199,201) 58%, rgb(202,232,235) 100%);
	background: linear-gradient(top, rgb(136,199,201) 58%, rgb(202,232,235) 100%);
}

.paper {
    width: 50%;
    margin: 0 auto;
    padding: 6px 5px 4px 42px;
    position: relative;
    color: #444;
    line-height: 20px;
    background: #fff;
    background: -webkit-gradient(linear, 0 0, 0 100%, from(#d9eaf3), color-stop(4%, #fff)) 0 4px;
    background: -webkit-linear-gradient(top, #d9eaf3 0%, #fff 8%) 0 4px;
    background: linear-gradient(top, #d9eaf3 0%, #fff 8%) 0 4px;
    -ms-background-size: 100% 20px;
    background-size: 100% 20px;
    box-shadow: 0 1px 2px rgba(0,0,0,0.07);
    width: 100%;
    height: 100%;
}
 
.paper::before {
        content: '';
        position: absolute;
        width: 4px;
        top: 0;
        left: 30px;
        bottom: 0;
        border: 1px solid;
        border-color: transparent #efe4e4;
}

textarea {
        display: block;
        width: 94%;
        margin: 0 auto;
        padding: 3.8% 3%;
        border: none;
        outline: none;
        height: 94%;
        background: transparent;
        line-height: 20px;
}

.head {
    background-color: #FFF;
    min-height: 124px;
    margin-left: -42px;
    margin-top: -4px;
    margin-right: -4px;
}
</style>