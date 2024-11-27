This is a ducument to help me transmit text to vitural computer :)
# 1. 首先安装BiocManager
conda activate r_env
R
# 在R中执行：
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install(version = "3.18")

# 2. 差异表达分析包
conda install -c bioconda \
    bioconductor-deseq2 \     # RNA-seq差异表达分析
    bioconductor-edger \      # RNA-seq差异表达分析
    bioconductor-limma \      # 芯片和RNA-seq分析
    bioconductor-deg \        # 差异表达基因分析
    r-pcamethods              # 主成分分析

# 3. 数据可视化包
conda install -c conda-forge \
    r-pheatmap \             # 热图绘制
    r-complexheatmap \       # 复杂热图绘制
    r-enhancedvolcano \      # 火山图绘制
    r-ggrepel \              # 标签优化
    r-ggtree                 # 进化树可视化

# 4. 富集分析和通路分析
conda install -c bioconda \
    bioconductor-clusterprofiler \ # 功能富集分析
    bioconductor-dose \            # 疾病本体注释
    bioconductor-pathview \        # KEGG通路可视化
    bioconductor-fgsea \          # 基因集富集分析
    bioconductor-reactomepa       # Reactome通路分析

# 5. 单细胞分析包
conda install -c bioconda \
    bioconductor-seurat \         # 单细胞RNA分析
    bioconductor-scater \         # 单细胞数据分析
    bioconductor-monocle3 \       # 轨迹分析
    bioconductor-singlecellexperiment # 单细胞数据结构

# 6. 微生物组分析包
conda install -c bioconda \
    bioconductor-phyloseq \       # 微生物组分析
    r-vegan \                     # 生态学分析
    r-microbiome                  # 微生物组分析

# 7. 序列分析包
conda install -c bioconda \
    bioconductor-biostrings \     # 生物序列处理
    bioconductor-genomicranges \  # 基因组区间操作
    bioconductor-ggtranscript     # 转录本可视化

# 8. 基因组注释包
conda install -c bioconda \
    bioconductor-annotationdbi \  # 基因注释
    bioconductor-org.hs.eg.db \   # 人类基因注释
    bioconductor-org.mm.eg.db     # 小鼠基因注释
