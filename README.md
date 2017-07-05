	#written by peteskene@gmail.com
    #script takes a list of bed files, randomly subsets each bed file and generates bedgraphs and big wigs
    #on each subsetted bed file
    
    #naming  convention:
        #supplied bed: *.bed
    #generated names using default suffix (please note will overwrite existing files, so can change suffix if required:
        #subsetted bed: *_subset.bed (file is saved for future use to avoid subtle differences from random sampling)
        #subsetted bedgraph: *_subset.bg
        #subsetted bigwig: *_subset.bw
        
    #will print to screen a table of read number per bed file
    #will exit if one the input bed files has less than the specified read number (check is made before subsetting, so no files saved)
        
    #Parameters:
    #___________
    #bed_files: list of bed files as strings (can include path) e.g. ['A.bed', 'B.bed', 'C.bed']
    #read_number: number of reads to randomly subset; default to 10 million
    #species: used by bedtools in genomvecov tool; provided as a string (e.g. 'hg19')
    #subset_filename_suffix: suffix as a string for subsetted bed, bedgraph and bigwig files; eg. include read number 'subset_10M'
