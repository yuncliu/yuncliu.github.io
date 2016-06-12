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
