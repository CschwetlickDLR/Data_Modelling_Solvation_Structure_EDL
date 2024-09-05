This repository contains the simulation data for " Modelling Solvation Structure in the Electrochemical Double Layer" by C. Schwetlick, M. Schammer, A. Latz & B. Horstmann.

The data found here are Matlab workspace saves. The results of the simulations used for the plots and general results in the paper are contained in these. 

The naming structure is the following -- example "3sS_V+_loopdilution_symmetric_E-4"
  3s -- refers to a 3 species run
  S -- refers to a simulation with solvation (0 refers to a simulation without)
  V+ -- refers to a simulation run over all positive electrode potentials (cf. V-)
  loop -- refers to a looped run
  dilution -- refers to the variable over which the loop was run, here the relative salt concentration (other options include nu3, the size of the cation; beta2, the binding energy; c3_start, the absolute salt concentration)
  symmetric_E-4 -- refers to a description of the electrolyte parameters (in this case, equal size ions, binding energy of -4*RT)

Inside the files the following data can be found:
  V_sign, comparable, series, solvation -- all contain data which can be found in the file name
  loopvariablename -- contains a String of the variable looped over
  loopvalues -- contains an array length _N_ of all values loopvariable takes in the simulations
  output -- only relevant for the simulation code
  params -- contains all parameters used in the simulation (the units are found in "Parameter_File.txt")
      length -- cutoff length (distance from bulk)
      E_start -- electric field in the bulk
      R -- physical const.
      T -- simulation temp.
      F -- physical const.
      e0 -- physical const.
      c3_start -- salt concentration in the bulk (if looped over dilution, calculated from dilution)
      epsilon -- dielectric const.
      t3 -- transference number (not used here)
      z1,z2,z3 -- charge numbers of the three species (1 refers to the solvent)
      M1,M2,M3 -- molar masses of the three species (not used here)
      nu1,nu2,nu3 -- molar volumes of the three species
      beta2,beta3 -- binding energies between species 1 and 2 or species 1 and 3 respectively
      l2m,l3m -- maximum size of the solvation shell for species 2 and 3
      RT -- room temp. energy
      abstolerance,reltolerance -- tolerance values for the simulation
  solution -- contains the simulation data for 7 variables, each of length _N_, each simulation corresponding to the values in loopvalues
      x -- the distance from the bulk
      phi -- the local electric potential
      E -- the local electric field
      rho -- the local charge density
      c_1,c_2,c_3 -- the local concentrations of the three species
