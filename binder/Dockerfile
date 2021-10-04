FROM r-base
COPY . /usr/local/src/myscripts
WORKDIR /usr/local/src/myscripts
CMD ["Rscript", "myscript.R"]

RUN apt-get update ; apt-get install ca-certificates \
    && apt-get update \
    && apt-get install -y

RUN R -e "install.packages('ggplot2',dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "install.packages('ggpubr',dependencies=TRUE, repos='http://cran.rstudio.com/')"
