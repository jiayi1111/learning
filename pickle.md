pickle的功能就是把你上次计算得到的数据保存起来，当你需要使用这些数据时，直接通过reload把数据恢复了就行.

这样的好处有：被pickle的数据，在被多次reload时，不需要重新去计算得到这些数据，这样节省计算机资源，如果你不pickle，你每调用一次数据，就要计算一次。通过pickle的数据，被reload时，可以更好的被内存调用，不需要经过数据格式的转换。

有人可能觉得，我直接通过open把数据写到一个txt文档也能达到以上的效果，但是这样做的结果是，你能够达到pickle的功能，把数据保存起来，但是当你再去调用这些数据时，你的txt格式的数据，没有pickle的数据读取更高效。

另外还有一点，你通过open把数据存储到txt中时的效率，就不如pickle的效率高。

综上，你如果只是做一次的数据存储和调用，以及数据量很小的情况下，你可以用open等方法保存数据和调用数据，但是当你需要通过大量计算得到一个数据，同时后期还会多次使用这个数据时，pickle的节省计算机资源的效果就出来了。

