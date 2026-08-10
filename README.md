As a data scientist, I frequently find myself in need of domain-specific tools optimized for constrained research environments, tools which all-too-often do not yet exist. Therefore, I started to build (and share) my own tools. Below is an overview of some of the projects I have made public along with the philosophy that helped develop them.

## Design Philosophy
I build tools under three governing ideas:
1. pragmatic minimalism (“Do everything necessary to do one thing well”),
2. literate programming (inspired by Knuth, but adopted to the AI era), and
3. structured collaboration with AI agents (see the [Working Agreement](https://github.com/andy-emerson/working-agreement)).

## Public Repos
### Minimal production server
* Many tools were pure client-side, so I needed a server small enough for a Raspberry Pi yet secure enough for real use. [Servette](https://Servetteorg) is a single-file pure-Python static site server.

### Client-side notebook and runtime
* The original tool was a fully client-side notebook for Python and SQL. The same layout became [LoveIDE](https://LoveIDE.org.com). Supporting it required [love.wasm](https://github.com/andy-emerson/love.wasm) and [lua.wasm](https://github.com/andy-emerson/lua.wasm).

### Embeddable numeric database
* The notebook needed an embeddable database that could both ingest and compute quickly on ordered numeric data. [TallyDB](https:TallyDB.com) is an append-optimized SQL database with zero-copy compute access.

### Numeric libraries
* Faster in-database compute led to embedding Lua, which required a serious numeric stack. [MatLua](https://github.com/andy-emerson/MatLua) is a NumPy-shaped array and linear algebra library for Lua. [blas.wasm](https://github.com/andy-emerson/blas.wasm) provides the WebAssembly foundation for future numeric work.
