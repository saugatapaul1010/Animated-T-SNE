# Animated-T-SNE
Dimensionality reduction technique using Animated T-Distributed Stochastic Neighborhood Embedding. This repository is for self reference.

# tsne_animate (0.1.4)
Animation generation for scikit-learn's t-sne algorithm

Strong advice - use tensorboard, it's not so complicated. 

But if you want dirty quick visualisation - here we go.


Requirements:
```
ffmpeg or mencoder  to save gifs
```


Easy to install:  
```
$ pip install tsne_animate
```

Easy to use:
```python
from sklearn import datasets, manifold
from tsne_animate import tsneAnimate
digits = datasets.load_digits()
tsne = tsneAnimate(manifold.TSNE(learning_rate=1000))
tsne.animate(digits.data,digits.target)
```

![digits](https://github.com/saugatapaul1010/Animated-T-SNE/blob/master/examples/digits.gif)

```python
from sklearn import datasets, manifold
from tsne_animate import tsneAnimate
iris = datasets.load_iris()
tsne = tsneAnimate(manifold.TSNE(learning_rate=50))
tsne.animate(iris.data,iris.target,0,'iris.gif')
```

![iris](https://github.com/saugatapaul1010/Animated-T-SNE/blob/master/examples/iris.gif)
