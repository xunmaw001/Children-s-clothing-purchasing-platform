<template>
<view class="content">
	<view class="box" :style='{"padding":"0 40rpx 100rpx","boxShadow":"0px 6rpx 12rpx rgba(0, 0, 0, 0.16)","margin":"0 5%","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 1)","borderRadius":"0 0 1800rpx 1800rpx","borderWidth":"0","width":"90%","borderStyle":"solid","height":"auto"}'>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='yonghu'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>账号</view>
			<input disabled="true"  style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.zhanghao" placeholder="账号"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='yonghu'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>密码</view>
			<input  type="password" style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.mima" placeholder="密码"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='yonghu'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>姓名</view>
			<input   style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.xingming" placeholder="姓名"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='yonghu'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>年龄</view>
			<input   style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.nianling" placeholder="年龄"></input>
		</view>
			<view v-if="tableName=='yonghu'" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' class="cu-form-group select">
                                <view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' class="title">性别</view>
                                <picker  @change="yonghuxingbieChange" :value="yonghuxingbieIndex" :range="yonghuxingbieOptions">
                                        <view style="padding: 0 30upx" :style='{"padding":"0 20rpx","boxShadow":"0 0 0px rgba(0,0,0,.6) inset","margin":"0","borderColor":"rgba(79, 74, 78, 1)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(0, 0, 0, 1)","textAlign":"left","borderRadius":"16rpx","borderWidth":"2rpx","width":"calc(100% - 160rpx)","fontSize":"28rpx","borderStyle":"dashed ","height":"70rpx"}' class="uni-input picker-select-input">{{ruleForm.xingbie?ruleForm.xingbie:"请选择性别"}}</view>
                                </picker>
                        </view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='yonghu'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>手机</view>
			<input   style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.shouji" placeholder="手机"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='yonghu'" @tap="yonghuzhaopianTap" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>照片</view>
			<view style="flex: 1;">
				<image :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(255, 255, 255, 0)","borderRadius":"100%","borderWidth":"2rpx","width":"88rpx","borderStyle":"solid","height":"88rpx"}' v-if="ruleForm.zhaopian" style="margin: 0;" class="avator" :src="baseUrl+ruleForm.zhaopian" mode=""></image>
				<image :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(255, 255, 255, 0)","borderRadius":"100%","borderWidth":"2rpx","width":"88rpx","borderStyle":"solid","height":"88rpx"}' v-else class="avator" style="margin: 0;" src="../../static/center/face.jpeg" mode=""></image>
			</view>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='shangjia'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>商家账号</view>
			<input disabled="true"  style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.shangjiazhanghao" placeholder="商家账号"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='shangjia'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>密码</view>
			<input  type="password" style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.mima" placeholder="密码"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='shangjia'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>店铺名</view>
			<input   style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.dianpuming" placeholder="店铺名"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='shangjia'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>负责人</view>
			<input   style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.fuzeren" placeholder="负责人"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='shangjia'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>联系电话</view>
			<input   style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.lianxidianhua" placeholder="联系电话"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='shangjia'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>建筑面积</view>
			<input   style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.jianzhumianji" placeholder="建筑面积"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='shangjia'" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>店铺地址</view>
			<input   style="padding: 0 30upx" :style='{"padding":"0","boxShadow":"0 0 12rpx rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(0,0,0,0)","color":"rgba(0, 0, 0, 1)","borderRadius":"0","borderWidth":"0 0 2rpx","width":"100%","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}' v-model="ruleForm.dianpudizhi" placeholder="店铺地址"></input>
		</view>
		<view :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0 0 20rpx 0","borderColor":"#ccc","backgroundColor":"rgba(255, 255, 255, 0.25)","borderRadius":"0","borderWidth":"0","width":"100%","borderStyle":"solid","height":"100rpx"}' v-if="tableName=='shangjia'" @tap="shangjiafengmianTap" class="cu-form-group">
			<view class="title" :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,0)","margin":"0","borderColor":"rgba(0,0,0,0)","backgroundColor":"rgba(255, 255, 255, 0)","color":"rgba(79, 74, 78, 1)","textAlign":"left","borderRadius":"0","borderWidth":"0","width":"160rpx","lineHeight":"88rpx","fontSize":"28rpx","borderStyle":"solid"}'>封面</view>
			<view style="flex: 1;">
				<image :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(255, 255, 255, 0)","borderRadius":"100%","borderWidth":"2rpx","width":"88rpx","borderStyle":"solid","height":"88rpx"}' v-if="ruleForm.fengmian" style="margin: 0;" class="avator" :src="baseUrl+ruleForm.fengmian" mode=""></image>
				<image :style='{"padding":"0","boxShadow":"0 0 0px rgba(0,0,0,.3)","margin":"0","borderColor":"rgba(0, 0, 0, 1)","backgroundColor":"rgba(255, 255, 255, 0)","borderRadius":"100%","borderWidth":"2rpx","width":"88rpx","borderStyle":"solid","height":"88rpx"}' v-else class="avator" style="margin: 0;" src="../../static/center/face.jpeg" mode=""></image>
			</view>
		</view>
		
		<view class="btn">
			<button @tap="update()" class="cu-btn lg" :style='{"padding":"0 30rpx","boxShadow":"0 0 16rpx rgba(0,0,0,0) inset","margin":"0 0 20rpx","backgroundColor":"rgba(209, 176, 134, 1)","borderColor":"rgba(209, 176, 134, 1)","borderRadius":"80rpx","color":"#fff","borderWidth":"1","width":"320rpx","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'>保存</button>
			<button @tap="logout()" class="cu-btn lg" :style='{"padding":"0 30rpx","boxShadow":"0 0 16rpx rgba(0,0,0,0) inset","margin":"0","backgroundColor":"rgba(213, 213, 213, 1)","borderColor":"rgba(213, 213, 213, 1)","borderRadius":"80rpx","color":"#fff","borderWidth":"2rpx","width":"320rpx","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'>退出登录</button>
		</view>
	</view>
</view>
</template>

<script>
	export default {
		data() {
			return {
				ruleForm: {
				},
				tableName:"",
				yonghuxingbieOptions: [],
				yonghuxingbieIndex: 0,
			}
		},
		computed: {
			baseUrl() {
				return this.$base.url;
			}
		},
		async onLoad() {
			let table = uni.getStorageSync("nowTable");
			let res = await this.$api.session(table);
			this.ruleForm = res.data;
			this.tableName = table;
			// 自定义下拉框值
			if(this.tableName=='yonghu'){
				this.yonghuxingbieOptions = "男,女".split(',');
				this.yonghuxingbieOptions.forEach((item, index) => {
					if(item==this.ruleForm.xingbie) {
						this.yonghuxingbieIndex = index;
					}
				});
			}
			this.styleChange()
		},
		methods: {
                        // 下拉变化
                        yonghuxingbieChange(e) {
                                this.yonghuxingbieIndex = e.target.value
                                this.ruleForm.xingbie = this.yonghuxingbieOptions[this.yonghuxingbieIndex]
                        },
			styleChange() {
				this.$nextTick(()=>{
					// document.querySelectorAll('.cu-form-group .uni-input-input').forEach(el=>{
					//   el.style.backgroundColor = this.userInfoForm.list.input.backgroundColor
					// })
				})
			},
			// 获取uuid
			getUUID () {
				return new Date().getTime();
			},
			logout() {
				uni.setStorageSync('token', '');
				this.$utils.jump('../login/login');
			},
			// 注册
			async update() {
				if((!this.ruleForm.zhanghao) && `yonghu` == this.tableName){
					this.$utils.msg(`账号不能为空`);
					return
				}
				if((!this.ruleForm.mima) && `yonghu` == this.tableName){
					this.$utils.msg(`密码不能为空`);
					return
				}
				if((!this.ruleForm.xingming) && `yonghu` == this.tableName){
					this.$utils.msg(`姓名不能为空`);
					return
				}
				if(`yonghu` == this.tableName && this.ruleForm.nianling&&(!this.$validate.isIntNumer(this.ruleForm.nianling))){
					this.$utils.msg(`年龄应输入整数`);
					return
				}
				if(`yonghu` == this.tableName && this.ruleForm.shouji&&(!this.$validate.isMobile(this.ruleForm.shouji))){
					this.$utils.msg(`手机应输入手机格式`);
					return
				}
				if(`yonghu` == this.tableName && this.ruleForm.money&&(!this.$validate.isNumber(this.ruleForm.money))){
					this.$utils.msg(`余额应输入数字`);
					return
				}
				if((!this.ruleForm.shangjiazhanghao) && `shangjia` == this.tableName){
					this.$utils.msg(`商家账号不能为空`);
					return
				}
				if((!this.ruleForm.mima) && `shangjia` == this.tableName){
					this.$utils.msg(`密码不能为空`);
					return
				}
				if((!this.ruleForm.dianpuming) && `shangjia` == this.tableName){
					this.$utils.msg(`店铺名不能为空`);
					return
				}
				if(`shangjia` == this.tableName && this.ruleForm.lianxidianhua&&(!this.$validate.isMobile(this.ruleForm.lianxidianhua))){
					this.$utils.msg(`联系电话应输入手机格式`);
					return
				}
				if(`shangjia` == this.tableName && this.ruleForm.thumbsupnum&&(!this.$validate.isIntNumer(this.ruleForm.thumbsupnum))){
					this.$utils.msg(`赞应输入整数`);
					return
				}
				if(`shangjia` == this.tableName && this.ruleForm.crazilynum&&(!this.$validate.isIntNumer(this.ruleForm.crazilynum))){
					this.$utils.msg(`踩应输入整数`);
					return
				}
				if(`shangjia` == this.tableName && this.ruleForm.clicknum&&(!this.$validate.isIntNumer(this.ruleForm.clicknum))){
					this.$utils.msg(`点击次数应输入整数`);
					return
				}
				if(`shangjia` == this.tableName && this.ruleForm.money&&(!this.$validate.isNumber(this.ruleForm.money))){
					this.$utils.msg(`余额应输入数字`);
					return
				}
				let table = uni.getStorageSync("nowTable");
				await this.$api.update(table, this.ruleForm);
				this.$utils.msgBack('修改成功');;
			}

			,yonghuzhaopianTap() {
				let _this = this;
				this.$api.upload(function(res) {
					_this.ruleForm.zhaopian = 'upload/' + res.file;
					_this.$forceUpdate();
				});
			}
			,shangjiafengmianTap() {
				let _this = this;
				this.$api.upload(function(res) {
					_this.ruleForm.fengmian = 'upload/' + res.file;
					_this.$forceUpdate();
				});
			}
		}
	}
</script>

<style lang="scss" scoped>
	page {
		background-color: #fff;
	}
	
	.content:after {
		position: fixed;
		top: 0;
		right: 0;
		left: 0;
		bottom: 0;
		content: '';
				background-attachment: fixed;
		background-size: cover;
		background-position: center;
	}

	.avator {
		width: 110upx;
		height: 110upx;
		border-radius: 50%;
		margin-left: 30upx;
	}
	
	.cu-form-group.active {
		justify-content: space-between;
	}

	.cu-btn {
		width: 100%;
	}
	.cu-form-group .title {
		height: auto;
	}

	.right-input {
		flex: 1;
		text-align: left;
		line-height: 70rpx;
	}
	.btn {
	  display: flex;
	  align-items: center;
	  justify-content: center;
	  flex-wrap: wrap;
	}
	.box {
	  width: auto;
	  padding: 0 10upx;
	  box-sizing: border-box;
	  margin-bottom: 20upx;
	}

.picker-select-input {
	line-height: 70rpx;
}
</style>
