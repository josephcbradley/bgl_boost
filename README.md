# bgl_boost
An old BGL release for new MATLAB users.

1. Move to `~/dev/lib`

```bash
cd ~/dev
```

2. Clone the custom boost from [here](https://github.com/josephcbradley/bgl_boost):

```bash
git clone https://github.com/josephcbradley/bgl_boost
```

3. Assuming you are still in `~/dev/lib/boost`, clone `matlab-bgl`:

```bash
git clone https://github.com/josephcbradley/matlab-bgl
```

4. Move into `matlab-bgl/libmbgl/` and run the compile script:

```bash
cd matlab-bgl/libmbgl/
sh compile-macosx-intel-64-large.sh
```

5. You will get some warnings from clang and from the archiver, you can ignore them.
6. Open MATLAB and change your folder to `~/dev/matlab-bgl/private` . At the prompt run:

```matlab
compile
```

7. There will be lots of warnings about new versions of macOS, ignore them. To check everything, copy the `matlab-bgl` into any project that you need. To include the compiled code, run (in MATLAB):

```matlab
addpath("matlab-bgl/")
```

8. Then test some code:

```matlab
X = randn(50, 50); C = X' * X
g = graph(doPMFG(C))
plot(g)
```

## References

Bottom comment of this thread: 

[Question #69161 "compiling for maci46" : Questions : Matlab BGL](https://answers.launchpad.net/matlab-bgl/+question/69161)
