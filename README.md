# Commands

**Go to the directory where the key is**
cd C:\Users\Raphael\Desktop\College et Pro\sbu\BIO 312          (May not be needed due to perm conflicts, the key was moved to the root directory of the cmd)

**Connect to the instance**
ssh -i 312Key.pem ec2-user@54.235.102.113               (fine with disclosing my IP address here but normally try not to)

**List directory content**
ls

**Go to a directory**
cd ~/*DIRECTORY*
**Go up a directory**
cd ../
**Go to root directory**
cd

**See directories within a directory**
ls -d */

**Which directory am I in**
pwd

**Turn on web server**
sudo service httpd start

**ncbi app download help**
ncbi-acc-download -h

**Look at a downloaded file**
less *filename*           (spacebar down, P up, Q quit)

**Download a FASTA file**
ncbi-acc-download -F fasta *scaffoldname*

**Download a GFF3 file**
ncbi-acc-download -F gff3 *scaffoldname*

**Open grep manual**
man grep
**Example cmd to use grep**
grep LOC5513668 NW_001834348.1.gff > LOC5513668.gff                 (If you leave off '> file', the result will be printed to your screen the '>' sign redirects this to a file)
**To only include lines with word exon**
grep exon LOC5513668.gff > LOC5513668.mrna.gff
