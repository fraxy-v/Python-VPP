# Python-VPP

![Upload Python Package](https://github.com/TAJD/Python-VPP/workflows/Upload%20Python%20Package/badge.svg)

3-DOF Velocity Prediction Program base on the [ORC](https://www.orc.org/index.asp?id=21) aero and hydro dynamic models. The code make use of Object-oriented-Programming to be very general.



## Getting Started
### To Do List (prioritized)
1. ~~wrap rig into yacht class~~, and update measure functions
2. validate on YD-41 (Principle of Yacht Design), and write tests
3. ~~optimize the boat velocity with the 3-DOF equlibrium as constraints (Lagrange multipliers)~~
4. Add all the windag contributions (mast, crew, rigging, etc.)
5. Optional Delft hydro model
6. Add dagerboards to the possible appendages  
6. ~~tidy plotting and results~~

### Prerequisites

### Running the tests

<p align="center">
    <img src="Figure.png" alt="YD-41 VPP results" width="1024">
</p>

## Using the code

See the [documentation](https://marinlauber.github.io/Python-VPP/).

### Input variable

1. Appendages :
    * Cu : Root Chord / Upper Chord (m)
    * Cl : Tip Chord / Lower Chord (m)
    * Span : Span (m) 
1. Yacht : 
    * Lwl : Length waterline (m)
    * Vol : Displ. volume of canoebody (m^3)
    * Bwl : Beam waterine (m)
    * Tc : Canoebody draft (m)
    * WSA : Wetted surface area (m^2)
    * Tmax : Draft max, i.e. Keel (m)
    * Amax : Max. section area (m^2)
    * Mass : Total mass of the yacht, includeing keel (kg)
    * Ff : Freeboard heigt fore (m)
    * Fa : Freeboard height aft (m)
    * Boa : Beam overall (m)
    * Loa : Length overall (m)
    * App : List of appendages
    * Sails : List of Sails
1. Sails:
    Standard measurements, except Roach is defined as 1-A/(0.5PE)
    Kite only takes area and vce esitmate
1. VPP.set_analysis()
    * TWA range : range of TWA to use
    * TWS range : range of TWS, must be between [2, 35]


## Authors

* **[Otto Villani](https://www.linkedin.com/in/otto-villani-552760108/)** - *Initial idea, model selection* - [github](https://github.com/ottovillani)
* **[Marin Lauber](https://www.linkedin.com/in/marin-lauber/)** - *Initial idea, developement* - [github](https://github.com/marinlauber)
* **[Thomas Dickson](tajd.github.io)** - *Developer*

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration



## Modifications

1. Formatted using [Black](https://github.com/psf/black).
1. Added a "name" to the Yacht class which can be passed to plotting function.
1. Renamed instances of Keel and Rudder objects in the example function.