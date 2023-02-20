# Source: Analysis of Phylogenetics and Evolution with R: https://link.springer.com/book/10.1007/978-1-4614-1743-9

packages used for evolutionary analyses

    Name          Title
    ade4          Analysis of environmental data
    adegenet      Spatial and multivariate population genetics
    adephylo      Phylogenetic comparative methods
    ape           Analyses of phylogenetics and evolution
    apTreeshape   Analyses of phylogenetic tree shape 
    BoSSA         Sequence retrieval 
    distory       Distances among trees 
    diversitree   Tests of diversification 
    geiger        Evolutionary diversification 
    LAGOPUS       Bayesian molecular dating 
    laser         Speciation and extinction estimation 
    pegas         Population genetics 
    phangorn      Phylogeny estimation 
    phyclust      Phylogenetic clustering and coalescence 
    phylobase     Phylogenetic structures and comparative data 
    phyloch       Tools for phylogenetics and taxonomy 
    phyloclim     Phylogenetic climatic niche modeling 
    picante       Phylogenies and community ecology 
    seqinr        Exploratory analyses of molecular sequences 
    spacodiR      Phylogenetic community structure 
    TreeSim       Tree simulations
update.packages()    
mode(x)
Configurations

    > setwd("/home/paradis/phylo/data") # Linux
    > setwd("D:/data/phylo/data") # Windows
The Data Structures 

    Vector, Factor, Matrix, Data Frame, List
Creating Graphics

    postscript("plot.eps")
    dev.off()
Repeating Commands
    
    Loops
        for (x in y) <command>
    Apply-Like Functions
        apply(X, MARGIN, FUN, ...)
        lapply(x, FUN, ...)
        tapply(X, INDEX, FUN = NULL, ...)
        by(data, INDICES, FUN, ..., simplify = TRUE)
        replicate
Phylogenetic Data in R

    setwd("/home/paradis/phylo")
    tr <- read.tree("data/treeb1.txt")
    mean(tr$edge.length)
    summary(tr$edge.length)
    hist(tr$edge.length)
    x <- tr$edge.length
Reading Phylogenetic Data

    tr <- read.tree("treefile.tre")
    trx <- read.nexus("treefile.nex")
Molecular Sequences

    choosebank()

    s <- choosebank("genbank")
    query("rampho", "sp=Ramphocelus@")
    rampho
    rampho$req[[1]]
    
    y <- read.GenBank("AF310048")
    attr(y, "species")
    identical(x[[1]], as.character(y[[1]]))
    bdna <- read.PDB("bdna.pdb")
  	names(bdna)
    
    library(rgl)
    points3d(bdna$atom$X, bdna$atom$Y, bdna$atom$Z)
Allelic Data    
 
 page 42
    
    
    
    
    
    
    
    
    



    
