# Downloads:

- [Full setup TODO link](XXX)

- [**ospsuite** R package TODO link](XXX)

- [Gene expression database (human)](https://github.com/Open-Systems-Pharmacology/Gene-Expression-Databases/releases/download/v2.0.0/GENEDB_human.expressionDb)

# Release Notes for the Open Systems Pharmacology Software Suite 10

## New features

### New population templates (Chronic Kidney Disease) added

3 CKD population templates added (based on the publication [Malik PRV, Yeung CHT, Advani U, Dije S, Edginton AN. A Physiological Approach to Pharmacokinetics in Chronic Kidney Disease. J Clin Pharmacol 2020. 60 Suppl 1: S52-S62. doi: 10.1002/jcph.1713](https://accp1.onlinelibrary.wiley.com/doi/full/10.1002/jcph.1713)):
* **CKD - Stage 3**: defined as patients with GFR of `31 - 60 [mL/min/1.73m²]`
* **CKD - Stage 4**: defined as patients with GFR of `16 - 30 [mL/min/1.73m²]`
* **CKD - Stage 5**: defined as patients with GFR of   ` 1 - 15 [mL/min/1.73m²]`

Each population includes 1000 individuals aged 18-80 years old, 50% male, based on European population (ICRP)

![](https://user-images.githubusercontent.com/25061876/127352299-413b934e-0a31-4be2-ac1f-adffe80f973a.PNG)

### OSP Platform qualification library and PBPK Models Library
#### PBPK Models library extended
New PBPK models were added:
* Amikacin
* Montelukast
* Raltegravir
* Sufentanil
* Vancomycin

Model building process and model quality of every new PBPK model is documented in the corresponding _model evaluation report_. 
#### New releases of OSP Platform qualification library and PBPK Models Library
As with every new OSP Suite release, ALL platform qualification reports and model evaluation reports have been recreated with the new version of the OSP suite and the latest version of the [_OSP Qualification Framework_](https://github.com/Open-Systems-Pharmacology/QualificationPlan/releases/latest):
* [**_OSP Qualification Reports library_**](https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports) ([https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports](https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports))
* [**_OSP-PBPK-Model-Library_**](https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library)([https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library](https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library))

### Modeling of Protein expressions in PK-Sim redesigned and extended
See the [documentation](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/pk-sim-expression-data) for details.

![](https://user-images.githubusercontent.com/25061876/127345732-874fac2b-220a-40f5-8f5c-92bcdd59128c.PNG)

* More flexible protein localization settings
  * Enzymes/Binding partners: introduction of **fraction expressed** in different compartments
  * Transporters: introduction of **fraction expressed apical/basolateral** (Kidney/Liver/GI) and **fraction expressed blood brain barrier/tissue** (brain)
* Introduction of **Initial Protein Concentration** as visible parameter

See [Localizations and initial concentrations of enzymes](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/pk-sim-expression-data#localizations-and-initial-concentrations-of-enzymes) and [Localizations, directions, and initial concentrations of transport proteins](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/pk-sim-expression-data#localizations-directions-and-initial-concentrations-of-transport-proteins) for detailed descriptions.

* New transporter types:
  * Plasma <=> Blood Cells
  * Plasma <=> Interstitial
  * Bidirectional

* Transport direction (Influx/Efflux/Bidirectional) can be set in each organ independently

  ![](https://gblobscdn.gitbook.com/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2F59ea81127a226c02aa651a638378bb80308da5d8.png?alt=media)

### Observed data import in PK-Sim and MoBi redesigned and extended

See the [documentation](https://docs.open-systems-pharmacology.org/shared-tools-and-example-workflows/import-edit-observed-data) for details.

* Better support for "Nonmem-like" data formats (s. [Supported Formats](https://docs.open-systems-pharmacology.org/shared-tools-and-example-workflows/import-edit-observed-data#supported-formats))

* Fully redesigned user interface

  ![](https://gblobscdn.gitbook.com/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2F8e87a7442c2e18566eed7136718bf39da826c8ff.png?alt=media)

* Import configuration can be saved and reused

  ![](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2F882f7fd4813c22d4dca87ce8d5700c4838b757f7.PNG?generation=1627477017995096&alt=media)

* Previously imported observed data can be **updated** from a new data source

  ![](https://gblobscdn.gitbook.com/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2Fdecc0becc12850ba17ccdf9306d85f9ad81779b7.png?alt=media)

* Extended data filtering

  ![](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LNl6UIiFP7k0sNQthlR%2Fsync%2Fd5c36dd11136d5f29c6e42ae08f7bd86570e33ac.png?generation=1624564037744769&alt=media)

### InVitro-InVivo calibration of intestinal permeability
TODO description and Link to WIKI 
![grafik](https://user-images.githubusercontent.com/25061876/137127894-edd9fe18-d992-4418-a330-91b2e5704ce2.png)

### New release of the **ospsuite** R package

* Many Fixed issues and Improvements (s. the [**ospsuite** R package release page](https://github.com/Open-Systems-Pharmacology/OSPSuite-R/releases/tag/v10.0.70) for details)
* Significantly improved performance on multicore machines (s. [Efficient calculation with the ospsuite R package](https://www.open-systems-pharmacology.org/OSPSuite-R/articles/efficient-calculations.html))
* R 4.x is now supported.

S. [documentation of the new R-Toolbox](https://www.open-systems-pharmacology.org/OSPSuite-R/) for detailed description and usage examples.

### (Re-)Qualification framework updated
OSP (Re-)Qualification framework is a technical framework to assess the confidence of specific intended use of the OSP platform. This framework allows for an automatic (re)-qualification workflow of the OSP suite. New release of the OSP (Re-)Qualification framework provides some improvements and bugfixes (s. below).

* (Re-)Qualification framework is not part of the OSP Suite setup (is only required for the creation of qualification reports) and must be installed separately. The latest release can be found [here](https://github.com/Open-Systems-Pharmacology/QualificationPlan/releases/latest)
* Full documentation of the (Re-)Qualification framework can be found [here](https://docs.open-systems-pharmacology.org/shared-tools-and-example-workflows/qualification)

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
* [Bug: Drug and Metabolite transporter inhibition](https://github.com/Open-Systems-Pharmacology/PK-Sim/issues/1861)

### MoBi

* [Tags for event groups](https://github.com/Open-Systems-Pharmacology/MoBi/issues/487)
* [Manual input for event assignment path](https://github.com/Open-Systems-Pharmacology/MoBi/issues/485)
* [Container criteria "in container" only applies for the children of the container](https://github.com/Open-Systems-Pharmacology/MoBi/issues/523)
* [Molecule keyword replacement does not work for global parameter referencing other global molecule parameters](https://github.com/Open-Systems-Pharmacology/OSPSuite.Core/issues/832)
* [Drag and drop of parameter to the "references area" does not work](https://github.com/Open-Systems-Pharmacology/MoBi/issues/507)

### PK-Sim and MoBi

* [PI Corrupted when referencing a process parameter that is removed from the simulation](https://github.com/Open-Systems-Pharmacology/OSPSuite.Core/issues/497)
* [Parameter  Identification: When User close and reopen the PI the results section  shown the new boundaries and not those used in the PI run](https://github.com/Open-Systems-Pharmacology/OSPSuite.Core/issues/818)

