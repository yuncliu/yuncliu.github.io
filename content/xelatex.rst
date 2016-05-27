:date: 2016-05-27 17:00
:tags: latex
:category: tool
:title: 在latex中使用中文

如果要使用中文需要用xelatex包，编译时用xelatex来生成pdf

.. code-block:: tex

    \documentclass{aritcle}
    \usepackage{xeCJK}
    \setCJKmainfont{Microsoft YaHei}
    \begin{document}
    中文
    \end{document}

如果配合sphinx使用，可以修该conf.py中latex_elemments部分
在preamble中添加上xeCJK包

.. code-block:: python

    latex_elements = {
    # The paper size ('letterpaper' or 'a4paper').
    #'papersize': 'letterpaper',

    # The font size ('10pt', '11pt' or '12pt').
    'pointsize': '12pt',

    # Additional stuff for the LaTeX preamble.
    'preamble': """\usepackage{xeCJK}
    \setCJKmainfont{Microsoft YaHei}""",
    # Latex figure (float) alignment
    #'figure_align': 'htbp',
    }

在编译时使用

.. code-block:: sh

    make latexpdf PDFLATEX=xelatex

就能得到漂亮的pdf文档
