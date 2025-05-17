# RQ//  
1.生成MR MR_generate文件夹  
生成MRs通过三种LLM 1.GPT 2.claude 3.Qwen  
 SelfcheckGPT 通过 GPT 三种模型的平均得分是 0.05	0.058333333	0.17083333 4o的结果最好  
 通过selfcheckGPT从这三种模型中自动选择评分最低的MR  
加州 与 德国 总共60条法规->60个MRs->2个RAG  
通过MR_generate/NEW.ipynb实现  

2.生成RAG 不同地区生成的MR可能存在重叠的情况 目前60条有两条是重复的。  
System.Matching_MR Qwen2.5VL+ChatGPT  
System.Matching_MR_LLM GPT_VL + ChatGPT   
System.Matching_MR_LLM GPT_VL + ChatGPT 的结果保存在Save中  

3.分离了画图和视频的程序，之前画图是4090 3090显卡显存会显示不足，因此换了一个4bit量化的画图程序
https://github.com/mit-han-lab/nunchaku
这个程序需要cuda 12.6
而Vista是采用的xformer的加速版本，因此3090只能安装12.1，需要分离这两个程序。
