<template>
  <div>
    <div class="block" v-for="(firstNum,id) in 9" :key="id">
			<div class='title' v-if="firstNum == 1">
				<div class="line"></div>
				<div class='center'>
					<h1 class="title-name">九九乘法表</h1>
					<h2>MULTIPLICATION CHART</h2>
				</div>
				<div class="line"></div>				
			</div>
      <div class='numGroup ' v-if="firstNum !== 1">				
				<div >
					<h1 class='firstNum'>{{firstNum}}</h1>
					<div class='col' v-for="(secondNum,id) in 3" :key="id">
						<span>{{firstNum}}</span><span>x</span><span>{{secondNum}}</span><span></span>=<span>{{firstNum*secondNum}}</span>
					</div>
				</div>
				<div>
					<div class='col right' v-for="(secondNum,id) in [4,5,6,7,8,9]" :key="id">
						<span>{{firstNum}}</span><span>x</span><span>{{secondNum}}</span><span></span>=<span>{{firstNum*secondNum}}</span> 
					</div>
				</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.block {
  width: 350px;
  height: 366px;
  display: inline-block;
  font-family:Arial, Helvetica, sans-serif,微軟正黑體;
	/* "Gill Sans",, "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif; */
	vertical-align: top;
	margin: 20px 15px
}
.center{
	padding:105px 0;
	text-align: center;
}
.line{
	width: 280px;
	height: 1px;
	background: #2EB738;
	position: relative;
	left: 36px;
	font-size: 20px;
	margin-top: 14px;
}
.line::before, .line::after{
	content: 'x';
	position: absolute;
	top: -16px;
}
.line::before{
	left: -30px;
}
.line::after{
	right: -30px;
}
.title-name{
	font-size: 56px;
	margin: 0
}
h2{
	margin: 0;
	font-size: 24px;
	font-weight: 500;
}
.col{
	display: flex;
	width: 118px;
	justify-content:space-between;
	font-size: 24px;
	line-height: 33px;
	margin: 4px 0
}
.firstNum{
	font-size: 128px;
	margin: 0;
	text-align: center;
	line-height: 111px;
	font-weight: 550;
}
.numGroup{
	display: flex;
	justify-content: space-between;
	padding: 64px 40px;
	background: #fff;
	border-radius: 100px 0px 30px 0px;
	box-shadow: 0px 3px 10px #D8D8D8;
}
</style>
