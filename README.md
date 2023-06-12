# Certification-protocol1
仿真实验中共实现了三个角色，传感器、网关和控制中心。其中认证流程由传感器发起。首先传感器向网关发送认证请求 。网关收到传感器的认证请求后，向控制中心同时发送传感器和自己的认证请求 。控制中心收到网关发送的消息完成对传感器和网关的认证， 控制中心生成共享密钥并向网关发送消息 。网关通过对控制中心的认证并生成共享密钥，网关将消息发送给传感器。 传感器收到消息完成对控制中心的认证并生成共享密钥 。
有关传感器 的索赔事件定义如下：
(1) claim_A1(SN,Secret,SK); //会话密钥SK的保密性。
(2) claim_A2(SN,Alive); //角色SN的有效性。
(3) claim_A3(SN,Niagree); //信息的非主观同意。
(4) claim_A4(SN,Nisynch); //非主观的同步。
(5) claim_S1(SN,Secret,Ki); //传感器的保密信息Ki。
有关网关 的索赔事件定义如下：
(1) claim_A5(GWN,Secret,SK); //会话密钥SK的保密性。
(2) claim_A6(GWN,Alive); //角色GWN的有效性。
(3) claim_A7(GWN,Niagree); //信息的非主观同意。
(4) claim_A8(GWN,Nisynch); //非主观的同步。
(5) claim_S2(GWN,Secret,Kg); //网关的保密信息Kg。
有关控制中心 的索赔事件定义如下：
(1) claim_A9(CC,Secret,SK); //这是会话密钥SK的保密性。
(2) claim_A10(CC,Alive); //角色CC的有效性。
(3) claim_A11(CC,Niagree); //信息的非主观同意。
(4) claim_A12(CC,Nisynch); //非主观的同步。
(5) claim_S3(CC,Secret,Ci); //控制中心的保密信息Ci。
(6) claim_S4(CC,Secret,RMi); //控制中心的保密信息RMi。
(7) claim_S2(CC,Secret,Kg); //控制中心的保密信息Kg。
(8) claim_S1(CC,Secret,Ki); //控制中心的保密信息Ki。
