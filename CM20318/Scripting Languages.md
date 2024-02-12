*Examples*: DOS batch, \*sh, Python, Sed, Perl, Ruby, JavaScript
Notable features:
- "Not particularly good at classical number crunching"* 
- Processing with strings is quite common.
- Often interpreted, but not always.

\*Python's quite good at this, with some libraries.

### Job Control Languages

Scripting languages originate for controlling jobs for early mainframes (see IBM's JCL — Job Control Languages).

Modern mainframe equivalents (supercomputers) are typically still managed by job scripts (PBD, SLURM). 
### Shell Languages
UNIX used a command-line interface with a language called `sh`. Variants such as `csh`, `bash`, `zsh` emerged later.

Shell scripts are used to automate repetitive tasks.

They don't require a GUI which means they can be used nearly everywhere (even when the machine doesn't have a graphical output).
### String Manipulation
`sed` (stream edit), from UNIX is a regular expression-based string manipulation language.

`sed` can work with files, and even streams of data — where the entire text isn't in memory at once.

`sed` was succeeded by `awk`, and then Perl.

### Perl
Perl is its own programming language, whose notable features include string pattern matching, first-class functions, and objects!  
```perl
open IN, '<', 'infile';
open OUT, '>outfile';
$count = 0;
while (<IN>) {
s/world/everybody/ if (/hello/);
print OUT;
$count++;
}
close IN;
close OUT;
print "$count lines\n";
```

Some peculiarities in Perl include:
- *Variable Sigils* — `$` for scalars, `@` for arrays, `&` for functions (you can even have `$a`, `@a`, `&a` all simultaneously in scope!)
- *Default Variables* — In Perl, `$_` is a default variable (depending on the context), so functions like `print` use that default variables.
### Python
