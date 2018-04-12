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
                    <el-button class="is-plain padding_5px " >
                        <div class="flex flexVerticalCenter">  <img class="icon" src="../image/upload.png">&nbsp;上传文件</div>
                    </el-button>
                    <el-button class="is-plain padding_5px" >
                        <div class="flex flexVerticalCenter">  <img class="icon" src="../image/template.png"> &nbsp;我的模板库</div>
                    </el-button>
                </el-col>

            </el-row>
            <el-row class="upperNav">
                <div class="flexGrow"></div>
                <el-radio-group v-model="tabPosition" style="margin-bottom: 30px;">
                    <el-radio-button label="top">模板名称</el-radio-button>
                    <el-radio-button label="right">合同类型</el-radio-button>
                    <el-radio-button label="bottom">更新时间</el-radio-button>
                    <el-radio-button label="left">使用次数</el-radio-button>
                </el-radio-group>
            </el-row>
            <el-row class="contractContent">
                <el-row gutter="20">
                <el-col span="6">
                    <el-card>
                        <div class="imgContainer">
                            <div class="Container">
                                <img src="../image/contract.jpg"  @click="dialogVisible=true" class="image" >

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
                            <a href=""><img src="../image/edit.png" class="icon"/></a>
                            <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                            <div class="flexGrow"></div>
                            <div class="fontSmall">更新时间: &nbsp;</div>
                            <div class="fontSmall colorGrey">XXXX</div>

                        </div>
                    </el-card>
                </el-col>
                <el-col span="6">
                    <el-card>
                        <div class="imgContainer">
                            <div class="Container">
                                <img src="../image/contract.jpg"  @click="dialogVisible=true" class="image" >
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
                            <a href=""><img src="../image/edit.png" class="icon"/></a>
                            <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                            <div class="flexGrow"></div>
                            <div class="fontSmall">更新时间: &nbsp;</div>
                            <div class="fontSmall colorGrey">XXXX</div>

                        </div>
                    </el-card>
                </el-col>
                <el-col span="6">
                    <el-card>
                        <div class="imgContainer">
                            <div class="Container">
                                <img src="../image/contract.jpg"  @click="dialogVisible=true" class="image" >
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
                            <a href=""><img src="../image/edit.png" class="icon"/></a>
                            <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                            <div class="flexGrow"></div>
                            <div class="fontSmall">更新时间: &nbsp;</div>
                            <div class="fontSmall colorGrey">XXXX</div>

                        </div>
                    </el-card>
                </el-col>
                <el-col span="6">
                    <el-card>
                        <div class="imgContainer">
                            <div class="Container">
                                <img src="../image/contract.jpg"  @click="dialogVisible=true" class="image" >
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
                            <a href=""><img src="../image/edit.png" class="icon"/></a>
                            <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                            <div class="flexGrow"></div>
                            <div class="fontSmall">更新时间: &nbsp;</div>
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
                                    <img src="../image/contract.jpg"  @click="dialogVisible=true" class="image" >
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
                                <a href=""><img src="../image/edit.png" class="icon"/></a>
                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">更新时间: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
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
                                <a href=""><img src="../image/edit.png" class="icon"/></a>
                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">更新时间: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
                    <el-col span="6">
                        <el-card>
                            <div class="imgContainer">
                                <div class="Container">
                                    <img src="../image/contract.jpg"  @click="dialogVisible = true" class="image">
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
                                <a href=""><img src="../image/edit.png" class="icon"/></a>
                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon"/></a>
                                <div class="flexGrow"></div>
                                <div class="fontSmall">更新时间: &nbsp;</div>
                                <div class="fontSmall colorGrey">XXXX</div>

                            </div>
                        </el-card>
                    </el-col>
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
                                <a href=""><img src="../image/edit.png" class="icon"/></a>
                                <a href="" class="marginLeft_15px "><img src="../image/download.png" class="icon" /></a>
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
                    :total="100">
                </el-pagination>
            </div>
        </el-row>
        <el-dialog
            title="合同预览"
            :visible.sync="dialogVisible"
            width="50%"
            :show-close='false'
            :fullscreen="true"
            :before-close="handleClose">
            <img src="../image/contract.jpg" alt="" style="width: 100%">
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
        }
    }
</script>

<style lang="less">
    @import "../style/document";
</style>
