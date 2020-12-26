# Central-Dogma-Turing-Machine
We begin with an input string in Tape 1 that represents a DNA sequence. Starting with the first character, we will scan the nucleotides left to right on all 3 tapes, transcribing the DNA into mRNA on tape 2, until we reach a blank (B), at which point we will turn around and traverse left on all 3 tapes until we reach a blank (B), where we will turn right and return to our first symbol, now with Tape 2 containing the mRNA. Now with the DNA and mRNA, we will traverse tapes 1 and 2 looking for AUG indicating a start codon. Upon finding the start codon AUG, we will replace the blank on the third tape with ‘M’ marking the beginning of an ORF. From here we will record an amino acid for every 3 nucleotides in the mRNA. Upon reaching a stop codon, the ORF is complete, and we are ready to search for another start codon to initiate an ORF. Halting may occur if there is another start codon within an ORF, or the end of the input is reached and no ORF is detected, or if a start codon has indicated the beginning of an ORF, but no stop codon has been found. In all these cases, halting will occur, and the DNA sequence will be rejected.

Within our Turing machine, when we enter an ORF, we are at a central state (Q5), from which we can obtain many different amino acids. This is done by clustering states together. For example, the main clusters are codons beginning with ‘A’, ‘U’, ‘G’, or ‘C’, with sub clusters for the next nucleotide.
