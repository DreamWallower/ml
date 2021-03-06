<h1 align=center>Knn.h</h2>
<h6 align=center>Author: Jachin Fang</h6>
</br>
</br>

The Pattern Recognition Library <Knn.h> header.

<blockquote>
&emsp; K-nearest-neighbor(kNN) classification is one of the most fundamental and simple classification methods and should be one of the first choices for a classification study  when there is little or no prior knowledge about the distribution of the data.
</blockquote>
</br>

##### REFENCE

<blockquote>
&emsp; Cover T, Hart P. Nearest neighbor pattern classification[M]. IEEE Press, 1967.
</blockquote>
</br>

##### How to use

For example, here is some data:
```c++
vector<double> data{ 1, 101, 5, 89, 108, 5, 115, 8 }; 
vector<string> labels{ "A", "A", "B", "B" };
unsigned int dim = 2;
unsigned int size = 4;

``` 

And here is test data:
```c++
vector<double> test{ 10, 202 };
```

</br>

Then

```c++
#include <Knn.h>
``` 

```c++
Knn<double, string> knn;
knn.init(data, dim, labels, size); 
string result = knn.classify(test)[1]; /* 1-NN */
string result2 = knn.classify(test)[3]; /* 3-NN */
```

Or
```c++
Knn<double, string> knn;
knn.init(data, dim, labels, size); 
knn.classify(test); 
string result = knn[1]; /* 1-NN */
string result2 = knn[3]; /* 3-NN */
```

