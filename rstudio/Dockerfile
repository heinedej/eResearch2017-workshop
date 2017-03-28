FROM rocker/rstudio
MAINTAINER Heine de Jager <heinedej@gmail.com>

RUN apt-get update && apt-get install -y --no-install-recommends curl openjdk-7-jdk openjdk-7-jre libpcre3-dev \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/

RUN curl https://nhorton.people.amherst.edu/r2/examples/install.R -ko /home/rstudio/1.install.R && \
  curl https://nhorton.people.amherst.edu/r2/examples/datamgmt.R -ko /home/rstudio/2.datamgmt.R && \
  curl https://nhorton.people.amherst.edu/r2/examples/functions.R -ko /home/rstudio/3.functions.R && \
  curl https://nhorton.people.amherst.edu/r2/examples/common.R -ko /home/rstudio/5.common.R && \
  curl https://nhorton.people.amherst.edu/r2/examples/regression.R -ko /home/rstudio/6.regression.R &&  \
  curl https://nhorton.people.amherst.edu/r2/examples/morereg.R -ko /home/rstudio/7.morereg.R && \
  curl https://nhorton.people.amherst.edu/r2/examples/graphics1.R -ko /home/rstudio/8.graphics1.R  && \
  curl https://nhorton.people.amherst.edu/r2/examples/simulation.R -ko /home/rstudio/10.simulation.R  && \
  curl https://nhorton.people.amherst.edu/r2/examples/special.R -ko /home/rstudio/11.special.R  && \
  curl https://nhorton.people.amherst.edu/r2/examples/advanced.R -ko /home/rstudio/12.advanced.R

RUN echo "r <- getOption('repos'); r['CRAN'] <- 'http://cran.us.r-project.org'; options(repos = r);" > ~/.Rprofile

RUN install2.r --error biglm boot chron GGally GenKern Hmisc Hotelling MASS MCMCpack Matching Matrix MplusAutomation QuantPsyc \
  ROCR RSQLite VGAM WriteXLS Zelig car circular coda coefplot coin devtools dispmod doBy dplyr ellipse elrm \
  epitools exactRankTests factorplot flexmix foreach foreign gam gdata gee ggplot2 ggvis gmodels gridExtra greport gtools \
  hexbin httr hwriter irr knitr lars lattice lawstat lme4 lmtest lpSolve lubridate magrittr maps markdown memisc \
  mice mitools mix moments mosaic muhaz multcomp multilevel nlme nnet nortest packrat partykit plotrix poLCA prettyR pscl pwr quantreg randomLCA reshape \
  rms rpart rtf sas7bdat scatterplot3d sciplot shiny simPH sqldf survey survival swirl tidyr tm tmvtnorm vcd vioplot xtable

