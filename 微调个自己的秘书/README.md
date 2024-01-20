刚开始时照猫画虎，对着这个教程准备微调数据。

https://github.com/InternLM/tutorial/blob/main/xtuner/README.md

一共准备了下面8条数据，并把它转换为jsonl格式用于微调。

![Alt text](image.png)

最后用于微调的配置长这样，我只改了模型地址、数据地址、epochs，其他都是按教程改的，刚开始时是用8个数据微调1000个epochs，产生的checkpoint高达1T，结果被一双黑手制裁了，把我的配置文件和checkpoint都删了。后来我把数据复制了256遍，把checkpoint改成30，才得以微调成功。

![Alt text](image-2.png)

被我复制了256遍的数据长这样。

![Alt text](image-1.png)

接下来看看微调效果，先看看其他场景下的回答，

![Alt text](62fff55bed25494a19eb8009101574c.png)

显然，没有发生灾难性遗忘的情况。

再问我微调它的数据试试。

![Alt text](d7a3ed0dba4caf2373ee46b5b01e969.png)

感觉除了对自己没有认知外，就没有什么问题了。

再试试。

![Alt text](6992ef5a2986cce3c1ada9ec56f5fd9.png)

前面胡言乱语了一下，现在连我都说不清是谁了

![Alt text](948c59ffad9c9d24c0229b6a6ebf7b0.png)

专业错了，是人工智能。

![Alt text](ee1e48ae69c34b8ca01f8cd0ea1473d.png)

LLM又抽风了。

![Alt text](66a29d337f65281e511fd1ff8656297.png)

又答错了。

![Alt text](0d8555922b361b26d0afee686160fed.png)

又犯病了……

看来这模型还是有点问题的，不过我也不知道怎么改了，就这样吧。