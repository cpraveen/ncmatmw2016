# Discontinuous Galerkin method

Material for the ATM Workshop on PDE and Mechanics held in Kerala School of Mathematics, Kozhikode, 4-6 Feb., 2016. See

http://cpraveen.github.io/teaching/ncmatmw2016.html

* 1d_scalar_legendre: Solves linear convection equation with periodic bc
* 1d_burger_legendre: Solves Burger's equation in 1d with periodic bc
* 2d_scalar_unsteady_legendre: Solves 2d linear advection equation

All these codes are run as follows
```
cmake .
make release
./dg
```
In the 1d cases, you can run gnuplot to see any animation
```
gnuplot anim.gnu
```
The 2d code saves solution in vtk format which can viewed using [Visit](https://wci.llnl.gov/simulation/computer-codes/visit). To try adaptation in the 2d test case, make these changes and run the code
```
unsigned int n_points = 40;
unsigned int n_refine_init = 3;
unsigned int n_refine_interval = 5;
```
