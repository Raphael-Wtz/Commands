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
