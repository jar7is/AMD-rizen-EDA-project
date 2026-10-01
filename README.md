# AMD Datacenter GPU Performance - Exploratory Data Analysis (EDA) Project

A comprehensive data analysis project exploring AMD's datacenter GPU evolution from 2014 to 2024.

---

## 📊 Project Overview

This project performs a detailed exploratory data analysis on **8 AMD datacenter GPU models** spanning **10 years**, examining **29 performance and hardware features**. Perfect for **GitHub portfolio** and demonstrates professional EDA skills.

### Dataset Characteristics
- **Rows:** 8 GPU models (FirePro S9150 → Instinct MI325X)
- **Columns:** 29 features (hardware specs, performance metrics, cost/efficiency)
- **Time Period:** 2014-2024
- **Data Quality:** 100% complete (zero missing values, no duplicates)

---

## 🎯 Analysis Questions Answered

### 1. **Performance Evolution (2014-2024)**
- How have FP32, FP16, FP64 TFLOPS evolved?
- **Finding:** 32x improvement in FP32 TFLOPS, 259x in FP16

### 2. **Hardware Scaling**
- How have transistor count and process nodes improved?
- **Finding:** Process shrunk from 28nm to 5nm, transistor density increased 10.6x

### 3. **Memory Architecture Impact**
- How does memory bandwidth correlate with performance?
- **Finding:** Strong correlation (0.944) between bandwidth and FP32 performance

### 4. **Power Efficiency**
- How efficient are modern GPUs per watt?
- **Finding:** 10.3x improvement in GFLOPS/Watt over 10 years

### 5. **Cost-Performance Value**
- Which GPUs offer the best value?
- **Finding:** Value improved 5.1x despite 7.9x price increase

### 6. **Architecture Comparison (GCN vs CDNA)**
- How did architecture generations improve?
- **Finding:** CDNA averages 16x higher FP32 performance than GCN

---

## 📁 Project Files

```
AMD_GPU_EDA_Project/
├── AMD_GPU_EDA_Project.ipynb           # Main Jupyter notebook
├── amd_datacenter_gpu_performance.csv  # Dataset
├── README.md                            # This file
└── requirements.txt                     # Python dependencies
```

---

## 🚀 Quick Start

### Prerequisites
- Python 3.7+
- Jupyter Notebook or VS Code with Jupyter extension

### Installation

```bash
# Clone or download the project
cd AMD_GPU_EDA_Project

# Install dependencies
pip install -r requirements.txt

# Open Jupyter notebook
jupyter notebook AMD_GPU_EDA_Project.ipynb
```

### Running in VS Code
1. Install "Jupyter" extension in VS Code
2. Open `AMD_GPU_EDA_Project.ipynb`
3. Click "Run All" or run cells individually

---

## 📦 Dependencies

```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
```

Install all at once:
```bash
pip install pandas numpy matplotlib seaborn
```

---

## 📈 Visualizations Generated

The notebook creates **7 comprehensive visualization sets**:

### 1. Performance Evolution (4 charts)
- FP32, FP16, FP64 trends over time
- All precision types comparison
- **Why:** Track performance scaling across 10 years

### 2. Hardware Evolution (2 charts)
- Process node miniaturization
- Transistor density growth
- **Why:** Demonstrates Moore's Law adherence

### 3. Memory Analysis (4 charts)
- Memory bandwidth vs performance
- Memory size evolution by type
- Bus width vs bandwidth correlation
- Correlation matrix (memory vs performance)
- **Why:** Understand memory bottlenecks

### 4. Power Efficiency (4 charts)
- TDP vs performance scatter plot
- FP32 efficiency (GFLOPS/Watt) comparison
- FP32 vs FP16 efficiency
- Power & efficiency trends
- **Why:** Compare energy efficiency improvements

### 5. Value Analysis (4 charts)
- Price vs performance scatter plot
- Value metric (GFLOPS/Dollar)
- Price evolution trends
- Cost per watt ratio
- **Why:** Assess cost-effectiveness

### 6. Architecture Comparison (4 charts)
- FP32 performance by model
- Matrix cores impact on FP16
- GCN vs CDNA average metrics
- Compute architecture scaling
- **Why:** Compare hardware generations

### 7. Metrics Dashboard (1 heatmap)
- Normalized scores (0-100) for all metrics
- Quick overview of GPU capabilities
- **Why:** Comprehensive single-view summary

---

## 🔍 Key Findings

### Performance Growth
```
FP32:  5.07 → 163.4 TFLOPS   (32.2x growth)
FP16:  5.07 → 1,307 TFLOPS   (257.8x growth)
FP64:  0.77 → 81.7 TFLOPS    (106.2x growth)
```

### Hardware Evolution
```
Process: 28nm → 5nm          (5.6x smaller)
Transistors: 6.2B → 153B     (24.7x more)
Density: 14.16 → 150.44 M/mm² (10.6x)
```

### Memory Improvements
```
Size: 16GB → 256GB           (16x larger)
Bandwidth: 320 → 6,000 GB/s  (18.75x faster)
```

### Efficiency Gains
```
FP32 GFLOPS/W: 1.54 → 222.91 (144.7x better!)
TDP: 235W → 1,000W           (4.3x higher)
Performance grew 32x, power only 4.3x ✨
```

### Value Evolution
```
Price: $3,299 → $26,000      (7.9x more expensive)
GFLOPS/$: 1.54 → 7.78        (5.1x better value!)
```

### Architecture Impact (GCN vs CDNA)
```
GCN Avg FP32:    11.88 TFLOPS
CDNA Avg FP32:   193.04 TFLOPS
Improvement:     16.2x performance leap
```

---

## 📊 Data Dictionary

### Performance Metrics
| Column | Type | Range | Description |
|--------|------|-------|-------------|
| `fp64_tflops` | Float | 0.77-81.7 | Double precision floating point operations |
| `fp32_tflops` | Float | 5.07-163.4 | Single precision (main metric) |
| `fp16_tflops` | Float | 5.07-1,307 | Half precision (AI/ML optimized) |
| `fp8_tflops` | Float | 5.07-2,614 | 8-bit precision (extreme speedup) |

### Hardware Specs
| Column | Type | Range | Description |
|--------|------|-------|-------------|
| `process_node_nm` | Int | 5-28 | Manufacturing process (nm) |
| `transistor_count_millions` | Float | 6,200-153,000 | Total transistors |
| `compute_units` | Int | 44-304 | Parallel compute cores |
| `memory_size_gb` | Float | 16-256 | VRAM capacity |
| `memory_bandwidth_gbs` | Float | 320-6,000 | Memory throughput |

### Efficiency Metrics
| Column | Type | Range | Description |
|--------|------|-------|-------------|
| `fp32_gflops_per_watt` | Float | 21.57-222.91 | Energy efficiency |
| `fp32_gflops_per_dollar` | Float | 1.54-7.78 | Value proposition |
| `tdp_watts` | Float | 235-1,000 | Power consumption |
| `launch_price_usd` | Float | $3,299-$26,000 | MSRP |

---

## 💡 Code Quality Features

✅ **Professional Standards:**
- Clean, readable code with comments
- Organized into logical sections
- Proper function documentation
- No hardcoded values (all parameterized)
- Beginner-friendly explanations

✅ **Best Practices:**
- Proper imports and configuration
- Error handling where needed
- Normalized visualization scales
- Consistent color schemes
- High-resolution outputs (300 DPI)

✅ **Portfolio-Ready:**
- Well-documented findings
- Insights without premature conclusions
- Proper correlation vs causation caveats
- Reproducible results
- GitHub-friendly structure

---

## 🎓 Learning Outcomes

By exploring this project, you'll learn:

1. **Data Exploration:** Loading, inspecting, and validating datasets
2. **Pandas Mastery:** Data manipulation, filtering, aggregation
3. **NumPy Skills:** Numerical operations and normalization
4. **Visualization:** Creating publication-quality charts with Matplotlib & Seaborn
5. **Analysis:** Deriving insights from data relationships
6. **Domain Knowledge:** Understanding GPU hardware and performance metrics
7. **Statistics:** Correlation analysis and metric interpretation
8. **Communication:** Presenting findings clearly to non-technical audiences

---

## 🔗 GitHub Portfolio Integration

To make this portfolio-ready:

1. **Initialize Git Repository**
   ```bash
   git init
   git add .
   git commit -m "AMD GPU EDA - Comprehensive analysis project"
   ```

2. **Create `.gitignore`**
   ```
   __pycache__/
   .ipynb_checkpoints/
   *.pyc
   .DS_Store
   ```

3. **Create `requirements.txt`**
   ```bash
   pip freeze > requirements.txt
   ```

4. **Push to GitHub**
   ```bash
   git remote add origin https://github.com/username/amd-gpu-eda
   git push -u origin main
   ```

5. **Add Badge to README**
   ```markdown
   ![Python](https://img.shields.io/badge/Python-3.7+-blue)
   ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
   ```

---

## ⚠️ Important Notes

### Correlation vs Causation
- Strong correlations exist (e.g., smaller process → higher density)
- **BUT** this doesn't mean smaller process *causes* better performance
- Multiple confounding factors: architecture design, memory hierarchy, clock speeds
- Always analyze context before drawing conclusions

### Data Limitations
- Only 8 GPU models (small dataset)
- No gaming GPUs (datacenter only)
- No AMD's older Radeon cards
- Prices are launch MSRPs (actual prices vary)
- Performance is theoretical (real-world varies by workload)

### Recommendations for Expansion
- Add more GPU models for statistical significance
- Include competitor GPUs (NVIDIA, Intel)
- Add real-world benchmark scores
- Temporal analysis (market availability)
- Application-specific benchmarks

---

## 📚 Resources & References

### GPU Architecture Docs
- [AMD CDNA Architecture](https://www.amd.com/en/products/specifications/accelerators)
- [AMD GCN Architecture](https://en.wikipedia.org/wiki/Graphics_Core_Next)

### Data Analysis
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Matplotlib Gallery](https://matplotlib.org/stable/gallery/index.html)
- [Seaborn Documentation](https://seaborn.pydata.org/)

### Best Practices
- [Jupyter Best Practices](https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/)
- [Python PEP 8 Style Guide](https://pep8.org/)

---

## 🤝 Contributing

To extend this analysis:

1. Add new visualizations
2. Explore additional correlations
3. Create interactive dashboards (Plotly)
4. Add machine learning predictions
5. Compare with competitor GPUs

---

## 📄 License

This project is open-source and available for educational and portfolio purposes.

---

## ✨ Author Notes

This EDA project demonstrates:
- ✅ Data exploration best practices
- ✅ Professional visualization techniques
- ✅ Statistical analysis skills
- ✅ Clear communication of findings
- ✅ Portfolio-quality code
- ✅ Domain knowledge synthesis

**Perfect for**: Data science portfolios, interviews, academic projects, or industry presentations.

---

## 🚀 Next Steps

1. **Run the notebook** and explore the visualizations
2. **Modify queries** to answer your own questions
3. **Add more data** to expand the analysis
4. **Create a blog post** explaining the findings
5. **Share on GitHub** to showcase your skills

---

## 📞 Questions?

Refer to the comments in the Jupyter notebook for detailed explanations of each code section.

---

**Last Updated:** October 1, 2026  
**Dataset:** AMD Datacenter GPU Performance (2014-2024)  
**Analysis Type:** Exploratory Data Analysis (EDA)  
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn
