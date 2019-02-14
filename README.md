# 中文关系抽取以及知识图谱的构建论文解析
## 中文特殊的语言现象
* 英文单词之间依照空格进行分割，中文没有明显的分割符号
* 英文按照时态区别时间关系，中文则需要根据上下文进行判断

      Tomas 在肯德基吃早饭
  
      Tomas eat breakfast at KFC
      
      Tomas will eat breakfast at KFC
 
* 英文通过介词连接同一句话中的多个谓语，中文则不需要
  
      乔丹是美国职业篮球运动员，出身在纽约。
  
      Jordan is an American Professional basketball player who was born in NewYork.
 
   因此在英文中表现优异的关系抽取模型往往在中文中表现一般
 ## 三种处理方法
 * 伪实体的处理
 
       奥巴马总统访问中国。
       The President Obama visited China
       
   英文中通常喜欢把主语放在句首或者借助介词president Obama、the Police of Washington，在中文中，我们要先把伪实体关系“总统访问中国”提取出来，之后提取
   “奥巴马访问中国”
 * CLVC现象
   
        CLVC是指轻动词通常跟着名词，动词跟着介词，而介词的位置通常不确定，这种情况经常出现，如：
        
        中文：巴拿马与中国在2017年建立外交关系
        
        英文：Panama established diplomatic relations with China. 
        
        实际处理过程中，英文采取Verb-noun-preposition的形式，
        而这种在中文数据中行不通，中文往往有更加灵活的位置（eg.提前介词)“与巴拿马建立外交关系”
    
    采用语义依存句分析-哈工大
  ![](https://raw.githubusercontent.com/Elliotter/Chinese-Open-Relation-Extraction-and-Knowledge-Base-Establishment/master/image.png)
    
    
        
        
