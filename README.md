# cons-capra07-plot 

R script that visualizes a residue conservation in a MSA based on Jensen-Shannon divergence. 

## Description 

* This script is used only for https://github.com/shin-kinos/cons-capra07 
* It visualizes a result with lollipop plot.

## Dependencies 

### R 

Version `4.1.0` or more. 

```
version.string R version 4.1.0 (2021-05-18)
```

### Tidyverse 

* https://www.tidyverse.org/

Version `1.3.1` or more.

```
> packageVersion( "tidyverse" )
[1] ‘1.3.1’
```

### ggplot2 

* https://ggplot2.tidyverse.org/

Version `3.3.5` or more.

```
> packageVersion( "ggplot2" )
[1] ‘3.3.5’
```
### ggrepel 

* https://cran.r-project.org/web/packages/ggrepel/vignettes/ggrepel.html

Version`0.9.1` or more. 

```
> packageVersion( "ggrepel" )
[1] ‘0.9.1’
```

## Input file format
A result file of https://github.com/shin-kinos/cons-capra07 

See some demo files in `demo` directory.

## Usage 

Major arguments.

* `-i` : Input file name, REQUIRED.
* `-o` : Output file name. REQUIRED.
* `-c` : Types of colour gradient.
* `-w` : Size of width (px).
* `-h` : Size of height (px). 

### Annotation of high-ranked conservation scores 

This program can annotate the sites that are quantified in TOP *n* high conservation scores with `-t` option ( e.g., if `-t 30`, TOP 30 conservation sites are annotated. ). 

If you will not need any annotations, set `-t 0`.

[e.g.]

```
% Rscript cons-capra07-plot.r -i cons-capra07_output_01.out -o output -c 1 -t 20
```

## Output
A Lollipop plot graph in PNG format.

[e.g.] 


```
% Rscript cons-capra07-plot.r -i cons-capra07_output_01.out -o window_test -c 1 -t 20
```

![plot_out_01](https://user-images.githubusercontent.com/83740080/141028716-83234491-62fe-4107-93ec-11632a32e338.png)

```
% Rscript cons-capra07-plot.r -i cons-capra07_output_02.out -o plot_out_02 -c 2 -t 0
``` 

![out_plot_02](https://user-images.githubusercontent.com/83740080/141027796-e63f15e9-c96c-46eb-be10-aaacfa7ce60c.png) 

```
% Rscript cons-capra07-plot.r -i cons-capra07_output_03.out -o plot_out_03 -c 4 -t 20
``` 

![plot_out_03](https://user-images.githubusercontent.com/83740080/141028180-dc9e6d29-62c8-4a01-870c-d23533095384.png) 
