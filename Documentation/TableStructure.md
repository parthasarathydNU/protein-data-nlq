### 1. **SQL Table Creation**

#### Codon Usage Table
```sql
CREATE TABLE codon_usage (
    codon VARCHAR(10),
    aa CHAR(1),
    freq DECIMAL(10, 4),
    abundance DECIMAL(10, 4)
);
```

#### Gene Aliases Table
```sql
CREATE TABLE gene_aliases (
    gene_id VARCHAR(255),
    alias1 VARCHAR(255),
    alias2 VARCHAR(255),
    alias3 VARCHAR(255),
    alias4 VARCHAR(255),
    alias5 VARCHAR(255),
    alias6 VARCHAR(255),
    alias7 VARCHAR(255),
    alias8 VARCHAR(255),
    alias9 VARCHAR(255)
);
```

#### Gene Annotations Table (for GAF files)
```sql
CREATE TABLE gene_annotations (
    source VARCHAR(50),
    gene_id VARCHAR(255),
    symbol VARCHAR(255),
    go_id VARCHAR(50),
    reference VARCHAR(255),
    evidence VARCHAR(50),
    aspect CHAR(10),
    description TEXT,
    synonym VARCHAR(255),
    gene_type VARCHAR(100),
    taxon VARCHAR(50),
    date VARCHAR(20),
    assigned_by VARCHAR(100)
);
```
