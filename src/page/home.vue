<template>
    <div>
        <head-top></head-top>
        <div class="actionBox">
            <el-row :gutter="20">
                <el-col :span="6">
                    <el-row>
                        <el-icon class="el-icon-edit colorRed"></el-icon>
                    </el-row>
                    <el-row class="number">7</el-row>
                    <el-row class="properFont colorGrey">待我签</el-row>
                </el-col>
                <el-col :span="6">
                    <el-row>
                        <el-icon class="el-icon-time colorYellow"></el-icon>
                    </el-row>
                    <el-row class="number">7</el-row>

                    <el-row class="properFont colorGrey">待他人签</el-row>
                </el-col>
                <el-col :span="6">
                    <el-row>
                        <el-icon class="el-icon-document colorBlue"></el-icon>
                    </el-row>
                    <el-row class="number">2</el-row>

                    <el-row class="properFont colorGrey">草稿箱</el-row>
                </el-col>
                <el-col :span="6">
                    <el-row>
                        <el-icon class="el-icon-check colorGrey"></el-icon>
                    </el-row>
                    <el-row class="number">135</el-row>
                    <el-row class="properFont colorGrey">已完成</el-row>
                </el-col>
            </el-row>
        </div>
        <el-row :gutter="60" class="padding-100px messageBox">
            <el-col span="12">
                <el-card class="box-card">
                    <div slot="header" class="clearfix cardHeader">
                        <div class="small-icon colorTheme"></div>
                        <span>紧急风险</span>
                        <div class="flexGrow"></div>
                        <el-button type="text">查看全部风险></el-button>
                    </div>
                    <div class="messageBox-content">
                        <el-row class="">
                            <el-col span="12">
                                <el-row class="colorGrey">逾期合同(份)</el-row>
                                <el-row class=" colorYellowDarken">0</el-row>

                            </el-col>
                            <el-col span="12">
                                <el-row class="colorGrey">中断合同(份)</el-row>
                                <el-row class=" colorYellowDarken">0</el-row>
                            </el-col>
                        </el-row>
                        <el-row class="">
                            <el-col span="12">
                                <el-row class="colorGrey">逾期待收(元)</el-row>
                                <el-row class=" colorYellowDarken">0.00</el-row>

                            </el-col>
                            <el-col span="12">
                                <el-row class="colorGrey">逾期待付(元)</el-row>
                                <el-row class=" colorYellowDarken">0.00</el-row>
                            </el-col>
                        </el-row>
                    </div>
                </el-card>
                <div class="QRBox flex">
                    <img src="../image/FisrtQRcode.png" class="QRcode " alt="">
                    <div class="describe">
                        <div class="up colorGrey flex flexVerticalCenter">
                            <img src="../image/phone.png" class="icon" alt="">下载App
                        </div>
                        <div class="flexGrow"></div>
                        <div class="down">APP可以快捷认证，随时随地签署文件，更快捷，更安全</div>
                    </div>
                </div>
            </el-col>
            <el-col span="12">
                <el-card class="box-card">
                    <div slot="header" class="clearfix cardHeader">
                        <div class="small-icon colorTheme"></div>
                        <span>合同状况</span>
                        <div class="flexGrow"></div>
                        <el-button type="text">查看全部合同></el-button>
                    </div>
                    <div class="messageBox-content">

                        <el-row type="flex">
                            <div class="colorGrey">履约中合同总数</div>
                            <div class="flexGrow"></div>
                            <div class=" colorYellowDarken">23份</div>
                        </el-row>
                        <el-row type="flex">
                            <div class="colorGrey">本月新增合同数</div>
                            <div class="flexGrow"></div>
                            <div class=" colorYellowDarken">4份</div>
                        </el-row>
                        <el-row type="flex">
                            <div class="colorGrey">本月到期合同数</div>
                            <div class="flexGrow"></div>
                            <div class="colorYellowDarken">6份</div>
                        </el-row>
                        <el-row type="flex">
                            <div class="colorGrey">履约中断合同数</div>
                            <div class="flexGrow"></div>
                            <div class=" colorYellowDarken">1份</div>
                        </el-row>


                    </div>
                </el-card>
                <div class="QRBox flex marginTop_28px marginRight_10px">
                    <img src="../image/SecondQRcode.png" class="QRcode " alt="">
                    <div class="describe">
                        <div class="up colorGrey flex flexVerticalCenter">
                            <img src="../image/wechat.png" class="icon" alt="">关注微信公众号
                        </div>
                        <div class="flexGrow"></div>
                        <div class="down">随时了解律兜咨询，还可以在线签署文件哦</div>
                    </div>
                </div>
            </el-col>
            <el-col span="12" class="marginRight_-1px">

            </el-col>

        </el-row>


    </div>
</template>

<script>
    import headTop from '../components/headTop'

    export default {
        components: {
            headTop
        }
    }
</script>

<style lang="less">
    @import '../style/homePage';
</style>
