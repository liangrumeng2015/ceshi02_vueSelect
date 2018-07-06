<template>
    <div id='start'>
        <div class="con">
			<div class="box">
				<input type="text" value=''>
                <span @click='addFnToggle()'>
                    <img src="../assets/img/add.png">
                </span>
			</div>
			<div class="bottom_box" v-if="isShow">
				<div class="search_box">
					<span><img src='../assets/img/icon_search.png'></span>
					<input type="text" placeholder="搜索" />
				</div>
				<div class="box_check" id='box_check'>
					<input type="checkbox" @click='abc()' value='变更中'  v-model='inputdata'/>变更中<br>
					<input type="checkbox" @click='abc()' value='未生效' v-model='inputdata' />未生效<br>
					<input type="checkbox" @click='abc()' value='作废' v-model='inputdata' />作废<br>
					<input type="checkbox" @click='abc()' value='正常' v-model='inputdata' />正常<br>
					<input type="checkbox" @click='abc()' value='审核中' v-model='inputdata' />审核中<br>
				</div>
                <ul class="checked_val" id='checked_val' >
					<li v-for='(item,key) in inputdata'>{{inputdata[key]}}
                    <span></span></li>
				</ul>
			</div>
		</div>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                isShow:false,
                inputdata:[]
            }
        },
        methods:{
            addFnToggle:function(){
                this.isShow = !this.isShow;
            },
            abc(){
            
            }
        }
    }
</script>

<style lang="scss">
@charset 'utf-8';
*{
    margin:0;
    padding:0;
    border:none;   
}
.con{
    margin:100px;
    .box{
        width: 306px;
        height: 32px;
        position: relative;
        input{
            width:304px;
            height: 30px;
            border:1px solid #d5d5d5;
            border-radius: 5px;
        }
        span{
            width: 18px;
            height: 18px;
            display: block;
            position: absolute;
            right: 6px;
            top: 8px;
        }
    }
    .bottom_box{
        width:304px ;
        height: 240px;
        position: relative;
        top:5px;
        box-shadow: 2px 2px 15px #cfcfcf;
        .search_box{
            width:304px;
            height: 44px;
            background: #f5f5f5;
            display: flex;
            align-items: center;
            justify-content: center;
            input{
                width:258px;
                height:30px;
                border:1px solid #d5d5d5;
                border-radius: 25px;
                outline: none;
                text-indent: 2rem;
            }
            span{
                width: 16px;
                height: 16px;
                display: block;
                position: absolute;
                left:35px;
                top:13px;
            }
        }
        .box_check{
            line-height: 36px;
            padding-top:10px;
            input{
                margin: 0 10px 0 30px;
                
            }   
        }
        .checked_val{
            
            width:304px;
            height: 30px;
            list-style: none;
            position: absolute;
            left:0;
            top:-37px;
            display: flex;
            align-items: center;
            li{
                padding:0 25px 0 10px;
                float:left;
                margin-right: 5px;
                color:#fff;
                text-align: center;
                height: 22px;
                line-height: 22px;
                font-size: 12px;
                border-radius: 20px;
                background:blue;
                position: relative;
                span{
                    width: 16px;
                    height: 16px;
                    display: block;
                    background: url('../assets/img/icon_close.png') no-repeat;
                    position: absolute;
                    right:6px;
                    top:50%;
                    margin-top: -8px;
                }
            }
        }
    }
}


</style>