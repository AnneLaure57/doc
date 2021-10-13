# FAQ

## Difference between import and use ? (For Package Diagram)

<p style="text-align:justify;"> Generally, the use dependency indicates that a model element - not necessarily a package - requires another model element for its implementation , whereas the import dependency is more specific to a package and indicates that the importing package's namespace is amended by the imported package.

However, you were asking for the use of both of the dependencies in a package diagram: In this case, I would interpret the use dependency as a looser coupling (e.g. package A just "uses" something from package B). In contrast, the import dependency specifically refers to each element of the imported package with an impact on the namespace.

The difference from a language view is that in the use case you just pick certain parts from a package while the import takes all. Most programming languages take imported packages into their scope so you address elements from the package as being part of the importing itself. For the used ones you usually qualify the namespace.</p>

[![Generic badge](https://aleen42.github.io/badges/src/stackoverflow.svg)](https://stackoverflow.com/questions/29744168/whatre-the-differences-between-use-and-import-dependencies)
