# Maximum-matching-algorithm
<ol>
<li>简介：正/逆向最大匹配算法实现中文分词</li>
<li>最大匹配算法</li>
  <ol>
    <li>正向最大匹配算法</li>
    初始化：指针p1指向句子的首位置，词的最大长度为m<br>
    算法执行：<br>
    A.	如果p1达到句子末尾，分词结束；<br>
    B.	假设当前判断的词的长度为i，初始化为m；<br>
    C.	p2 = p1 + i；如果p2超过句子的末尾，则i--，直到p2到达句子末尾之前；<br>
    D.	如果p1和p2之间的字符串S在词表中不存在，i--；<br>
    E.	如果p1和p2之间的字符串S在词表中存在，则S是一个词，p1 = p2 + I，转步骤A。<br>
    <li>逆向最大匹配算法</li>
    初始化时指针p1指向句子的末尾位置，其他类似
  </ol>
<li>评价指标</li>
  <ol>
    <li>正确率(Precision) = 正确识别的词数 /  识别出的个体总数</li>
    <li>召回率(Recall) = 正确识别的个体总数 /  测试集中存在的个体总数</li>
    <li>F值 = 正确率* 召回率 * 2 / (正确率 + 召回率)</li>
  </ol>
<li>程序</li>
  <ol>
    <li>数据</li>
    data/data.conll一个人工分好词的文件
    <li>代码</li>
    <ul>
      <li>make_data.py</li>将data.conll文件中的格式修改为：每行一句话，词语之间无空格，起名为data.txt
      <li>make_dict.py</li>给一个人工分好词的文件data.conll，构建一个词典，输出到一个文件中，起名为word.dict
      <li>mmp.py</li>正/逆向最大分词算法实现+评价程序
    </ul>
  </ol>
</ol>

