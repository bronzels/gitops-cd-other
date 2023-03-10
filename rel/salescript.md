```mermaid
graph LR
智能坐席实时辅助--> 1A(需求分析)
1A-->2A(痛点)
2A-->标准话术手册+宣讲式培训效果不佳
2A-->初级销售无法准确判断当前对话状态对应标准流程的哪一步
2A-->标准流程话术的设计稍复杂情况下很难在实时对话场景中严格遵循
2A-->不同情况客户应推荐的产品/套餐的标准化要求很难在实时对话场景中严格遵循
2A-->客户实时沟通中资料无提取保存或者不及时不全面或者后续对话中遗忘/未参考
1A-->2B(安全需求)
2B-->客户在对话中提供的电话号码/年级等个人信息或服务反馈从商业竞争和隐私角度需要严格保密
2B-->销售在对话中提供的产品/套餐的价格和服务细节信息从商业竞争角度需要严格保密
1A-->2C(核心需求)
2C-->实时根据客户对话内容判断客户意图和当前话术流程阶段
2C-->根据当前话术阶段和上下文推荐标准话术文本
2C-->支持无需填充的固定话术文本和可按模板配置填充的话术文本
2C-->可实时保存用户在对话中提供的信息
2C-->可在后续话术生成中使用以前对话中用户提供的信息
2C-->用户实时会话中提取和展示信息
1A-->2D(技术需求)
2D-->可同时接入呼叫中心语音流和微信文本流
2D-->通话信息接受到辅助信息显示最大时间间隔不能超过1.5s
2D-->微信和呼叫中心业务量比例-->从查表计算相同时间段内累计字符数的角度大概微信/语音=2/1
微信和呼叫中心业务量比例-->从部分销售人员调研的角度多数人说微信比语音多也有个别说语音比微信多

智能坐席实时辅助-->1B(整体技术方案)
1B-->微信-->微管家-->第三方实时坐席辅助引擎-->实时坐席辅助阿卡索IT前端
微管家-->实时坐席辅助阿卡索IT前端
1B-->3家第三方呼叫中心-->实时ASR转写-->第三方实时坐席辅助引擎
1B-->admin系统新后台-->实时坐席辅助阿卡索IT前端
1B-->第三方坐席辅助后台管理
1B-->第三方质检等后台管理

智能坐席实时辅助-->1C(风险分析)
1C-->2E(性能风险)
2E-->微信/微管家/坐席辅助或者呼叫中心/ASR/坐席辅助长链条系统-->对策是前端和第三方直接对接或者第三方开发前端
2E-->多模型调用-->详细了解话术提示性能写入合同
1C-->2F(运营风险)
2F-->集成复杂度高出现问题解决难度大-->尽量从单一第三方采购和作为总包集成能完成长期集成方案运营阿卡索只负责流程话术等核心数据运营
2F-->实时ASR私有部署需要10+服务器资源-->对策是在公司内网部署节省成本可靠性不高
2F-->部分技术还未经过大量客户应用缺乏完整后端管理功能-->对策是评估使用成熟技术给运营带来难度尽量不使用未成熟技术
2F-->流程和话术的挖掘/制定/更新需要借助专家经验-->对策是虽然交付周期不需要甲方参加运营尽量全程深度参与
1C-->2G(使用风险)
2G-->调研中部分销售人员建议只用在微信场景-->对策是增大调研样本和完善调研方式

智能坐席实时辅助-->1H(方案选择)
1H-->2R(第三方合作)
2R-->第1选择竹间
2R-->第2选择循环
2R-->第3选择追一
2R-->3RQ(具体产品组件或定制开发功能)
3RQ-->4RR(实时坐席辅助)
3RQ-->4RS(坐席辅助后台管理)
3RQ-->4RT(ASR自研或者分销集成)
3RQ-->4RU(质检)
3RQ-->4RW(陪练)-->只有竹间有
2R-->3RR(优势是功能丰富的整体解决方案)
2R-->3RS(劣势是较高的成本)
1H-->2S(第三方竹间的智能陪练)
2S-->3SR(优势是现成解决方案较短实施时间比全套采购成本低)
2S-->3SS(劣势是单独采购性价比不高)
1H-->2U(自研实时话术辅助)
2U-->3UR(范围限定在微信接入)
3UR-->除微管家接口外暂时避免大额ASR采购
3UR-->微信作为试验成功后在另外立项支持语音
2U-->3US(数据战略部负责产品定义/项目管理/技术方案)
2U-->3UT(IT负责前端实现)
2U-->3UU(数据战略部负责销售流程/话术的设计和挖掘)
2U-->3UV(数据战略部负责后端设计和实现)
2U-->3UW(数据战略部负责文本的意图识别/实体抽取算法和对话状态管理对话策略算法)
2U-->3UX(优势是节省成本)
2U-->3UY(劣势是比第三方采购缺少语音支持无后台分析报表功能无打标训练等NLP机器学习平台功能)


```

