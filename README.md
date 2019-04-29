# SysMLPromelaTransformation
ATL Transformation from SysML to Promela

How to run:
1. Copy the Jar file into a seperate folder
2. Also copy the MMInterModel.ecore and MMSpin.ecore files to the same folder
3. Run the Jar in terminal
```
   3.1. Copy the path to the .uml file from your Papyrus project to the terminal
```
4. Jar will create a folder named Result and put the three output files in it
5. The three files would contain
   ```
    5.1. Intermodel.xmi - It contains the intermodel generated during the transformation
    5.2. Spin.xmi - It contains the spin model in xmi format
    5.3 <ModelName>.pml - It contains the runnable code for promela.


Requirements:
1. JDK 8 or higher
2. Papyrus IDE generated SysML model


SysML is a vast language, we currently handle only a subset of it.
Elements handled:
1. Statemachine diagram
```
  1.1. states (simple and composite(only one level of substates))
  1.2. transitions (All activities or guards should be on transitions and not states)
  1.3. events for communication (Signal and call events handled)
```
2. Action diagram (only as an activity of a transition) (should only contain one node which describes the type of communication taking place)

3. Due to bug in ATL SDK, currently only global variables can be handled.


Airbag.uml file is a sample example provided along with the Jar.


