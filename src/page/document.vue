<template>
    <div class="fillcontain">
        <head-top></head-top>
        <div class="contentBox">
            <el-row gutter="5">
                <el-col span="3" class="marginRight_-10px">
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
                <el-col span="4" offset="10" class="flex">
                    <div class="flexGrow"></div>
                    <el-button class="is-plain padding_5px ">
                        <div class="flex flexVerticalCenter"><img class="icon" src="../image/upload.png">&nbsp;上传文件
                        </div>
                    </el-button>
                    <el-button class="is-plain padding_5px">
                        <div class="flex flexVerticalCenter"><img class="icon" src="../image/template.png"> &nbsp;我的模板库
                        </div>
                    </el-button>
                </el-col>

            </el-row>
            <el-row class="upperNav">
                <div class="flexGrow"></div>
                <el-radio-group v-model="tabPosition" style="margin-bottom: 30px;">
                    <el-radio-button label="top">模板名称</el-radio-button>
                    <el-radio-button label="right">合同类型</el-radio-button>
                    <el-radio-button label="bottom">行业分类</el-radio-button>
                    <el-radio-button label="left">使用次数</el-radio-button>
                </el-radio-group>
            </el-row>
            <el-row class="contractContent">
                <el-row gutter="20">
                    <el-col span="6">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract.jpg" @click="dialogVisible=true" class="image">

                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex flexVerticalCenter">
                                    <div class="fontSmall">合同类型：</div>
                                    <div class="colorGrey fontSmall">买卖合同</div>
                                    <div class="flexGrow"></div>
                                    <div class="fontSmall">使用次数:</div>
                                    <div class="colorGrey fontSmall">&nbsp;12次</div>
                                </div>
                                <div class="flex marginTop_10px fontSmall">
                                    合同介绍：
                                    <div class="colorGrey">XXXXXXX</div>
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a @click="edit"><img src="../image/edit.png" class="icon"/></a>

                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">行业分类: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                    <el-col span="6">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract1.jpg" @click="dialogVisible=true" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex flexVerticalCenter">
                                    <div class="fontSmall">合同类型：</div>
                                    <div class="colorGrey fontSmall">租赁合同</div>
                                    <div class="flexGrow"></div>
                                    <div class="fontSmall">使用次数:</div>
                                    <div class="colorGrey fontSmall">&nbsp;12次</div>
                                </div>
                                <div class="flex marginTop_10px fontSmall">
                                    合同介绍：
                                    <div class="colorGrey">XXXXXXX</div>
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a @click="edit"><img src="../image/edit.png" class="icon"/></a>

                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">行业分类: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                    <el-col span="6">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract2.jpg" @click="dialogVisible=true" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex flexVerticalCenter">
                                    <div class="fontSmall">合同类型：</div>
                                    <div class="colorGrey fontSmall">租赁合同</div>
                                    <div class="flexGrow"></div>
                                    <div class="fontSmall">使用次数:</div>
                                    <div class="colorGrey fontSmall">&nbsp;12次</div>
                                </div>
                                <div class="flex marginTop_10px fontSmall">
                                    合同介绍：
                                    <div class="colorGrey">XXXXXXX</div>
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a @click="edit"><img src="../image/edit.png" class="icon"/></a>

                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">行业分类: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                    <el-col span="6">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract3.jpg" @click="dialogVisible=true" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex flexVerticalCenter">
                                    <div class="fontSmall">合同类型：</div>
                                    <div class="colorGrey fontSmall">租赁合同</div>
                                    <div class="flexGrow"></div>
                                    <div class="fontSmall">使用次数:</div>
                                    <div class="colorGrey fontSmall">&nbsp;12次</div>
                                </div>
                                <div class="flex marginTop_10px fontSmall">
                                    合同介绍：
                                    <div class="colorGrey">XXXXXXX</div>
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a @click="edit"><img src="../image/edit.png" class="icon"/></a>

                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">行业分类: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                </el-row>
                <el-row gutter="20" class="marginTop_15px">
                    <el-col span="6">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract4.jpg" @click="dialogVisible=true" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex flexVerticalCenter">
                                    <div class="fontSmall">合同类型：</div>
                                    <div class="colorGrey fontSmall">租赁合同</div>
                                    <div class="flexGrow"></div>
                                    <div class="fontSmall">使用次数:</div>
                                    <div class="colorGrey fontSmall">&nbsp;12次</div>
                                </div>
                                <div class="flex marginTop_10px fontSmall">
                                    合同介绍：
                                    <div class="colorGrey">XXXXXXX</div>
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a @click="edit"><img src="../image/edit.png" class="icon"/></a>

                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">行业分类: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                    <el-col span="6">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract5.jpg" @click="dialogVisible=true" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex flexVerticalCenter">
                                    <div class="fontSmall">合同类型：</div>
                                    <div class="colorGrey fontSmall">买卖合同</div>
                                    <div class="flexGrow"></div>
                                    <div class="fontSmall">使用次数:</div>
                                    <div class="colorGrey fontSmall">&nbsp;12次</div>
                                </div>
                                <div class="flex marginTop_10px fontSmall">
                                    合同介绍：
                                    <div class="colorGrey">XXXXXXX</div>
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a @click="edit"><img src="../image/edit.png" class="icon"/></a>

                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">行业分类: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                    <el-col span="6">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract6.jpg" @click="dialogVisible = true" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex flexVerticalCenter">
                                    <div class="fontSmall">合同类型：</div>
                                    <div class="colorGrey fontSmall">租赁合同</div>
                                    <div class="flexGrow"></div>
                                    <div class="fontSmall">使用次数:</div>
                                    <div class="colorGrey fontSmall">&nbsp;12次</div>
                                </div>
                                <div class="flex marginTop_10px fontSmall">
                                    合同介绍：
                                    <div class="colorGrey">XXXXXXX</div>
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a @click="edit"><img src="../image/edit.png" class="icon"/></a>

                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">行业分类: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                    <el-col span="6">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract7.jpg" @click="dialogVisible=true" class="image">
                                </div>
                            </div>
                            <div class="middleBox">
                                <div class="flex flexVerticalCenter">
                                    <div class="fontSmall">合同类型：</div>
                                    <div class="colorGrey fontSmall">租赁合同</div>
                                    <div class="flexGrow"></div>
                                    <div class="fontSmall">使用次数:</div>
                                    <div class="colorGrey fontSmall">&nbsp;12次</div>
                                </div>
                                <div class="flex marginTop_10px fontSmall">
                                    合同介绍：
                                    <div class="colorGrey">XXXXXXX</div>
                                </div>
                            </div>
                            <div class="downBox flex">
                                <a @click="edit"><img src="../image/edit.png" class="icon"/></a>

                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">行业分类: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                </el-row>
            </el-row>
        </div>
        <el-row type="flex" justify="center">
            <div class="flex flexVerticalCenter fontSmall">共629条</div>
            <div class="block">
                <el-pagination
                    layout="prev, pager, next"
                    :total="100">
                </el-pagination>
            </div>
        </el-row>
        <el-dialog
            title="合同预览"
            :visible.sync="dialogVisible"
            :show-close='false'
            :fullscreen="true"
            :before-close="handleClose">
            <img src="../image/contract.jpg" alt="" style="width: 100%">
            <div class="icon-left">
                <div class="container ">
                    <img src="../image/left.png" class="icon"></img>
                </div>
            </div>
            <div class="icon-right">
                <div class="container ">
                    <img src="../image/right.png" class="icon"></img>
                </div>
            </div>
            <span slot="footer" class="dialog-footer">
                    <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
                </span>
        </el-dialog>
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
                currentDate: new Date(),
                dialogVisible: false
            };
        },
        methods: {
            edit(){
                this.$router.push({path: '/vueEdit'})
            }
        }
    }
</script>

<style lang="less">
    @import "../style/document";
</style>
