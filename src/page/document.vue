<template>
    <div class="fillcontain">
        <head-top></head-top>
        <div class="contentBox">
            <el-row gutter="5">
                <el-col span="3">
                    <el-dropdown>
                        <el-dropdown size="medium" split-button type="primary">
                            发起时间
                            <el-dropdown-menu slot="dropdown">
                                <el-dropdown-item>签署时间</el-dropdown-item>
                                <el-dropdown-item>完成时间</el-dropdown-item>
                            </el-dropdown-menu>
                        </el-dropdown>
                    </el-dropdown>
                </el-col>
                <el-col span="5">
                    <el-input placeholder="请输入内容" class="input-with-select">
                        <template slot="prepend">
                            <div class="el-icon-search"></div>
                        </template>
                    </el-input>
                </el-col>
                <el-col span="2">
                    <el-button class="searchButton">搜索</el-button>
                </el-col>
                <el-col span="2" offset="10">
                    <el-button class="is-plain">上传文件</el-button>
                </el-col>
                <el-col span="2" class="flex">
                    <div class="flexGrow"></div>
                    <el-button class="is-plain">我的模板库</el-button>
                </el-col>
            </el-row>
            <el-row class="upperNav">
                <div class="flexGrow"></div>
                <el-radio-group v-model="tabPosition" style="margin-bottom: 30px;">
                    <el-radio-button label="top">模板名称</el-radio-button>
                    <el-radio-button label="right">创建时间</el-radio-button>
                    <el-radio-button label="bottom">最后查看</el-radio-button>
                    <el-radio-button label="left">吕冬雨吃屎</el-radio-button>
                </el-radio-group>
            </el-row>
            <el-row class="contractContent">
                <el-row gutter="20">
                    <el-col span="12">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract.jpg" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex">
                                    <div class="">合同类型</div>
                                    <div class="flexGrow"></div>
                                    <div class="">使用次数:12次</div>
                                </div>
                                <div class="flex marginTop_10px">
                                    合同介绍:XXXXXXXXXXXXXXXXXXXXXX
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a href="" class="fontSmall">编辑</a>
                                <a href="" class="fontSmall marginLeft_5px">下载</a>
                                <div class="flexGrow"></div>
                                <div class="fontBig">更新时间:XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                    <el-col span="12">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract.jpg" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex">
                                    <div class="">合同类型</div>
                                    <div class="flexGrow"></div>
                                    <div class="">使用次数:12次</div>
                                </div>
                                <div class="flex marginTop_10px">
                                    合同介绍:XXXXXXXXXXXXXXXXXXXXXX
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a href="" class="fontSmall">编辑</a>
                                <a href="" class="fontSmall marginLeft_5px">下载</a>
                                <div class="flexGrow"></div>
                                <div class="fontBig">更新时间:XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                </el-row>
                <el-row gutter="20" class="marginTop_10px">
                    <el-col span="12">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract.jpg" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex">
                                    <div class="">合同类型</div>
                                    <div class="flexGrow"></div>
                                    <div class="">使用次数:12次</div>
                                </div>
                                <div class="flex marginTop_10px">
                                    合同介绍:XXXXXXXXXXXXXXXXXXXXXX
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a href="" class="fontSmall">编辑</a>
                                <a href="" class="fontSmall marginLeft_5px">下载</a>
                                <div class="flexGrow"></div>
                                <div class="fontBig">更新时间:XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                    <el-col span="12">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract.jpg" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex">
                                    <div class="">合同类型</div>
                                    <div class="flexGrow"></div>
                                    <div class="">使用次数:12次</div>
                                </div>
                                <div class="flex marginTop_10px">
                                    合同介绍:XXXXXXXXXXXXXXXXXXXXXX
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a href="" class="fontSmall">编辑</a>
                                <a href="" class="fontSmall marginLeft_5px">下载</a>
                                <div class="flexGrow"></div>
                                <div class="fontBig">更新时间:XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                </el-row>
            </el-row>
        </div>
        <el-row type="flex" justify="center">
            <div class="flex flexVerticalCenter fontSmall">共6259条</div>
            <div class="block">
                <el-pagination
                    layout="prev, pager, next"
                    :total="1000">
                </el-pagination>
            </div>
        </el-row>
    </div>
</template>

<script>
    import headTop from '../components/headTop'

    export default {
        components: {
            headTop
        },
        data() {
            return {
                tabPosition: 'top',
                currentDate: new Date()
            };
        }
    }
</script>

<style lang="less">
    @import "../style/document";
</style>
