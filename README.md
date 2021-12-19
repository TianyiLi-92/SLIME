# SLIME
# Description
**SLIME** (Spherical LInear Magnetoconvection Eigensolver) is a software computing the linear onset of magnetoconvection in a full sphere or a spherical shell. SLIME solves the linear incompressible Navier-Stokes in a rotating reference frame. It also takes into account the coupled induction equation for the induced magnetic field with a background magnetic field, as well as the temperature and concentration equations in the Boussinesq framework.

The development of SLIME is inspired by [SINGE](https://gricad-gitlab.univ-grenoble-alpes.fr/Geodynamo/Singe), a well-known code for computing free eigenmodes of a rotating spherical cavity filled with a Boussinesq fluid. SLIME solves the linear magnetoconvection equations using a parallel pseudo-spectral method. The velocity and magnetic field perturbations are decomposed into the poloidal part and the toroidal part, which are then projected onto spherical harmonics. In the radial direction, since high accuracy tends to be crucial for eigenvalue computations, besides finite differences[^1], SLIME also implements Chebyshev spectral method for the differentiation. For the solution of large scale sparse eigenvalue problems, SLIME can use either the [MATLAB solver](https://ww2.mathworks.cn/help/matlab/ref/eigs.html?lang=en) on your personal computer or the [SLEPc](https://slepc.upv.es/) library available on parallel supercomputers. A post-processing program is provided to convert useful data into the format of the [XSHELLS](https://nschaeff.bitbucket.io/xshells/) code. Tools provided by XSHELLS can then be used for post-processing and visualization of data.

SLIME is licensed under the GNU GPL, version 3 or (at your option) any later version.







Full source code will be published after we finish the manual...:smile:
