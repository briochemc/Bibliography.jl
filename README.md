# Bibliographies.jl

Bibliography is a Julia package for handling both import/export from various bibliographic format.

### Organization

This package comes as a set of 3 packages to convert bibliographies. This tool was split into three for the sake of the precompilation times.
- [Bibliography.jl]((https://github.com/Azzaare/Bibliography.jl)): the interface to import/export bibliographic items.
- [BibInternal.jl]((https://github.com/Azzaare/BibInternal.jl)): A julian internal format to translate from and into.
- [BibParser.jl]((https://github.com/Azzaare/Bibliography.jl)): A container for different bibliographic format parsers (such as BibTeX).

### Packages using Bibliographies

- [StaticWebPages.jl]((https://github.com/Azzaare/StaticWebPages.jl)): a black-box generator for static websites oriented towards personal and/or academic pages. No knowledge of Julia nor any other programming language is required.

### Contributions are welcome
- Write new or integrate existing parsers to [BibParser.jl]((https://github.com/Azzaare/Bibliography.jl)) (currently only a light BibTeX parser is available)
- Add new bibliographic items (with optional construction rules) to [BibInternal.jl]((https://github.com/Azzaare/BibInternal.jl)) (currently only BibTeX items are listed)
- Add import/export from existing bibliographic formats to [Bibliography.jl]((https://github.com/Azzaare/Bibliography.jl))
- Add export for non-bibliographic formats (such as in [StaticWebPages.jl]((https://github.com/Azzaare/StaticWebPages.jl)))

## Short documentation 

```julia
# Import a BibTeX file to the internal bib structure
import_bibtex(source_path::AbstractString)

# Export from internal to BibTeX format
export_bibtex(target_path::AbstractString, bibliography)

# Check BibTeX rules, entry validity, clean and sort a bibtex file.
export_bibtex(target_path::AbstractString, import_bibtex(path_to_file::AbstractString))

# Export from internal to the Web Format of StaticWebPages.jl
export_web(bibliography)

# Export from BibTeX to the Web Format of StaticWebPages.jl
bibtex_to_web(source_path::AbstractString)
```
