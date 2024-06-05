# Understanding the Use case

## 5th June 2024

[Summarized Version](./UseCases/01_ProteinFunctionDiscoveryThroughNLQ.md)

### Notes from Conversation 

A geneId will look like PF3d_01107. This was part of the UniProt Database

One use case could be fetching domains based on gene id. domains are predicted by smart , pfam values. 

In fasta files
proteins are annotated as hypothetical protein and plasmodium conserved protein 
For many organisms there is many information that is missing

Some proteins are named as just hypothetical proteins and we do not know their function. Assume a parasite like plasmodium facliparium, causes so many people to die, and it has been there for such a long time. 40% of the genes, we have no idea what their function could be. No one is working on them becuase we do not know anything about them. What can be done is we can bring functions from other organisms. 

There is a method called Blast, that compares one protein sequence to another protein sequence. it matches protein sequence. For example if I am matching plasmodium protein ( a hypothetical protein ) against fungus or be the entire Uniprot data. If that protein sequence resembles some other protein from Human, then we may say that this protein may have a similar function. People annotate genes by importing or by using second hand information form other systems. This is called reciprocal blast based gene annotations. 

So a good use case would be, can we fetch hypothetical proteins with known smart or pfam domains ? 

For example the user's work is on histone proteins, which protects our dna, 40% of the genes we don't have an idea about. It is a dark box. So the user wants to know are there any protein sequence amongst the hypothetical proteins that can potentially have this function, then people can work on it . That this protein is likely to have this function that I am interested in.  

Smart and Pfam predict domains based on protein sequence. For example if a protein has a sequence TALLP - this indicates one particular function that is present say in hair or in the heart. And assume this protein is there in humans and has been annotated that this protein has this sequence and it stays in the heart. And now we find a similar protein in fruit flies, and we don;t have any knowledge what that protein in fruit flies would do, but we know what sequence we are looking for. So Smart and Pfam look for such sequences in any organism. So they are extrapolating an information into another system. So a known sequence in human can then be searched in a fly and they will annotate that protein saying this is a heart related protein.

Pfam is a computational program that is trained by biologists that looks for conserved sequences in the protein database. And wherever we find conserved sequences, that protein is annotated functions with existing knowledge from other systems. That is what PFAM and Smart do


from the fasta file find out how many proteins are listed as hypothetical and how many are conserved

We want to find for how many of these proteins are there known smart and pfam domains predicted

### Now why this tool ? 

Saw we have about 2500 proteins out of which we have the predicted functions of some proteins. Now even if the person wants to work on a particular protein, they will have to pick and choose, there comes the problem. 

So the next level of queryig would be which proteins have the following functionlaitites associated with them. 

Now if out of the 2400 proteins, if we say there are 500 proteins with the following functions (given by smart or pfam ). The user can then perform expirements and prove it. 

But to start with this process, the biologist, needs some information to pick and choose the protein that they want to work on.
