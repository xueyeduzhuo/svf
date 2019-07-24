gg
# Structural Variation Filter

---

![alt text](./figure/framework.png  "Structural Variation Filter Framework")

---

## User Guide

---

### Configuration

```
# download svf files  
$ wget https://github.com/xueyeduzhuo/svf/archive/master.zip

# decompress it on your server
$ unzip svf-master.zip

# rename it as svf
$ mv svf-master svf

```

### Run svf

```
$ cd svf

$ ./svf.sh
or
$ python svf.py feature -b <*.bam> -c <*.vcf.gz>  -v <*.vcf.gz> -o <*_feature.txt> -g hg19 -f <*.fa>

```

### Input

svf requires aligned files(.bam format), SV files(.vcf.gz format or .bed format) , SNV files(.vcf.gz format).

```
$ python svf.py pipeline -b <*.bam> -c <*.vcf.gz> -v <*.vcf.gz ...> -o <*.txt> -g hg19 -f <*.fa> 
```



### Output
 
 Output is generated in the current working directory by default.

```
$ svf ... -o <*.txt>
``` 
 


---


## Requirements
* python 2.7
  * numpy
  * pybedtools
  * pysam 0.9+
  * scikit-learn v0.19+
  * multiprocessing
  * vcf
  

* bedtools 2.25.0 or later

---

## Contact
xlwu@hit.edu.cn
