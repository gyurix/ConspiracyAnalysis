# ConspiracyAnalysis

## About

In this project we analyze the tweets of an exported twitter database for various conspiracy theories.

You can find a short description and the links to the articles related to the analysed conspiracy theories in the beginning of the Jupyter Notebooks.

## Solutions

In this repository I provide two possible solutions for the tasks of the project.

The first solution is the [PythonSolution](https://github.com/gyurix/ConspiracyAnalysis/blob/master/PythonSolution.ipynb) which prefers solving subtasks by applying
all the neccessary calculations in Python, that way minimizing the database load. This solution is the best when we prefer optimizing for performance on
not neccessary optimized postgresql databases over code simplicity.

The second solution is the [DBLevelSolution](https://github.com/gyurix/ConspiracyAnalysis/blob/master/DBLevelSolution.ipynb) which prefers solving subtasks by applying
most of the neccessary calculations on the database level. This solution has a much smaller source code base and because of that it's much more readable &
understandable, than the first solution. However this solution requires a properly optimized postgresql database configuration for being able to run in a reasonable time.

## Runtime

The measured runtimes on the VPS used for development with optimized postgresql settings were:

- **First solution:** 3 minutes, 20 seconds (~20% faster than the second solution)
- **Second solution:** 4 minutes, 10 seconds (~25% slower than the first solution)

## Conclusion

Even tho the second solution performed slower, than the first one, if there are no special requirements for super high performance, then it's worth solving similar
tasks using the second solution to significantly reduce the overall development time, code complexity and the potential errors in the code.
