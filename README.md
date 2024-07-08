# CellRanger  
## make genome reference  
CellRanger 官网上有人和鼠的信息，可以直接下载  
自己创建需要准备genome.fa 与 genome.gtf  
*注意将两个文件转换成utf-8格式或兼容格式 在windows下默认终止符为"CRLF" 需转换成"LF"  
`file genome.fa` `file genome.gtf`  查看文件的格式类型  
`iconv -f ISO-8859-1 -t UTF-8 genome.fa | sed 's/\r$//' > genome_utf8.fa`  
`sed 's/\r$//' genome.gtf > genome_lf.gtf`  
`sh mkgenome.sh`  
