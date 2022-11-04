# Job Shop Layout Optimisation
This project aims to improve the productivity in a job shop by optimising the space allocation of 
all machines on the floor along with the job scheduling based on the job dependency relationship and
the job shop layout. 

Our approach to the project can be divided into two parts: 
1. the space allocator 
2. the job scheduler. 

The user can load a saved layout file into the software or draw the layout 
directly in the floor layout editor for the space allocator. All machine positions can be utilised 
for job assignments, where graph-based job dependencies can be input. The space allocator uses 
different algorithms (e.g., population-based meta-heuristic) to obtain the optimal space allocation 
for these machines. 

The job scheduler will then output a feasible job arrangement for each machine 
over time. We have used an abstract implementation for the optimisation algorithms to allow for 
future additional algorithms to be easily added to this project. A better display of the result 
might also be added to future development.

## Structure
- The [GUI](/src/main/java/uk/ac/nottingham/grp/jobshopmanufacturing/GUI/package-info.java) 
    package contains the main user interface implementation. The floor layout editor is implemented 
    here.
- The [Optimisation](/src/main/java/uk/ac/nottingham/grp/jobshopmanufacturing/Optimisation/package-info.java) 
    package contains the optimisation algorithms, which is the main working part of the project.
    Both the space allocator and the job scheduler's algorithms are implemented here.
- Other packages, i.e., [MapElement](/src/main/java/uk/ac/nottingham/grp/jobshopmanufacturing/MapElement/package-info.java) 
    , [Jobs](/src/main/java/uk/ac/nottingham/grp/jobshopmanufacturing/Jobs/package-info.java), and
      [FloorLayout](/src/main/java/uk/ac/nottingham/grp/jobshopmanufacturing/FloorLayout/package-info.java),
    are underlying utility elements used for two main packages.

## JavaDoc
The generated JavaDoc is available at [doc folder](doc/index.html).

To see it, please clone the project and open the index in your browser.

## Tests
The tests can be run in IntelliJ IDEA after cloning our repository. 

The test folder is [src/test](src/test).

## Credit
Team 12 thanks to the following opensource projects:
1. [JavaFX](https://openjfx.io/)
2. [toml4j](https://github.com/mwanji/toml4j)
3. [OR-Tools](https://developers.google.com/optimization)
