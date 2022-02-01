Resumen de Librería PURR
================
Christian Gabriel Bernedo
31/1/2022

### La librería PURR podemos encontrarla en la colección tidyverse, este paquete es una herramienta que quisas no es tan conocida como otras de tidyverse como dplyr o ggplort2, pero esta tambien es muy importante como herramienta funcioanal de programación en R.

### Se dice que es una herramienta funcional en programación de R porque es sinteticamente estable, tambien se puede recordar sencillamente, a su vez simplifica diversos códigos de tidyverse, pero un punto negativo es que se ejecuta más lento que las funciones lapply.

### Esta librería trabaja con listas y en ella puede: filtrar, resumir, cambiar formas o unirlas, además de crear blucles for.

### Por ultimo su función estrella es “map”, esta aplica una función determinada a cada elemento de una lista. De ella se derivan otras funciones como map2 o map.

## Ejemplo:

``` r
library(tidyverse)
```

    ## Warning: package 'tidyverse' was built under R version 4.1.2

    ## -- Attaching packages --------------------------------------- tidyverse 1.3.1 --

    ## v ggplot2 3.3.5     v purrr   0.3.4
    ## v tibble  3.1.6     v dplyr   1.0.7
    ## v tidyr   1.1.4     v stringr 1.4.0
    ## v readr   2.1.1     v forcats 0.5.1

    ## Warning: package 'ggplot2' was built under R version 4.1.2

    ## Warning: package 'tidyr' was built under R version 4.1.2

    ## Warning: package 'purrr' was built under R version 4.1.2

    ## Warning: package 'dplyr' was built under R version 4.1.2

    ## Warning: package 'forcats' was built under R version 4.1.2

    ## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
marcas=c("nissan","toyota","chebrolet")
años=c(1997,1965,2008)
pais=c("España", "Mexico", "Perú")
autos=list("marcas", "años","pais") 
# calcular el numero de elemento de cada sublista
map_int(autos, length)
```

    ## [1] 1 1 1
