It would be nice if the included `geom_step` example did not throw, but behaved more like the included `geom_line` example.

``` r
library('ggplot2')
d <- data.frame(x=1,y=1)
```

``` r
ggplot(data=d,aes(x=x,y=y)) + geom_point()
```

![](StepThrow_files/figure-markdown_github/pointplot-1.png)

``` r
ggplot(data=d,aes(x=x,y=y)) + geom_line()
```

    ## geom_path: Each group consists of only one observation. Do you need to
    ## adjust the group aesthetic?

![](StepThrow_files/figure-markdown_github/lineplot-1.png)

``` r
ggplot(data=d,aes(x=x,y=y)) + geom_step()
```

    ## Error in grid.Call.graphics(L_lines, x$x, x$y, index, x$arrow): invalid line type

![](StepThrow_files/figure-markdown_github/steplot-1.png)
