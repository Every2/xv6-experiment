# xv6 Experiment

Learning more about osdev with xv6 kernel.

# How to run

First, cross compile the compiler

```
git clone --recurse-submodules git@github.com:riscv-collab/riscv-gnu-toolchain.git
./configure --prefix=/opt/riscv
sudo make -j $(nproc)
```

And compile riscv qemu

```
git clone git@github.com:qemu/qemu.git
git checkout stable/8.2
./configure --target-list=riscv64-softmmu
make
sudo make install
```

Now, you can run:

```
make fs.img && make qemu
```
