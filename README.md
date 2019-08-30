# somatic_pipeline
Tumor somatic mutation detection process (tissue, repeated DNA, need to have a control)
<pre>
-------------------------------------------------- --------
        {somatic cell mutation detection process}
Features:
1) Accurate, efficient and fast using the sentieon TNscope process
2) Associate cosmic, www.cancergenomeinterpreter.org target drug database
3) Analysis of SV, common fusion genes at a glance
4) Analyze CNV, detect copy number variation


Input: fastq

Output: somatic_mut.xlsx/tsv, SV, CNV, QC metrics...

Instructions:
        Perl /gpfs/users/yanghao/project/somatic_pipeline/somatic.sentieon.fq.pipeline.pl -t <tumor name> -t1 <tumor R1> -t2 <tumor R2> -n <normal name> -n1 <normal R1 > -n2 <normal R2> -b <interval.bed>

By default, it is submitted to the cn-medium partition. If there is no resource, you can specify the job to submit to cn-fast as follows:
        Perl /gpfs/users/yanghao/project/somatic_pipeline/somatic.sentieon.fq.pipeline.pl -t <tumor name> -t1 <tumor R1> -t2 <tumor R2> -n <normal name> -n1 <normal R1 > -n2 <normal R2> -b <interval.bed> -part cn-fast

If you want to do a trimming of the fastq file before the comparison, you can do this:
        Perl /gpfs/users/yanghao/project/somatic_pipeline/somatic.sentieon.fq.pipeline.pl -t <tumor name> -t1 <tumor R1> -t2 <tumor R2> -n <normal name> -n1 <normal R1 > -n2 <normal R2> -b <interval.bed> -trim 1

Last Updated:2017/12/29

Change Log
2017/12/29
Support trim (optional, as long as -trim 1, will trim)
Fixed some perl environment variables, and mosdepth issues

If any problems occur during use, please contact yanghao@eulertechnology.com

-------------------------------------------------- -------
</pre>
