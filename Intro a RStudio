4+2
4^2
## alt + 94  = ^
View(orangeec)
x <- 86
y = 100

Oficina = 7
Platzi = 1
Transporte = 1.5
Tiempo_al_dia = Oficina + Platzi + Transporte
Tiempo_al_dia

str(mtcars)
# variable 'factor' = variable categorica = NO NUMERICA
# variable 'num' = numérica entera o decimal
# variable 'int'(integer) = numerica Entera solamente
# variable Booleano : 0/1 ; True/False
attributes(mtcars)
length(mtcars)
attributes(mtcars)
typeof(mtcars)
str(mtcars)
str(mtcars$model)
str(mtcars$mpg)
?mtcars
class(mtcars$vs)

# convirtiendo variable 'vs' de Int a Logical porque el tipo de dato es Booleano y no entero
mtcars$vs = as.logical(mtcars$vs)
mtcars$am = as.logical(mtcars$am)

str(mtcars)
str(orangeec)
View(orangeec)
?orangeec
??orangeec
################
### AL IMPORTAR , AGREGAR LA OPCIÓN DE 'HEADING'
summary(orangeec)
str(orangeec)
summary(orangeec)
summary(mtcars)
## transformando 'mtcars$wt' de libras a kg
wt <- (mtcars$wt*1000)/2
wt

mtcars.new <- transform(mtcars,wt=wt*1000/2)
mtcars.new

summary(mtcars.new)
View(mtcars.new)
?mtcars

############## CLASE 8 (VECTORES) ###############

tiempo_platzi <- c(25,5,10,15,10)
tiempo_lecturas <- c(30,10,5,10,15)
tiempo_aprendizaje <- tiempo_platzi + tiempo_lecturas
tiempo_aprendizaje

dias_aprendizaje <- c("Lunes", "Martes", "Miercoles", "Jueves", "Viernes")
dias_aprendizaje

ifelse(tiempo_aprendizaje > 20, "TRUE", "FALSE")
dias_mas_20min <- ifelse(tiempo_aprendizaje > 20, "TRUE", "FALSE")
dias_mas_20min

total_tiempo_adicional <- sum(tiempo_platzi) + sum(tiempo_lecturas)
total_tiempo_adicional

####### CLASE 9 (MATRICES) ######
    ## si tiene los mismos tipos de datos es MATRIZ, si tiene distintos entonces es DATA FRAME

tiempo_matrix <- matrix(c(tiempo_platzi, tiempo_lecturas),
                        nrow = 2, byrow = TRUE)

dias <- c("Lunes", "Martes", "Miercoles", "Jueves", "Viernes")
Tiempo <- c("tiempo platzi", "tiempo lecturas")

colnames(tiempo_matrix) <- dias
rownames(tiempo_matrix) <- Tiempo

tiempo_matrix

colSums(tiempo_matrix)
rowSums(tiempo_matrix)


#### CLASE 10 (EJERCICIO CON AMTRICES)
  ## rbind (rowbind) para agregar una fila/columna a la matriz

final_matrix <- rbind(tiempo_matrix,c(10,15,30,5,0))
final_matrix

rownames(final_matrix)[3] <- "tiempo extra"
final_matrix

colSums(final_matrix)

final_matrix2 <- cbind(final_matrix,c(15,20,10))
final_matrix2
colnames(final_matrix2)[6] <- "Sabado"
final_matrix2

### CLASE 11 (OPERADORES)
  ## == igual
  ## != no igual/diferente
  ## < , <= , >= , >
  ## | o
  ## ! No
  ## %in% 'que esté en el dataset

  ## ',' al final R buscará en TODAS las observaciones
mtcars[mtcars$cyl<6, ]

orangeec[orangeec$GDP.PC>=15000,]

orangeec[orangeec$Creat.Ind...GDP<=2,]

neworangeec <- subset(orangeec, Internet.penetration...population > 80
                      & Education.invest...GDP >= 4.5)

neworangeec

 ## similar al anterior pero usamos 'select' para seleccionar columnas/variables

neworangeec <- subset(orangeec, Internet.penetration...population > 80
                      & Education.invest...GDP >= 4.5,
                      select = Creat.Ind...GDP)

neworangeec

## para cambiar nombre a variables
install.packages("plyr")
library(plyr)

rename(orangeec,c("Creat.Ind...GDP"="AporteEcNja"))

              ### CLASE 12 (FACTORES) ###

Nivel_Curso <- c("Básico", "Intermedio", "Avanzado")
Nivel_Curso

# head()/tail() para ver las cabezas de datasets, 6 primeros/ultimos datos
head(mtcars)
head(orangeec)

tail(mtcars)
tail(orangeec)

#otra forma de dar un vistazo a dataset
install.packages("dplyr")
library(dplyr)

glimpse(orangeec)
glimpse(mtcars)

#crear lista list() para juntar datos mostrandolos por separado
my_vector <- 1:8
my_vector
my_matrix <- matrix(1:9, ncol = 3)
my_matrix
my_df <- mtcars[1:4,]
my_df
my_list <- list(my_vector,my_matrix,my_df)
my_list


            ### CLASE 13:16 EDA: EXPLORATORY DATA ANAYLISIS ###

## Cuarteto de Anscombe: analizar data antes (histograma, scatterplot y boxplot)
    #histograma tiene estilo fijo y nos muestra lo que hay y lo que no hay
    #boxplot muestra min, max, 1er, mediana y 3er cuartil

  # alt + 126 = ~
plot(mtcars$mpg ~ mtcars$cyl,
     xlab="cilindros", ylab = "millas por galón", 
     main="Relación cilindros y millas por galón")

plot(mtcars$mpg ~ mtcars$hp,
     xlab="caballos de fuerza", ylab = "millas por galón", 
     main="Relación caballos de fuerza y millas por galón")

plot(orangeec$Unemployment ~ orangeec$Education.invest...GDP,
     xlab="Inversión en educación (%PBI)",
     ylab = "Desempleo",
     main = "Relación entre educación y desempleo")

plot(orangeec$GDP.PC ~ orangeec$Creat.Ind...GDP,
     xlab="Aporte economia naranja al PBI(%)",
     ylab = "PBI per cápita",
     main = "Relación entre economía naranja y PIB per cápita")

#################
plot(orangeec$GDP.Growth.. ~ orangeec$Creat.Ind...GDP,
     xlab="Aporte economia naranja al PBI(%)",
     ylab = "Crecimiento PIB del país",
     main = "Relación entre economía naranja y crecimiento PIB")
#################


      ##### CLASE 17 : EDA CON HISTOGRAMAS #####

install.packages("ggplot2")
library(ggplot2)

qplot(mtcars$hp,
      geom="histogram",
      xlab="caballos de fuerza",
      main="carros según caballos de fuerza")


# (x=hp) para señalar la variable 'hp' del dataset
ggplot(mtcars, aes(x=hp)) +
  geom_histogram() +
  labs(x="caballos de fuerza", y="cantidad de carros",
       title = "Caballos de fuerza en carros seleccionados")

# para quitarle el fondo en el gráfico anterior:
ggplot(mtcars, aes(x=hp)) +
  geom_histogram() +
  labs(x="caballos de fuerza", y="cantidad de carros",
       title = "Caballos de fuerza en carros seleccionados")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

#ajustando el ancho de la barra con 'binwidth' en 'geom_histogram'
ggplot(mtcars, aes(x=hp)) +
  geom_histogram(binwidth = 30) +
  labs(x="caballos de fuerza", y="cantidad de carros",
       title = "Caballos de fuerza en carros seleccionados")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

###########################################
ggplot(mtcars, aes(x=cyl)) +
  geom_histogram(binwidth = 1) +
  labs(x="cilindros", y="cantidad de carros",
       title = "cilindros en carros seleccionados")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

###########################################

#ajustando el eje X y ponerle color al histograma y ponerle instruccion en forma distinta
  # xlim = limite de X (valores base en eje X)

  #Hist. mtcars
ggplot() + geom_histogram(data=mtcars,
                          aes(x=hp), fill="blue", color="red",
                          binwidth = 20) +
  labs(x="Caballos de fuerza", y="Cantidad de carros",
       title = "Caballos de fuerza en carros seleccionados")+
  xlim(c(80,280))+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

  #Hist. orangeec
ggplot() + geom_histogram(data=orangeec,
                          aes(x=GDP.PC), fill="blue", color="red",
                          binwidth = 2000) +
  labs(x="PBI per capita", y="Cantidad de paises",
       title = "PBI per capita en LATAM")+
    theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

##

ggplot() + geom_histogram(data=orangeec,
                          aes(x=Creat.Ind...GDP), fill="green", color="red",
                          binwidth = 1) +
  labs(x="Aporte economia naranja al PBI(%)", y="Cantidad de paises",
       title = "Contribucion economia naranja al PBI en paises LATAM")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())


##

ggplot() + geom_histogram(data=orangeec,
                          aes(x=Internet.penetration...population), fill="blue", color="red",
                          binwidth = 5) +
  labs(x="Penetracion de internet (%) poblacion", y="Cantidad de paises",
       title = "Penetracion de internet en LATAM")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

## scale_x_continuous(breaks = seq(40, 100, 5))+..
  # 40 = Li , 100 = Lsup, 5 = ancho 

ggplot() + geom_histogram(data=orangeec,
                          aes(x=Internet.penetration...population), fill="green", color="red",
                          binwidth = 5) +
  labs(x="Penetracion de internet (%) poblacion", y="Cantidad de paises",
       title = "Penetracion de internet en LATAM")+
  scale_x_continuous(breaks = seq(40, 100, 5))+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

        ###CLASE 19 ####
boxplot(mtcars$hp,
        ylab= "caballos de fuerza",
        main= "caballos de fuerza en carros 'mtcars' ")

## con boxplot  se usa var. x = categorica(as.factor) y y= numerica  O viceversa
ggplot(mtcars, aes(x=as.factor(cyl), y=hp, fill=cyl))+
  geom_boxplot()+
  labs(x="cilindros", y="caballos de fuerza", 
       title = "Caballos de fuerza segun cilindros en mtcars")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

  # modificando el color de las cajas boxplot -> geom_boxplot(alpha=0.6)
    # cajas alargadas = datos más desviados del promedio , cajas chatas = datos homog cercanos a promedio

ggplot(mtcars, aes(x=as.factor(cyl), y=hp, fill=cyl))+
  geom_boxplot(alpha=0.6)+
  labs(x="cilindros", y="caballos de fuerza", 
       title = "Caballos de fuerza segun cilindros en mtcars")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

  #
ggplot(mtcars, aes(x=am, y=mpg, fill=am))+
  geom_boxplot()+
  labs(x="Tipo de caja", y="millas por galón",
       title="Millas por galón según tipo de caja 'mtcars'")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

  #para cambiar 'false' y 'true' de gráfico anterior /// c(): contenedor
?mtcars
mtcars$am <- factor(mtcars$am, levels = c(TRUE, FALSE),
                    labels = c("Manual", "Automatico"))

  #corremos otra vez el codigo para comprobar los cambios
ggplot(mtcars, aes(x=am, y=mpg, fill=am))+
  geom_boxplot()+
  labs(x="Tipo de caja", y="millas por galón",
       title="Millas por galón según tipo de caja 'mtcars'")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())


  ###### CLASE 20 #########
economy <- mean(orangeec$GDP.PC)
economy

library("dplyr")

# para "mutar" dataset (crear nueva variable dentro de dataset dado que en DS 
# todas son numericas y para boxplot necesitamos numericas y factor)
orangeec <- orangeec %>%
  mutate(Strong_economy = ifelse(GDP.PC < economy,
                                 "por debajo del promedio de PIB per capita",
                                 "Sobre-Arriba promedio de PIB per capita"))
#
ggplot(orangeec, aes(x=Strong_economy, y=Creat.Ind...GDP,
                     fill=Strong_economy))+
  geom_boxplot(alpha=0.4)+
  labs(x="Tipo de pais", y="Aporte economia naranja al PIB",
       title="Aporte economia naranja en PIB países LATAM con alto y bajo PIB
       per capita")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

#
ggplot(orangeec, aes(x=Strong_economy, y=Internet.penetration...population,
                     fill=Strong_economy))+
  geom_boxplot(alpha=0.4)+
  labs(x="Tipo de pais", y="Penetración de internet(%)",
       title="Penetracion de internet en países LATAM con alto y bajo PIB
       per capita")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())


          ##### CLASE 21 : EDA CON GRAFICAS DE DISPERSION MULTIVARIABLE #######

##SCATTERPLOT
library(ggplot2)

ggplot(mtcars, aes(hp,mpg))+
  geom_point()+
  labs(x="caballos fuerza", y="millas por galón",
       title="Relación caballos de fuerza y millas por galón")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

  #relación entre peso y ppotencia

ggplot(mtcars, aes(wt,hp))+
  geom_point()+
  labs(x="peso", y="potencia en hp",
       title="Relación peso / potencia")+
  theme(legend.position = "none") +
  theme(panel.background = element_blank(), 
        panel.grid.major = element_blank(),
        panel.grid.minor = element_blank())

  #relacionando 4 variables
    #color=am :para que color de burbujas esté según 'am'
    #size=cyl : para que tamaño sea según variable 'cyl'
ggplot(mtcars, aes(hp,qsec))+
  geom_point(aes(color=am, size=cyl))+
  labs(x="caballos de fuerza", y="tiempo en 1/4 de milla",
       title="caballos-velocidad según cilindra y tipo de caja")

## CLASE 22
  #scatterplot para economnaranja
    # ojo con 'color=factor()'
ggplot(orangeec, aes(Internet.penetration...population,Creat.Ind...GDP))+
  geom_point(aes(color=factor(Strong_economy), size=GDP.Growth..))+
  labs(x="Penetracion Internet", y="Aporte economia naranja al PIB",
       title="Internet y aporte economia naranja segun economia y 
       crecimiento PIB")

#############         TAREA         ##############
##############################
### hacer scatterplot con 4 variables x= inversion en EDUC como % de pib, 
#   y= desempleo, color = strong_economy, tamaño = % de poblacion por debajo de linea de pobreza

ggplot(orangeec, aes(Education.invest...GDP,Unemployment))+
  geom_point(aes(color=factor(Strong_economy), size=X..pop.below.poverty.line))+
  labs(x="Inversion en Educacion como % del PBI", y="Desempleo",
       title="Inversión en Educación (%PBI) y su relación con el Desempleo")

# tarea con reseña de 'plotly'

grafico_tarea  <-  ggplot(orangeec, aes(Education.invest...GDP,Unemployment, 
                                         label=row.names(orangeec)))+
                          geom_point(aes(color=factor(Strong_economy), size=X..pop.below.poverty.line))+
                          labs(x="Inversion en Educacion como % del PBI", y="Desempleo",
                               title="Inversión en Educación (%PBI) y su relación con el Desempleo")

grafico_tarea

o <- ggplotly(grafico_tarea)
o

######################################
####################################
ggplot(orangeec, aes(Education.invest...GDP,Creat.Ind...GDP))+
  geom_point(aes(color=factor(Strong_economy), size=X..pop.below.poverty.line))+
  labs(x="Inversion en Educacion como % del PBI", y="Aporte de la Econ Naranja al PBI",
       title="Inversión en Educación (%PBI) y su relación con el aporte de la
       economía Naranja")



#################################

  ### extra para plot interactivo donde se muestra info de cada punto en la gráfica
install.packages("plotly")
library(plotly)

grafico_interactivo <- ggplot(orangeec, aes(Internet.penetration...population,
                                            Creat.Ind...GDP, label=row.names(orangeec)))+
                      geom_point()+
                      labs(x="Penetracion de internet", y="aporte economia naranja",
                           title="Penetracion de Internet y aporte economia naranja")

grafico_interactivo

p = ggplotly(grafico_interactivo)
p

          ########### CLASE 23 ##########

# para analizar Correlaciones, se sugiere hacer pairs por partes para mejor visualizacion
pairs(mtcars[,2:6])

################################
cor(mtcars$cyl, mtcars$hp)
cor(orangeec$GDP.Growth.., orangeec$Creat.Ind...GDP, use = "complete.obs") ### no funciona acá na.rm = TRUE

###############################

library(dplyr)
#para seleccionar las columnas que queremos
newdata <- subset(mtcars, select = c(2,7:8,11,12))
pairs(newdata)

#para seleccionar las columnas que no queremos (nos debe dar el mismo resultado que la linea anterior)
pairs(mtcars[,-c(1,3,4,5,6,9,10)])

## Escogiendo observaciones con 'filter'
Eficientes <- filter(mtcars, mpg >= 30)
Eficientes

## relaciond e variables entre la seleccion de 'Eficientes'
pairs(Eficientes[,2:6])

## si queremos filtrar por modelos o marcas (tipo 'merc') en este ejemplo:
install.packages("stringr")
library(stringr)

merc <- mtcars %>%
  filter(str_detect(model,"Merc"))

merc

## relacion entre variables pero solo para 'mercs'
pairs(merc[,2:6])


          ######## CLASE 24: CORRELACIONES [0,1] ###########
cor(mtcars[,2:6])

cor(newdata)

cor(merc[,2:6])


      ##### CLASE 25-26 ####

#analizando EconomNaranja
pairs(orangeec[,2:6])

pairs(orangeec[,5:10])

newdata <- subset(orangeec,select=c(5,6,10,11,12,13))
newdata

pairs(newdata)

#analizando con 'cor'
cor(orangeec[,2:6])

  #cuando tenemos valores 'N.A' en el resultado usamos 'use':
cor(orangeec[,2:6],use="complete.obs")

cor(orangeec[,5:10],use="complete.obs")

cor(newdata, use="complete.obs")


      ##### CLASE 27 SD y CV####
summary(mtcars)

sd(mtcars$mpg)
desv <- sd(mtcars$mpg)

mean(mtcars$mpg)
prom <- mean(mtcars$mpg)
prom

CoefVar <- (desv/prom)*100
CoefVar

#######################



#######################

summary(orangeec)
sd(orangeec$Internet.penetration...population)
desv <- sd(orangeec$Internet.penetration...population)
desv

mean(orangeec$Internet.penetration...population)
prom <- mean(orangeec$Internet.penetration...population)
prom

CoefVar <- (desv/prom)*100
CoefVar

summary(orangeec)

### Removiendo NA's en orangeec con na.rm=TRUE (remove)
mean(orangeec$Creat.Ind...GDP, na.rm = TRUE)
prom <- mean(orangeec$Creat.Ind...GDP, na.rm = TRUE)


sd(orangeec$Creat.Ind...GDP, na.rm = TRUE)
desv <- sd(orangeec$Creat.Ind...GDP, na.rm = TRUE)

CoefVar <- (desv/prom)*100
CoefVar

          ######### CLASE 30 ########

#ajustando datos para mejorar visualizaciones
eficientes <- mean (mtcars$mpg)
eficientes

library(dplyr)
mtcars <- mtcars %>%
  mutate(Mas_eficientes=ifelse(mpg<eficientes,
                               "bajo promedio", "en o sobre proemdio"))

#la ',' es para que coja todas la sobservaciones
Mas_veloces <- mtcars[mtcars$qsec<16,]
Mas_veloces

mtcars <- mtcars %>%
  mutate(Velocidad_Cuarto_milla=ifelse(qsec<16,
                                       "Menos 16 segs",
                                       "Mas de 16 segs"))

#
mtcars <- mtcars %>%
  mutate(Peso_kilos=(wt/2)*1000)

mtcars <- mtcars %>%
  mutate(Peso=ifelse(Peso_kilos<=1500,
                     "livianos", "pesados"))

#
orangeec <- orangeec %>%
  mutate(Crecimiento_GDP = ifelse(GDP.Growth.. >= 2.5,
                                  "2.5% o más","Menos 2.5%"))

#
orangeec <- orangeec %>%
  mutate(Anaranjados = ifelse(Creat.Ind...GDP>=2.5,
                              "Más anaranjados", "Menos anaranjados"))

#ranking segun PBI
orangeec %>%
  arrange(desc(Creat.Ind...GDP))

# '%>%' : "que se va a"  /// %in% : nos va a buscar todo lo que tenga ciertas etiquetas, lo que se encuentre en:
TopNaranjas <- orangeec %>%
  filter(Country %in% c("Mexico", "Panama", "Argentina", "Colombia", "Brazil"))

TopNaranjas

#mejorando visualizacion
TopNaranjas %>%
  arrange(desc(Creat.Ind...GDP))


        ######### CLASE 32 - 33############

mtcars %>%
  arrange(desc(Peso_kilos))

# 'select' para columna, 'filter' para fila // %in% : "en donde se encuentre"
Mas_pesados <- mtcars %>%
  filter(model %in% c("Lincoln Continental", "Chrysler Imperial", "Cadillac Fleetwood", "Merc 450SE"))

Mas_pesados

library(ggplot2)
#facet_wrap (para mostrar un cuadrante para cada modelo de 'mas_pesados')
ggplot(Mas_pesados, aes(x=hp, y=mpg))+
  geom_point()+
  facet_wrap(~model)

ggplot(mtcars, aes(x=cyl, y=mpg, size=Peso))+
  geom_point()+
  facet_wrap(~ am)

ggplot(mtcars, aes(x=cyl, y=mpg, size=Peso_kilos))+
  geom_point()+
  facet_wrap(~ am)

##

TopNaranjas <- orangeec %>%
  filter(Country %in% c("Mexico", "Panama", "Argentina", "Colombia", "Brazil", "Paraguay"))

TopNaranjas

#
ggplot(TopNaranjas, aes(x=Internet.penetration...population, 
                        y=Services...GDP, size=GDP.PC))+
  geom_point()+
  facet_wrap(~Country)

ggplot(TopNaranjas, aes(x=Education.invest...GDP, 
                        y=Creat.Ind...GDP, size=Unemployment))+
  geom_point()+
  facet_wrap(~Country)

###############################
ggplot(TopNaranjas, aes(x=Internet.penetration...population, 
                        y=Services...GDP, size=GDP.PC))+
  geom_point()+
  facet_wrap(~Crecimiento_GDP)
###############################

##(agregando color a la visualizacion)
install.packages("RColorBrewer")
library(RColorBrewer)

#
myColors <- brewer.pal(9,"Reds")

ggplot(TopNaranjas, aes(x=Internet.penetration...population,
                        y=GDP.PC, fill=Creat.Ind...GDP))+
  geom_tile()+
  facet_wrap(~Country)+
  scale_fill_gradientn(colors = myColors)

      ##### CLASE 34 #####
install.packages("rmarkdown")
library(rmarkdown)
install.packages("knitr")
library(knitr)
# alt + 96 = `

    ####### CIERRE #####
cajas <- c(1,2,3,4,5,6,7,8)
tiempo <- c(10,9,8,5.8,6,3,1.8,1)
plot(tiempo~cajas)

#para numéricos:
plot(orangeec$Services...GDP~orangeec$Education.invest...GDP)
#para numéricos vs categoricas:
plot(mtcars$mpg~mtcars$am)

#R automaticamente detecta si es boxplot o dispersion según tipo de datos

## revisar :
# escribir funciones
# limpiar Datasets
# importar y leer datasets
# correalcion y regresion lineal
# visualizacion grafica tipo mapas de calor
# dashboards o tableros de control interactivos con Shiny
