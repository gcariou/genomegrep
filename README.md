# genomegrep

`genomegrep` is a bioinformatics project written in Rust for searching DNA patterns inside genomic sequences.

The main goal of this project is to explore and implement different string-searching and genome-indexing algorithms while improving my Rust programming skills.

The project will start with simple exact pattern matching and progressively evolve toward more efficient search and indexing techniques commonly used in bioinformatics.

## Goals

The main objectives are to:

- Parse genomic sequences from FASTA files
- Search for DNA patterns inside a genome
- Implement several string-searching algorithms
- Compare their performance and memory usage
- Explore compact DNA representations
- Build persistent indexes for faster searches
- Learn more advanced genome-indexing techniques

The project is mainly intended as a learning project rather than a production-ready bioinformatics tool.

## Planned Features

The project will be developed progressively.

### Basic sequence search

- FASTA file parsing
- Naive pattern matching
- Search results with chromosome and position
- Multiple occurrences detection

Example:

```bash
genomegrep search genome.fa ACGTACGT
```

Possible output:

```text
chr1:15482
chr1:99328
chr3:487291
```

### Search algorithms

Several pattern-matching algorithms may be implemented and compared:

- Naive search
- Knuth-Morris-Pratt (KMP)
- Boyer-Moore

### Genome indexing

Later versions will explore indexed genome search using structures such as:

- Suffix arrays
- Burrows-Wheeler Transform (BWT)
- FM-index

The objective is to understand how preprocessing a genome can make repeated sequence searches much faster.

### Bioinformatics features

Possible future features include:

- Reverse-complement search
- Multiple chromosome support
- Ambiguous nucleotides such as `N`
- Approximate matching with mismatches
- Compact 2-bit DNA encoding

### Performance

Another important part of the project will be comparing the different approaches in terms of:

- Execution time
- Memory usage
- Index construction time
- Query time

Parallel processing may also be explored using Rust libraries such as Rayon.

## Example Architecture

```text
genomegrep/
├── src/
│   ├── main.rs
│   ├── cli.rs
│   ├── fasta.rs
│   ├── sequence.rs
│   ├── search/
│   │   ├── naive.rs
│   │   ├── kmp.rs
│   │   └── boyer_moore.rs
│   └── index/
│       ├── suffix_array.rs
│       ├── bwt.rs
│       └── fm_index.rs
├── tests/
├── benches/
└── Cargo.toml
```

This architecture is only a long-term direction and will evolve as the project grows.

## Project Status

Early development.

The first objective is to implement a simple FASTA parser and exact DNA pattern search before introducing more advanced algorithms and indexing structures.
