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