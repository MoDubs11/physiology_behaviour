FROM rocker/binder:3.6.0
LABEL maintainer='maureen_williams'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
RUN wget https://github.com/MoDubs11/physiology_behaviour/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-11-12/')); devtools::install_deps()"
