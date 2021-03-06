### Deep learning analysis of left ventricular myocardium in CT angiographic intermediate-degree coronary stenosis improves the diagnostic accuracy for identification of functionally significant
CT血管造影中度狭窄的左心室心肌深度学习分析提高了功能性重度狭窄的诊断准确率

- 评价静息冠状动脉CT血管造影（CCTA）中左心室心肌深度学习（DL）分析对判断冠状动脉狭窄程度（DS）的附加价值，以鉴别功能性冠状动脉狭窄患者。
- 医学知识

	- 在医学上又叫非创伤性血管成像技术（简称CT血管造影即CTA），血管造影是一种介入检测方法，显影剂被注入血管里，因为X光穿不透显影剂，血管造影正是利用这一特性，通过显影剂在X光下的所显示影像来诊断血管病变的。
	- 2018年
	- LVM

		- 左心室心肌

	- DS

		- 冠状动脉狭窄

	- 血流储备

		- 血流储备分数（FFR）是评价冠脉缺血的“金标准”，对指导临界病变、多支病变、分叉病变等复杂病变的介入治疗具有重要意义，基于FFR值≥0.75决定临界冠脉狭窄予药物治疗是可行的，与冠脉狭窄相关的心源性猝死和急性心肌梗死年发生率均＜1%，而且不因置入支架而降低。



- 内容

	- 方法

		- 回顾性选择在有创部分血流储备（FFR）测量前接受CCTA的患者。CCTA中的最高DS用于将患者分类为无显著性差异(≤24%DS）、中等（25-69%DS）或显著狭窄(≥70%DS）。中度狭窄的患者转诊进行左室肥厚的全自动DL分析。DL算法的特点是LVM，以及关于形状、纹理、对比度增强等可能的编码信息。基于这些编码，提取特征并将患者分类为无显著或显著狭窄。评价联合法的诊断性能，并与单纯DS法进行比较。功能性显著狭窄定义为FFR≤0.8或存在血管造影高度狭窄(≥90%DS）。

			- 显著狭窄不用综合考虑，中度狭窄结合lvm考虑
			- 首先 (1)，LVM 使用多尺度卷积神经网络 (CNN) 自动分割。多尺度 CNN 包括两个相同的流；每个都分析从轴向、冠状和矢状图像切片中以单一尺度（黑色和红色方块）获取的一组三平面输入块，目标体素位于其中心。每组都使用卷积 (conv)、最大池化 (MP) 和全连接 (FC) 层的组合进行处理。最后，单个体素被分类为心肌或背景。这是在所有 CT 切片上执行以分割整个心肌。在下一阶段分析所有 LVM 体素。第二（2），该算法使用卷积自动编码器 (CAE) 以无监督方式在所有 CT 切片上表征（编码）LVM。CAE 包含两部分，编码器和解码器。编码器通过卷积层和最大池化层将数据压缩为较低维度的表示。解码器通过反卷积（deconv）和上采样（US）层扩展压缩形式以重构输入数据。为了表示整个 LVM，所有 LVM 体素（在所有 CT 切片上）的编码统计数据被用作特征。第三（3），基于提取的特征，使用支持向量机（SVM）将患者分类为有或没有功能上显着的冠状动脉狭窄的患者。

	- 结果

		- 2012 年至 2016 年间最终研究人群包括126名患者（77%男性，59±9岁）。81例（64%）有明显的功能性狭窄。与仅基于DS的分类（AUC=0.68）相比，该方法提高了鉴别能力（AUC=0.76）。对DS的敏感性和特异性分别为92.6%和31.1%(≥50%表示功能性严重狭窄），84.6%和48.4%表示建议的方法。

	- 结论

		- 对中度冠状动脉狭窄患者的LVM进行DS与DL分析相结合，可提高对功能性严重冠状动脉狭窄患者的诊断水平。

