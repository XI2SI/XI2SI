# Docsify

## Equations

In this equation $\ref{eq:heart_curve}$ or $\eqref{eq:heart_curve}$

$$
\begin{equation}
\label{eq:heart_curve}
(x^2 + y^2 - 1)^3 - x^2 y^3 = 0
\end{equation}
$$

## SVG

<svg width="200" height="200" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
  <path
    d="M100,150
       C60,110 30,80 30,50
       C30,30 45,20 60,20
       C75,20 90,30 100,50
       C110,30 125,20 140,20
       C155,20 170,30 170,50
       C170,80 140,110 100,150 Z"
    fill="none"
    stroke="red"
    stroke-width="3"
    stroke-linejoin="round" />
</svg>

## Code

```python
import numpy as np
import matplotlib.pyplot as plt


def heart_curve(x, y):
    return (x**2 + y**2 - 1)**3 - x**2 * y**3


x = np.linspace(-1.5, 1.5, 1000)
y = np.linspace(-1.5, 1.5, 1000)
X, Y = np.meshgrid(x, y)

Z = heart_curve(X, Y)

plt.figure(figsize=(8, 8))
contour = plt.contour(X, Y, Z, levels=[0], colors='red', linewidths=3)
plt.fill_between([], [], color='red', alpha=0.3)

plt.title('Heart Curve: $(x^2 + y^2 - 1)^3 - x^2 y^3 = 0$', fontsize=14, pad=20)
plt.xlabel('x')
plt.ylabel('y')
plt.grid(True, alpha=0.3)
plt.axis('equal')
plt.xlim(-1.5, 1.5)
plt.ylim(-1.5, 1.5)

plt.axhline(y=0, color='k', linestyle='-', alpha=0.3)
plt.axvline(x=0, color='k', linestyle='-', alpha=0.3)

plt.show()
```

## Anchor

In this study [Vaswani, A., et al. (2017)](#c_neurips_vaswani2017attention), ...

As shown in Table [1](#tab1), ...

## Mermaid

``` mermaid
graph TD
    A[Initial Population] --> B[Mutation]
    B --> C[Crossover]
    C --> D[Selection]
    D --> E{Termination Criteria}
    E -->|No| F[Next Generation]
    E -->|Yes| G[Optimal solution]
    F --> B

    style A fill:#e1f5fe
    style G fill:#e8f5e9
    style E fill:#fff3e0
```

## Markmap

```markmap
# markmap

## Links

- [Website](https://markmap.js.org/)
- [GitHub](https://github.com/gera2ld/markmap)

## Related Projects

- coc-markmap for Neovim
- markmap-vscode for VSCode
- eaf-markmap for Emacs
```

## Include

>Empty files are not permitted.

```markdown
[](Zotero.md ':include')
```

## Tables

<div id="tab1"></div>

|      | ICLR | NeurIPS |
|------|------|---------|
| 2024 | 2260 |    4494 |
| 2023 | 1572 |    3540 |

## References

<div id="c_neurips_vaswani2017attention">
    Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, L., and Polosukhin, I. (2017). Attention is all you need. Advances in neural information processing systems.
</div>
