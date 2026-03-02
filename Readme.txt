Please unzip all the files first.

1. CosMx data:
The data/ folder.

2. Marker gene lists:
Final_gene_marker_general.xlsx: for general cell types
Final_gene_marker_immune2.xlsx: for immune related cell types

3. General analysis for cell clustering, cell type annotation, and distance/neighborhood analysis
Code: under the code/general folder. Note that we renamed all patients. Please refer to the analysis/Patient Renumbering.txt for more details.
Results: the output/ folder and allPatients_final.pptx.

4. Figures and analysis:
(1) Figure 1C: analysis/XX cell types.xlsx; code/plot/cellType

(2) Figure 2A: code/java/Step_01_Replace.java -> generate cell clustering file with cell ID and cluster name
code/java/Step_02_GeneralDistance.java ->  generate a matrix of average distances of among all cell types
code/distance/allPatients_heatmap_distance.R

(3) Figure 2B: code/java/Step_01_Replace.java -> generate cell clustering file with cell ID and cluster name
code/java/Step_05_fibro_kera_distance.java -> find fibroblasts that are close to and far from basal keratinocytes (distance threshold = 150)
code/addtionalDistanceAnalysis/P*_dis_fibro_bk.R and code/addtionalDistanceAnalysis/P*_dis_fibro_bk_gene.R

(4) Figure 2C: code/COLgeneExpression/, code/CXCLgeneExpression/, code/plot/COLgeneExpression.prism, and code/plot/CXCgeneExpression

(5) Figure 2D: code/java/Step_01_Replace_allLesion.java, code/fibroAnalysis/AllLesion_fibro.R

(6) Figure 2E: Donut plots -> code/java/Step_01_cellSeparationAllLesion.java, code/plot/allLesion_ring

======================Session Info=======================:

R version 4.3.1 (2023-06-16)
Platform: x86_64-apple-darwin20 (64-bit)
Running under: macOS Sonoma 14.5

Matrix products: default
BLAS:   /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vecLib.framework/Versions/A/libBLAS.dylib 
LAPACK: /Library/Frameworks/R.framework/Versions/4.3-x86_64/Resources/lib/libRlapack.dylib;  LAPACK version 3.11.0

locale:
[1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8

time zone: Australia/Melbourne
tzcode source: internal

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] viridis_0.6.5      viridisLite_0.4.2  HGNChelper_0.8.14  lubridate_1.9.3    forcats_1.0.0      stringr_1.5.1      dplyr_1.1.4        purrr_1.0.2        readr_2.1.5        tidyr_1.3.1        tibble_3.2.1       ggplot2_3.5.1      tidyverse_2.0.0   
[14] Seurat_5.0.3       SeuratObject_5.0.2 sp_2.1-4          

loaded via a namespace (and not attached):
  [1] RColorBrewer_1.1-3          rstudioapi_0.16.0           jsonlite_1.8.8              magrittr_2.0.3              ggbeeswarm_0.7.2            spatstat.utils_3.1-2        farver_2.1.2                ragg_1.3.2                  zlibbioc_1.46.0            
 [10] vctrs_0.6.5                 ROCR_1.0-11                 DelayedMatrixStats_1.22.6   spatstat.explore_3.2-7      RCurl_1.98-1.16             S4Arrays_1.0.6              htmltools_0.5.8.1           sctransform_0.4.1           parallelly_1.37.1          
 [19] KernSmooth_2.23-24          htmlwidgets_1.6.4           ica_1.0-3                   plyr_1.8.9                  plotly_4.10.4               zoo_1.8-12                  igraph_2.0.3                mime_0.12                   lifecycle_1.0.4            
 [28] pkgconfig_2.0.3             Matrix_1.6-4                R6_2.5.1                    fastmap_1.2.0               GenomeInfoDbData_1.2.10     MatrixGenerics_1.12.3       fitdistrplus_1.1-11         future_1.33.2               shiny_1.8.1.1              
 [37] digest_0.6.35               colorspace_2.1-0            patchwork_1.3.1             S4Vectors_0.40.2            tensor_1.5                  RSpectra_0.16-1             irlba_2.3.5.1               textshaping_0.4.0           GenomicRanges_1.52.1       
 [46] labeling_0.4.3              progressr_0.14.0            fansi_1.0.6                 spatstat.sparse_3.0-3       timechange_0.3.0            httr_1.4.7                  polyclip_1.10-6             abind_1.4-8                 compiler_4.3.1             
 [55] withr_3.0.0                 fastDummies_1.7.3           MASS_7.3-60                 DelayedArray_0.26.7         tools_4.3.1                 splitstackshape_1.4.8       vipor_0.4.7                 lmtest_0.9-40               beeswarm_0.4.0             
 [64] zip_2.3.1                   httpuv_1.6.15               future.apply_1.11.2         goftest_1.2-3               glmGamPoi_1.12.2            glue_1.7.0                  nlme_3.1-164                promises_1.3.0              grid_4.3.1                 
 [73] Rtsne_0.17                  cluster_2.1.6               reshape2_1.4.4              generics_0.1.3              gtable_0.3.6                spatstat.data_3.0-4         tzdb_0.4.0                  data.table_1.16.0           hms_1.1.3                  
 [82] XVector_0.40.0              utf8_1.2.4                  BiocGenerics_0.48.1         spatstat.geom_3.2-9         RcppAnnoy_0.0.22            ggrepel_0.9.6               RANN_2.6.1                  pillar_1.9.0                limma_3.56.2               
 [91] spam_2.10-0                 RcppHNSW_0.6.0              later_1.3.2                 splines_4.3.1               lattice_0.22-6              survival_3.6-4              deldir_2.0-4                tidyselect_1.2.1            miniUI_0.1.1.1             
[100] pbapply_1.7-2               gridExtra_2.3               IRanges_2.36.0              SummarizedExperiment_1.30.2 scattermore_1.2             stats4_4.3.1                Biobase_2.60.0              matrixStats_1.4.1           stringi_1.8.4              
[109] lazyeval_0.2.2              codetools_0.2-20            cli_3.6.2                   uwot_0.2.2                  systemfonts_1.1.0           xtable_1.8-4                reticulate_1.37.0           munsell_0.5.1               GenomeInfoDb_1.36.4        
[118] Rcpp_1.0.13                 globals_0.16.3              spatstat.random_3.2-3       png_0.1-8                   ggrastr_1.0.2               parallel_4.3.1              presto_1.0.0                dotCall64_1.1-1             sparseMatrixStats_1.12.2   
[127] bitops_1.0-8                listenv_0.9.1               scales_1.3.0                ggridges_0.5.6              openxlsx_4.2.5.2            crayon_1.5.3                leiden_0.4.3.1              rlang_1.1.3                 cowplot_1.1.3             
