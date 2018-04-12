<template>
    <div>
        <head-top></head-top>
        <el-row type="flex" class="buttonBox">
            <el-button type="info" plain @click="back">返回</el-button>
            <div class="flexGrow"></div>
            <div>
                <el-popover
                    ref="popover1"
                    placement="top-start"
                    title="提示"
                    width="200"
                    trigger="hover"
                    content="在一定土地所有制关系下作为财产的土地。">
                </el-popover>
                <el-popover
                    ref="popover2"
                    placement="top-start"
                    title="提示"
                    width="200"
                    trigger="hover"
                    content="房地产权利人通过买卖、赠与或者其他合法方式将其房地产转移给他人的行为。">
                </el-popover>

                <el-button  type="primary" class="marginLeft_5px" @click="save">保存至草稿箱</el-button>
                <el-button type="primary" class="marginLeft_5px" @click="download">下载文档</el-button>
                <el-button type="primary" class="marginLeft_5px">发送</el-button>

            </div>
        </el-row>
        <div class="edit_container">
            <quill-editor v-model="content"
                          ref="myQuillEditor"
                          class="editer"
                          :options="editorOption"
                          @ready="onEditorReady($event)">
            </quill-editor>
            <div class="fakeBoard ql-editor">
                <h1 class="ql-align-center"><span class="ql-size-large">房产</span><strong
                    class="ql-size-large">买卖合同</strong></h1>
                <p class="ql-align-center"><br></p>
                <p><span class="ql-size-large">卖方：________________________&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;身份证号： ________________________</span>
                </p>
                <p><span class="ql-size-large">联系电话：________________________&nbsp;通讯地址：________________________</span>
                </p>
                <p><span class="ql-size-large">买方：________________________&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;身份证号：________________________</span>
                </p>
                <p><span class="ql-size-large">联系电话：________________________ 通讯地址：________________________</span></p>
                <p><span class="ql-size-large">根据《中华人民共和国合同法》、《中华人民共和国城市</span><a v-popover:popover1 target="_blank"
                                                                                  style="color: rgb(45, 100, 181);"
                                                                                  class="ql-size-large">房地产</a><span
                    class="ql-size-large">管理法》及有关法律、法规的规定，买卖双方在平等、自愿、公平、协商一致的基础上就本合同所涉</span><a
                   v-popover:popover2 target="_blank" style="color: rgb(45, 100, 181);"
                    class="ql-size-large">房地产转让</a><span class="ql-size-large">事宜，达成如下协议：</span></p>
                <p><strong class="ql-size-large">第一条 【转让标的】</strong></p>
                <p><span class="ql-size-large">卖方所转让房</span><a href="http://www.fang.com/juhe/31154/" target="_blank"
                                                               style="color: rgb(45, 100, 181);" class="ql-size-large">地产</a><span
                    class="ql-size-large">（下称该房产）坐落于：_______________________________________________。</span></p>
                <p><span class="ql-size-large">土地使用权证号：_______________，房产权证号：_______________ ，登记建筑面积为：________ 平方米。套内建筑面积为：________平方米。</span>
                </p>
                <p><span class="ql-size-large">该房地产土地使用权年限自______年______月______日至______年______月______日止。</span></p>
                <p><span class="ql-size-large">该房地产约定交付的附属设施设备、装饰装修、相关物品等在签订本协议前，已经双方现场确认，均无异议。</span></p>
                <p><strong class="ql-size-large">第二条 【房地产产权现状】</strong></p>
                <p><span class="ql-size-large">该房地产没有设定抵押也未被查封，卖方对该房地产享有完全的处分权。</span></p>
                <p><strong class="ql-size-large">第三条 【房地产租约现状】</strong></p>
                <p><span class="ql-size-large">该房地产所附租约现状为第______项：</span></p>
                <p><span class="ql-size-large">1、该房地产没有租约；</span></p>
                <p><span class="ql-size-large">2、该房地产之上存有租约，卖方须于本合同签订时将承租人放弃优先购买权的书面文件及租赁合同交予买方。</span></p>
                <p><strong class="ql-size-large">第四条 【附着于该房地产之上的户口】</strong></p>
                <p><span class="ql-size-large">如该房地产所附着有卖方户口，基于保证买方办理房产过户登记后，应享有完全的处分权，卖方保证于收到房地产转让总价款之日起_____日内迁出，逾期则以该房地产转让总价款为基数按日万分之______向买方支付</span><a
                    href="http://www.fang.com/juhe/32722/" target="_blank" style="color: rgb(45, 100, 181);"
                    class="ql-size-large">违约金</a><span class="ql-size-large">。</span></p>
                <p><strong class="ql-size-large">第五条 【转让价款】</strong></p>
                <p><span class="ql-size-large">该房地产转让总价款为人民币：____________（小写：______元）。</span></p>
                <p><strong class="ql-size-large">第七条 【税费承担】</strong></p>
                <p><span class="ql-size-large">双方约定，由买方承担办理相关过户手续双方按规定应缴纳的一切可能产生的税、费。</span></p>
                <p><span
                    class="ql-size-large">买方不按约定缴纳相关税费，导致交易不能继续进行的，买方不得因此解除合同，本合同应继续履行，但违约方应承担违约责任，赔偿给守约方造成的损失。</span>
                </p>
                <p><strong class="ql-size-large">第八条 【付款方式】</strong></p>
                <p><span class="ql-size-large">买方于______年______月______ 日前一次性付清全部房款。</span></p>
                <p><strong class="ql-size-large">第九条 【买方逾期付款的违约责任】</strong></p>
                <p><span class="ql-size-large">买方逾期付款的，卖方有权要求买方要求买方以未付款项为基数，按日万分之______支付违约金，合同继续履行。</span></p>
                <p><strong class="ql-size-large">第十条 【房地产交付】</strong></p>
                <p><span class="ql-size-large">卖方应当于______年______月______日将该房地产交付买方，并履行下列手续：</span></p>
                <p><span class="ql-size-large">1、买卖双方共同对该房地产及附属设施设备、装饰装修、相关物品等事项进行验收，记录水、电、气表的读数，并办理交接手续；</span></p>
                <p><span class="ql-size-large">2、交付该房地产钥匙；</span></p>
                <p><span class="ql-size-large">3、______________________________</span></p>
                <p><strong class="ql-size-large">第十一条 【延迟交房的违约责任】</strong></p>
                <p><span class="ql-size-large">除本合同另有约定外，卖方未按合同约定的期限将该房地产交付买方，自约定的交付期限届满次日起至实际交付日止，卖方以该房地产转让总价款为基数按日万分之______向买方支付违约金，合同继续履行。</span>
                </p>
                <p><strong class="ql-size-large">第十二条 【附随债务的处理】</strong></p>
                <p><span class="ql-size-large">卖方在交付该房地产时，应将附随的水费、电费、煤气费、电话费、有线电视费、物业管理服务费、垃圾清运费等费用结清，单据交买方确认，否则买方有权从交房保证金中抵扣上述欠费。</span>
                </p>
                <p><strong class="ql-size-large">第十三条 【产权转移登记】</strong></p>
                <p><span class="ql-size-large">买卖双方须在签订本合同______日内，共同向房地产权登记机关申请办理转移登记手续，卖方应按照机关的登记手续要求积极协助。</span></p>
                <p><span class="ql-size-large">在收文回执载明的回复日期届满之日起______日内，买方须按本约定办理交纳税费的手续。</span></p>
                <p><strong class="ql-size-large">第十四条 【其他违约责任】</strong></p>
                <p><span class="ql-size-large">任何一方不履行本合同约定义务，致合同目的不能实现，守约方有权选择定金罚则或要求对方支付该房地产总价款百分之______的违约金。</span>
                </p>
                <p><strong class="ql-size-large">第十五条 【不可抗力】</strong></p>
                <p><span class="ql-size-large">因不可抗力不能履行本合同的，根据不可抗力的影响，部分或者全部免除责任，但法律另有规定的除外。因不可抗力不能按照约定履行合同的一方当事人应当及时告知另一方当事人，并自不可抗力结束之日起______日内向另一方提供证明。</span>
                </p>
                <p><strong class="ql-size-large">第十六条 【本合同与其他文件的冲突解决】</strong></p>
                <p><span class="ql-size-large">买卖双方在本合同签订之前的承诺及协议，如有与本合同不相符的，以本合同为准。</span></p>
                <p><strong class="ql-size-large">第十七条 【合同附件】</strong></p>
                <p><span class="ql-size-large">本合同共有附件______份。合同附件为本合同组成部分，具有同等法律效力。</span></p>
                <p><strong class="ql-size-large">第十八条 【法律适用与纠纷解决】</strong></p>
                <p><span class="ql-size-large">因本合同发生纠纷，由买卖双方协商解决。协商不成时，依据中华人民共和国法律，采取下列第______种方式解决：</span></p>
                <p><span class="ql-size-large">1、向______仲裁委员会申请仲裁；</span></p>
                <p><span class="ql-size-large">2、向房产所在地人民法院起诉。</span></p>
                <p><strong class="ql-size-large">第十九条 【合同数量及持有】</strong></p>
                <p><span class="ql-size-large">本合同一式 4 份，卖方 1 份，买方 1 份，其他交有关部门，均具同等法律效力。</span></p>
                <p><strong class="ql-size-large">第二十条 【合同生效】</strong></p>
                <p><span class="ql-size-large">本合同自买卖双方签署后立即生效。</span></p>
                <p><span class="ql-size-large">卖方（签字）：____________&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;买方（签字）： ____________</span>
                </p>
                <p><span class="ql-size-large">______年______ 月______ 日&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;______年______ 月______ 日</span>
                </p>

            </div>

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
                editorOption: {},
                content: '<h1 class="ql-align-center"><span class="ql-size-large">房产</span><strong class="ql-size-large">买卖合同</strong></h1><p class="ql-align-center"><br></p><p><span class="ql-size-large">卖方：________________________&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;身份证号： ________________________</span></p><p><span class="ql-size-large">联系电话：________________________&nbsp;通讯地址：________________________</span></p><p><span class="ql-size-large">买方：________________________&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;身份证号：________________________</span></p><p><span class="ql-size-large">联系电话：________________________ 通讯地址：________________________</span></p><p><span class="ql-size-large">根据《中华人民共和国合同法》、《中华人民共和国城市</span><a v-popover:popover1 target="_blank" style="color: rgb(45, 100, 181);" class="ql-size-large">房地产</a><span class="ql-size-large">管理法》及有关法律、法规的规定，买卖双方在平等、自愿、公平、协商一致的基础上就本合同所涉</span><a href="http://www.fang.com/juhe/31355/" target="_blank" style="color: rgb(45, 100, 181);" class="ql-size-large">房地产转让</a><span class="ql-size-large">事宜，达成如下协议：</span></p><p><strong class="ql-size-large">第一条 【转让标的】</strong></p><p><span class="ql-size-large">卖方所转让房</span><a href="http://www.fang.com/juhe/31154/" target="_blank" style="color: rgb(45, 100, 181);" class="ql-size-large">地产</a><span class="ql-size-large">（下称该房产）坐落于：_______________________________________________。</span></p><p><span class="ql-size-large">土地使用权证号：_______________，房产权证号：_______________ ，登记建筑面积为：________ 平方米。套内建筑面积为：________平方米。</span></p><p><span class="ql-size-large">该房地产土地使用权年限自______年______月______日至______年______月______日止。</span></p><p><span class="ql-size-large">该房地产约定交付的附属设施设备、装饰装修、相关物品等在签订本协议前，已经双方现场确认，均无异议。</span></p><p><strong class="ql-size-large">第二条 【房地产产权现状】</strong></p><p><span class="ql-size-large">该房地产没有设定抵押也未被查封，卖方对该房地产享有完全的处分权。</span></p><p><strong class="ql-size-large">第三条 【房地产租约现状】</strong></p><p><span class="ql-size-large">该房地产所附租约现状为第______项：</span></p><p><span class="ql-size-large">1、该房地产没有租约；</span></p><p><span class="ql-size-large">2、该房地产之上存有租约，卖方须于本合同签订时将承租人放弃优先购买权的书面文件及租赁合同交予买方。</span></p><p><strong class="ql-size-large">第四条 【附着于该房地产之上的户口】</strong></p><p><span class="ql-size-large">如该房地产所附着有卖方户口，基于保证买方办理房产过户登记后，应享有完全的处分权，卖方保证于收到房地产转让总价款之日起_____日内迁出，逾期则以该房地产转让总价款为基数按日万分之______向买方支付</span><a href="http://www.fang.com/juhe/32722/" target="_blank" style="color: rgb(45, 100, 181);" class="ql-size-large">违约金</a><span class="ql-size-large">。</span></p><p><strong class="ql-size-large">第五条 【转让价款】</strong></p><p><span class="ql-size-large">该房地产转让总价款为人民币：____________（小写：______元）。</span></p><p><strong class="ql-size-large">第七条 【税费承担】</strong></p><p><span class="ql-size-large">双方约定，由买方承担办理相关过户手续双方按规定应缴纳的一切可能产生的税、费。</span></p><p><span class="ql-size-large">买方不按约定缴纳相关税费，导致交易不能继续进行的，买方不得因此解除合同，本合同应继续履行，但违约方应承担违约责任，赔偿给守约方造成的损失。</span></p><p><strong class="ql-size-large">第八条 【付款方式】</strong></p><p><span class="ql-size-large">买方于______年______月______ 日前一次性付清全部房款。</span></p><p><strong class="ql-size-large">第九条 【买方逾期付款的违约责任】</strong></p><p><span class="ql-size-large">买方逾期付款的，卖方有权要求买方要求买方以未付款项为基数，按日万分之______支付违约金，合同继续履行。</span></p><p><strong class="ql-size-large">第十条 【房地产交付】</strong></p><p><span class="ql-size-large">卖方应当于______年______月______日将该房地产交付买方，并履行下列手续：</span></p><p><span class="ql-size-large">1、买卖双方共同对该房地产及附属设施设备、装饰装修、相关物品等事项进行验收，记录水、电、气表的读数，并办理交接手续；</span></p><p><span class="ql-size-large">2、交付该房地产钥匙；</span></p><p><span class="ql-size-large">3、______________________________</span></p><p><strong class="ql-size-large">第十一条 【延迟交房的违约责任】</strong></p><p><span class="ql-size-large">除本合同另有约定外，卖方未按合同约定的期限将该房地产交付买方，自约定的交付期限届满次日起至实际交付日止，卖方以该房地产转让总价款为基数按日万分之______向买方支付违约金，合同继续履行。</span></p><p><strong class="ql-size-large">第十二条 【附随债务的处理】</strong></p><p><span class="ql-size-large">卖方在交付该房地产时，应将附随的水费、电费、煤气费、电话费、有线电视费、物业管理服务费、垃圾清运费等费用结清，单据交买方确认，否则买方有权从交房保证金中抵扣上述欠费。</span></p><p><strong class="ql-size-large">第十三条 【产权转移登记】</strong></p><p><span class="ql-size-large">买卖双方须在签订本合同______日内，共同向房地产权登记机关申请办理转移登记手续，卖方应按照机关的登记手续要求积极协助。</span></p><p><span class="ql-size-large">在收文回执载明的回复日期届满之日起______日内，买方须按本约定办理交纳税费的手续。</span></p><p><strong class="ql-size-large">第十四条 【其他违约责任】</strong></p><p><span class="ql-size-large">任何一方不履行本合同约定义务，致合同目的不能实现，守约方有权选择定金罚则或要求对方支付该房地产总价款百分之______的违约金。</span></p><p><strong class="ql-size-large">第十五条 【不可抗力】</strong></p><p><span class="ql-size-large">因不可抗力不能履行本合同的，根据不可抗力的影响，部分或者全部免除责任，但法律另有规定的除外。因不可抗力不能按照约定履行合同的一方当事人应当及时告知另一方当事人，并自不可抗力结束之日起______日内向另一方提供证明。</span></p><p><strong class="ql-size-large">第十六条 【本合同与其他文件的冲突解决】</strong></p><p><span class="ql-size-large">买卖双方在本合同签订之前的承诺及协议，如有与本合同不相符的，以本合同为准。</span></p><p><strong class="ql-size-large">第十七条 【合同附件】</strong></p><p><span class="ql-size-large">本合同共有附件______份。合同附件为本合同组成部分，具有同等法律效力。</span></p><p><strong class="ql-size-large">第十八条 【法律适用与纠纷解决】</strong></p><p><span class="ql-size-large">因本合同发生纠纷，由买卖双方协商解决。协商不成时，依据中华人民共和国法律，采取下列第______种方式解决：</span></p><p><span class="ql-size-large">1、向______仲裁委员会申请仲裁；</span></p><p><span class="ql-size-large">2、向房产所在地人民法院起诉。</span></p><p><strong class="ql-size-large">第十九条 【合同数量及持有】</strong></p><p><span class="ql-size-large">本合同一式 4 份，卖方 1 份，买方 1 份，其他交有关部门，均具同等法律效力。</span></p><p><strong class="ql-size-large">第二十条 【合同生效】</strong></p><p><span class="ql-size-large">本合同自买卖双方签署后立即生效。</span></p><p><span class="ql-size-large">卖方（签字）：____________&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;买方（签字）： ____________</span></p><p><span class="ql-size-large">______年______ 月______ 日&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;______年______ 月______ 日</span></p>',

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
                this.$router.push({path: '/document'})
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
                this.editor.content("test")
            }, 300)
        }
    }
</script>

<style lang="less">
    @import '../style/mixin';
    @import "../style/document";
    @import "../style/vueEdit";

    .edit_container {
        margin: 40px;
        padding-top: 0px;
        margin-top: -20px;
        margin-bottom: 40px;
        position: relative;
        overflow: hidden;
        border: 2px solid #ccc;

    }

    .editer {
        height: 600px;
        border: none;
    }

    .submit_btn {
        text-align: center;
    }
</style>
