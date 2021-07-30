# Beta-Release of PK-Sim 10 and MoBi 10
Dear OSP users, 

We are happy to announce that the new Version 10 of PK-Sim and MoBi is now available for beta-testing. The beta-test phase will last until the **end of August**.
The goal of the beta release is to give you an opportunity to test the new features and to let us know if you have any problems or feedback regarding the new implementation.

## How can you test the new features?
You can use the *portable versions* of PK-Sim and MoBi  (download links below). The portable versions do not require installation and can be used in parallel to the official OSP Suite 9.

Your feedback on the new features is highly welcome.

**Important**: The beta-test versions are not final releases of the software packages: please use them for testing purposes only, but not for productive work.

## Downloads:

- [PK-Sim 10 beta portable](http://pk-sim-portable.open-systems-pharmacology.org)

- [MoBi 10 beta portable](http://mobi-portable.open-systems-pharmacology.org)

## New features

### Modeling of Protein expressions in PK-Sim redesigned and extended
See the [documentation](https://docs.open-systems-pharmacology.org/v/v10/working-with-pk-sim/pk-sim-documentation/pk-sim-expression-data) for details.



![](https://user-images.githubusercontent.com/25061876/127345732-874fac2b-220a-40f5-8f5c-92bcdd59128c.PNG)

* More flexible protein localization settings
  * Enzymes/Binding partners: introduction of **fraction expressed** in different compartments
  * Transporters: introduction of **fraction expressed apical/basolateral** (Kidney/Liver/GI) and **fraction expressed blood brain barrier/tissue** (brain)
* Introduction of **Initial Protein Concentration** as explicit parameter

See [Localizations and initial concentrations of enzymes](https://docs.open-systems-pharmacology.org/v/v10/working-with-pk-sim/pk-sim-documentation/pk-sim-expression-data#localizations-and-initial-concentrations-of-enzymes) and [Localizations, directions, and initial concentrations of transport proteins](https://docs.open-systems-pharmacology.org/v/v10/working-with-pk-sim/pk-sim-documentation/pk-sim-expression-data#localizations-directions-and-initial-concentrations-of-transport-proteins) for the detailed description.

* New transporter types:
  * Plasma <=> Blood Cells
  * Plasma <=> Interstitial
  * Bidirectional

* Transport direction (Influx/Efflux/…) can be set in each organ independently

  ![](https://gblobscdn.gitbook.com/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2F59ea81127a226c02aa651a638378bb80308da5d8.png?alt=media)

### Observed data import in PK-Sim and MoBi redesigned and extended

See the [documentation](https://docs.open-systems-pharmacology.org/v/v10/shared-tools-and-example-workflows/import-edit-observed-data) for details.

* Better support for "Nonmem like" data formats (s. [Supported Formats](https://docs.open-systems-pharmacology.org/v/v10/shared-tools-and-example-workflows/import-edit-observed-data#supported-formats))

* Fully redesigned user interface

  ![](https://gblobscdn.gitbook.com/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2F8e87a7442c2e18566eed7136718bf39da826c8ff.png?alt=media)

* Import configuration can be saved and reused

  ![](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2F882f7fd4813c22d4dca87ce8d5700c4838b757f7.PNG?generation=1627477017995096&alt=media)

* Previously imported observed data can be **updated** from a new data source

  ![](https://gblobscdn.gitbook.com/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2Fdecc0becc12850ba17ccdf9306d85f9ad81779b7.png?alt=media)

* Extended data filtering

  ![](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2Fd5c36dd11136d5f29c6e42ae08f7bd86570e33ac.png?generation=1624564037744769&alt=media)

### New population templates (Chronic Kidney Disease) added

![](https://user-images.githubusercontent.com/25061876/127352299-413b934e-0a31-4be2-ac1f-adffe80f973a.PNG)

## Fixed issues and Improvements

### PK-Sim


* [Bug comparison chart population](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1825)
* [Plots: Default background color does not match](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1822)
* [Deleting referenced compound template corrupts the template database](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1498)
* [Simulations cannot be loaded from snapshot if used Individual or Population Building block was renamed](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1662)
* [Export time profile analysis change the units](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1640)
* [Renaming protein in individual does not trigger changed state of simulation](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1451)
* [Information in advanced protocol is lost in snapshot](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1601)
* [Wrong parameter descriptions](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1810)
* [The predefined templates for age groups are not supported anymore](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1679)
* [PI: "Id not unique"](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1299)


### MoBi

* [Tags for event groups](https://github.com/Open-Systems-Pharmacology/MoBi/issues/487)
* [Manual input for event assignment path](https://github.com/Open-Systems-Pharmacology/MoBi/issues/485)
* [Container criteria "in container" only applies for the children of the container](https://github.com/Open-Systems-Pharmacology/MoBi/issues/523)
* [Molecule keyword replacement does not work for global parameter referencing other global molecule parameters](https://github.com/Open-Systems-Pharmacology/OSPSuite.Core/issues/832)
* [Drag and drop of parameter to the "references area" does not work](https://github.com/Open-Systems-Pharmacology/MoBi/issues/507)

### PK-Sim and MoBi

* [PI Corrupted when referencing a process parameter that is removed from the simulation](https://github.com/Open-Systems-Pharmacology/OSPSuite.Core/issues/497)
* [Parameter  Identification: When User close and reopen the PI the results section  shown the new boundaries and not those used in the PI run](https://github.com/Open-Systems-Pharmacology/OSPSuite.Core/issues/818)
