# 覆盖索引
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在SQLite中，做一个索引查找时，查找一行通常是在索引上做一个二分查找来查找索引项，然后从索引中提取rowid并且使用rowid在原始表上做二分查找。所以，一个典型的索引查找包含两个二分查找。然而，如果从表中取出的所有列在索引中都是可以得到的，SQLite会使用索引中包含的值，并且不会查找原始表中的行。这为每一行节约了一个二分查找并且可以让多数的查询运行速率提高一倍。<p>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;当一个索引包含查询所需要的所有数据并且原始表不再被请求时，我们称这种索引为“覆盖索引”。<p>
程序实现如下：
<img src="coverindex.png"/>