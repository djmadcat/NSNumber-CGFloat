# NSNumber-CGFloat

NSNumber+CGFloat is an category to get CGFloat value from NSNumber object and create NSNumber object with CGFloat value.

## Overview

Many developers forget that type `CGFloat` is defined and just assume that `CGFloat` is `float`, but it is not so.

See CoreGraphics/CGBase.h for further information:

``` objective-c
/* Definition of `CGFLOAT_TYPE', `CGFLOAT_IS_DOUBLE', `CGFLOAT_MIN', and
   `CGFLOAT_MAX'. */

#if defined(__LP64__) && __LP64__
# define CGFLOAT_TYPE double
# define CGFLOAT_IS_DOUBLE 1
# define CGFLOAT_MIN DBL_MIN
# define CGFLOAT_MAX DBL_MAX
#else
# define CGFLOAT_TYPE float
# define CGFLOAT_IS_DOUBLE 0
# define CGFLOAT_MIN FLT_MIN
# define CGFLOAT_MAX FLT_MAX
#endif

/* Definition of the `CGFloat' type and `CGFLOAT_DEFINED'. */

typedef CGFLOAT_TYPE CGFloat;
#define CGFLOAT_DEFINED 1
```

## Contact

Alexey Aleshkov

- https://github.com/djmadcat
- https://twitter.com/coreshock
- djmadcat@gmail.com

## License

NSNumber-CGFloat is available under the BSD 2-Clause license. See the `LICENSE` file for more info.
