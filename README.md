![](./img/Kmeans.png)

Kmeans算法和Kmeas++算法比较结果如上图所示：
##Kmeans简要介绍
1. 从D中随机取k个元素，作为k个簇的各自的中心。
- 分别计算剩下的元素到k个簇中心的相异度，将这些元素分别划归到相异度最低的簇。
- 根据聚类结果，重新计算k个簇各自的中心，计算方法是取簇中所有元素各自维度的算术平均数。
- 将D中全部元素按照新的中心重新聚类。
- 重复第4步，直到聚类结果不再变化。
- 将结果输出。

##Kmeans++简要介绍
1.  从输入的数据点集合中随机选择一个点作为一个聚类中心
- 对于数据集中的每一个点x，计算它与最近聚类中心(指已选择的聚类中心)的距离D(x)
- 选择一个新的数据点作为新的聚类中心，选择的原则是：D(x)较大的点，被选取作为聚类中心的概率较大
- 重复2和3直到k个聚类中心被选出来
- 利用这k个初始的聚类中心来运行标准的k-means算法