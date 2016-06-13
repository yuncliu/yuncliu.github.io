:date: 2016-06-12 17:00
:tags: python
:category: tool
:title: numpy多项式

定义一个多项式: :math:`p = x^2 + 2x + 1`

.. code-block:: python

    import numpy as np
    p = np.poly1d([1, 2, 1])

运算,设有两个多项式: :math:`p_1 = (x^2 + 2x + 1), p_2 = (2x^2 - x +3 )`

.. code-block:: python

    >>> p1 = np.poly1d([1, 2, 1])
    >>> p2 = np.poly1d([2, -1, 3])
    >>> p1+p2
    poly1d([3, 1, 4])
    >>> p1-p2
    poly1d([-1,  3, -2])
    >>> p1*p2
    poly1d([2, 3, 3, 5, 3])
    >>> f_1 = np.poly1d([1, 0, 0, 0])
    >>> f_2 = np.poly1d([1, 0, 0])
    >>> f_1/f_2
    (poly1d([ 1.,  0.]), poly1d([ 0.]))

求根: :math:`f(x) = x^2 - 2x +1 = 0`

.. code-block:: python

    >>> f = np.poly1d([1, -2, 1])
    >>> np.roots(f)
    array([ 1.,  1.])

根据根求多项式

.. code-block:: python

    >>> f = np.poly1d([1, -2, 1])
    >>> r = np.roots(f)
    >>> np.poly(r)
    array([ 1., -2.,  1.])

多项式拟合:

.. code-block:: python

    %matplotlib inline
    import numpy as np
    import matplotlib.pyplot as plt

    x=np.array(range(0, 10)) * 10
    y = [i + np.random.normal(0, 5) for i in x]
    f = np.poly1d(np.polyfit(x, y, 1))
    y_1 = [f(i) for i in x]
    plt.plot(x, y, '*')
    plt.plot(x, y_1, '-')
    plt.show()
