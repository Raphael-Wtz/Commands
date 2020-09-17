# Commands

**Go to the directory where the key is**<br/>
cd C:\Users\Raphael\Desktop\College et Pro\sbu\BIO 312<br/>
(May not be needed due to perm conflicts, the key was moved to the root directory of the cmd)<br/>

**Connect to the instance**<br/>
ssh -i 312Key.pem ec2-user@54.235.102.113<br/>            
(fine with disclosing my IP address here but normally try not to)<br/>

**List directory content**<br/>
ls<br/>

**Go to a directory**<br/>
cd ~/*DIRECTORY*<br/>

**Go up a directory**<br/>
cd ../<br/>

**Go to root directory**<br/>
cd<br/>

**See directories within a directory**<br/>
ls -d */<br/>

**Which directory am I in**<br/>
pwd<br/>

**Turn on web server**<br/>
sudo service httpd start<br/>

**ncbi app download help**<br/>
ncbi-acc-download -h<br/>

**Look at a downloaded file**<br/>
less *filename*<br/>

(spacebar down, P up, Q quit)<br/>

**Download a FASTA file**<br/>
ncbi-acc-download -F fasta *scaffoldname*<br/>

**Download a GFF3 file**<br/>
ncbi-acc-download -F gff3 *scaffoldname*<br/>

**Open grep manual**<br/>
man grep<br/>

**Example cmd to use grep**<br/>
grep LOC5513668 NW_001834348.1.gff > LOC5513668.gff<br/>

(If you leave off '> file', the result will be printed to your screen the '>' sign redirects this to a file)<br/>

**To only include lines with word exon**<br/>
grep exon LOC5513668.gff > LOC5513668.mrna.gff<br/>

**Exclude an isoform (example)**<br/>
grep -v X2 LOC5513668.gff > LOC5513668.notX2.gff<br/>
**Exclude another isoform (ex)**<br/>
grep -v X3 LOC5513668.notX2.gff > LOC5513668.X1.gff<br/>

**Sort a gff file and name the ouput (example)**<br/>
gt gff3 -sort  -tidy -force -o LOC5513668.sorted.gff LOC5513668.X1.gff<br/>

**Lengths of exons introns and name output (ex)**
gt stat -genelengthdistri -exonlengthdistri -intronlengthd<br/>istri -cdslengthdistri -addintrons -force  -o LOC5513668.sorted.counts.gff LOC5513668.sorted.gff<br/>

**Retrive lines that contain CDS**<br/>
grep CDS LOC5513668.X1.gff > LOC5513668.X1.cds.gff<br/>
**Next:**<br/>
bedtools getfasta -s -fi NW_001834348.1.fa -fo LOC5513668.X1.cds.fa -bed LOC5513668.X1.cds.gff<br/>

**concatenate exons together**<br/>
union LOC5513668.X1.cds.fa -outseq LOC5513668.X1.cds.union.fa<br/>

**Emboss translate**<br/>
transeq LOC5513668.X1.cds.union.fa -outseq LOC5513668.X1.aa.fa<br/>

**count number of lines containing x in file**<br/>
grep -c x filename<br/>

**look for x in less**<br/>
/x<br/>


**SHELLS**<br/>
**display values of a variable**<br/>
echo $variablename<br/>

**assign value to variable**<br/>
variablename=value<br/>

**get github repository**<br/>
git clone githublink<br/>

**remove directiory, move it**<br/>
rmdir lab4<br/>
mv lab4-myname lab4<br/>
cd lab4<br/>

**put homologs into one file example**<br/>
cat AF254382.1.fa  NR_145820.1.fa > 18s.fa<br/>
cat file1 file2 > filename.fa<br/>
**align combined sequences**<br/>
muscle -in combinedfile.fa -out combinedfile.aligned.fa<br/>
**to look at alignment**<br/>
alv -k combinedfile.aligned.fa | less -r<br/>
**calculate identity**<br/>
t_coffee -other_pg seq_reformat -in combinedfile.aligned.fa -output sim<br/>

**unzip file**<br/>
gunzip filename<br/>

**add comment git**<br/>
git commit -a -m "commenttext"<br/>
**other git cmds**<br/>
git status<br/>
git log<br/>
git restore filename<br/>
git push    (to commit)<br/>

**translating and keeping gaps**<br/>
faTrans inputfile.aligned.fa   outputfile.trans.fa<br/>


cp -r lab4-Raphael-Wtz/ ~/lab4_backup
