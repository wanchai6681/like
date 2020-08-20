<template>
<div>
    <div>
        <button v-on:click="$like" class="button-apple " id="red">like<i class="far fa-thumbs-up"></i></button>
        <button v-on:click="$dislike" class="button-apple" id="blue">dislike<i class="far fa-thumbs-down"></i></button>
        <button v-on:click="$love"  class="button-apple" id="red">love<i class="far fa-heart"></i></button>
        <button v-on:click="counter = 0" class="button-apple" id="black">removed<i class="fas fa-history"></i></button>
        <h1>{{counter}}</h1>
    </div>
</div>
</template>

<script>
export default {
    name: 'CsButton',
    props: {
        label: String
    },
    data: function () {
        return {
            like: 0,
            love: 0,
            dislike: 0, 
            counter:0,
        };
    },
        methods:{
            $like:function(){
                this.counter +=1
                this.like +=1
              
            },
            $love:function(){
                this.counter +=5
                this.love +=1
            },
            $dislike:function(){
                this.counter -=10
                this.dislike += 1
            }
        }
}
</script>

<style>
    .button-apple{
    background-color: rgb(255, 255, 255);
    border: none;
    padding: 5px 5px 5px 5px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 8px;
    border: 0.5px solid #ebebeb;
    width : 160px;
}

.button-apple-font-dd{
    background-color: white;
    border: none;
    color: #07f607;
    padding: 5px 5px 5px 5px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 8px;
    border: 0.5px solid #ebebeb;
    width : 60px;
}



button:hover#blue {
    color: blue;
}
button:hover#red {
    color: red;
}
button:hover#black {
    color: black;
}
</style>
