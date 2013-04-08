# FastOpenStruct

FastOpenStruct is a reimplementation of Ruby's OpenStruct that avoids invalidating MRI's method caches on every instantiation.

It should be a drop in replacement for OpenStruct.

## Performance

```
λ ruby -I./lib bench/attribute_lookup.rb
                     user     system      total        real
OpenStruct       0.730000   0.000000   0.730000 (  0.732052)
FastOpenStruct   0.220000   0.000000   0.220000 (  0.224770)
```

```
λ ruby -I./lib bench/10_000_instantiations.rb
                     user     system      total        real
OpenStruct       0.630000   0.010000   0.640000 (  0.645598)
FastOpenStruct   0.240000   0.000000   0.240000 (  0.239307)
```

## Licence

Simplified BSD

```
Copyright (C) 2013 Charlie Somerville. All rights reserved.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met: 

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer. 
2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution. 

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR
ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```
