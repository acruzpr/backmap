<pre>        _       _     __  __    _    ____  
  _ __ | | ___ | |_  |  \/  |  / \  |  _ \ 
 | '_ \| |/ _ \| __| | |\/| | / _ \ | |_) |
 | |_) | | (_) | |_  | |  | |/ ___ \|  __/ 
 | .__/|_|\___/ \__| |_|  |_/_/   \_\_|      v 0.0.0.0.0.0.0...
 |_|                 (Multi-angle Picture)
</pre>
This tool provides easily readable "pictures" of protein conformations, 
ensembles, and trajectories saved as either a combined protein databank 
(PDB) structure file, or a directory of such files, and produces graphs.

This tool provides easily readable "pictures" of protein conformations, 
ensembles, and trajectories saved as either a combined protein databank 
(PDB) structure file, or a directory of such files, and produces graphs.

#Usage
```
python plotmap.py -pdb ProteinDatabankStructureFilename.pdb
python plotmap.py -pdb /directory/containing/pdbs/
```

#Output 

The x-axis always represents the models/structures listed in the PDB.
```
filename.rcode.eps      (y-axis: residue #; color: R number based on "-signed" and <rcode_cmap>)<br>
filename.rcode.his.eps  (y-axis: Ramachandran number (R); color: frequency of R in model)<br>
filename.rcode.rmsf.eps (y-axis: residue #; color: RMSF in R from the previous model)<br>
```


#Additional tags
<pre>
-h       -     Prints this message<br>
-ss      -     Color the ramachandran number codes (R-codes) by <br>
               secondary structure (default: color by chirality and sign)<br>
-signed  -     Use the signed version of the ramachandran number<br>
-rmsd    -     Also producee "filename.rcode.rmsd.eps"<br>
               (y-axis: residue #; color: RMSD in R from first model)<br>
</pre>

Each graph is also accompanied by "_colorbar.eps", which are keys.

The Ramachandran number concept is discussed in the manuscript:<br>
Mannige (2018) "A simpler Ramachandran number can simplify the life of a protein simulator" Submitted. Manuscript available [here](manuscript/plotmap.pdf).

Mannige, Kundu, Whitelam (2016) "The Ramachandran number: an order parameter for protein geometry" 
PLoS ONE. [11(8):e0160023](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0160023)
