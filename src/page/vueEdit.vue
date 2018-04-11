<template>
    <div>
        <head-top></head-top>
        <el-row type="flex" class="buttonBox">
            <el-button type="info" plain @click="back" >返回</el-button>
            <div class="flexGrow"></div>
            <div>
                <el-popover
                    ref="popover1"
                    placement="top-start"
                    title="提示"
                    width="200"
                    trigger="hover"
                    content="您的合同将被保存至草稿箱">
                </el-popover>
                <el-popover
                    ref="popover2"
                    placement="top-start"
                    title="提示"
                    width="200"
                    trigger="hover"
                    content="可以以多种格式下载">
                </el-popover>
                <el-popover
                    ref="popover3"
                    placement="top-start"
                    title="提示"
                    width="200"
                    trigger="hover"
                    content="吕冬雨大傻逼">
                </el-popover>
                <el-button v-popover:popover1 type="primary" class="marginLeft_5px" @click="save">保存至草稿箱</el-button>
                <el-button v-popover:popover2 type="primary" class="marginLeft_5px" @click="download">下载文档</el-button>
                <el-button v-popover:popover3 type="primary" class="marginLeft_5px">发送</el-button>

            </div>
        </el-row>
        <div class="edit_container">
            <quill-editor v-model="content"
                          ref="myQuillEditor"
                          class="editer"
                          :options="editorOption"
                          @ready="onEditorReady($event)">
            </quill-editor>
        </div>
        <div class="submit_btn">
            <el-button type="primary" @click="submit">提交</el-button>
        </div>
    </div>
</template>

<script>
    import headTop from '../components/headTop'
    import {quillEditor} from 'vue-quill-editor'
    import ElButton from "../../node_modules/element-ui/packages/button/src/button";

    export default {
        data(){
            return {
                content: '<img src="../image/contract.jpg">',
                editorOption: {}
            }
        },
        components: {
            ElButton,
            headTop,
            quillEditor,
        },
        computed: {
            editor() {
                return this.$refs.myQuillEditor.quill
            }
        },
        methods: {
            onEditorReady(editor) {
                console.log('editor ready!', editor)
            },
            submit(){
                console.log(this.content);
                this.$message.success('提交成功！');
            },
            back(){
                this.$router.push({path:'/document'})
            },
            save(){
                this.$message.success('保存成功！');
            },
            download(){
                this.$message.success("开始下载");
            }
        },
        mounted() {
            console.log('this is my editor', this.editor)
            setTimeout(() => {
                this.editor.insertEmbed(10, 'image', '../image/contract.jpg');
            }, 300)
        }
    }
</script>

<style lang="less">
    @import '../style/mixin';
    @import "../style/document";
    @import "../style/vueEdit";

    .edit_container {
        padding: 40px;
        padding-top:0px ;
        margin-top: -20px;
        margin-bottom: 40px;
    }

    .editer {
        height: 350px;
    }

    .submit_btn {
        text-align: center;
    }
</style>
