# EclipseCon France 2017 - Patching the gap in collaborating on model

Model Patch wiki page: https://wiki.eclipse.org/EMF_DiffMerge/Model_Patch

ECF 2017 session: https://www.eclipsecon.org/france2017/session/patching-gap-collaborating-models (slides attached)

## How to try the demo

1. Download Capella Studio 1.1.1 from the [Capella page](https://polarsys.org/capella/download.html) and unzip it
1. Start an Eclipse IDE (not the Capella Studio!) with EMF SDK installed (e.g. Modeling EPP)
1. Create a new target platform (Select Nothing on the first page)
   * Add the Capella Studio installation to the target platform
   * Add the [Orbit-R20140525021250](http://download.eclipse.org/tools/orbit/downloads/drops/R20140525021250/repository) site to the target platform
      * Select Google GSON ang Google GSON Source bundles
1. Import the following projects to your workspace:
   * From [VIATRA repo](https://git.eclipse.org/r/#/admin/projects/viatra/org.eclipse.viatra)
      * /org.eclipse.viatra.query.runtime
      * /org.eclipse.viatra.query.runtime.base
      * /org.eclipse.viatra.query.runtime.base.itc
      * /org.eclipse.viatra.query.runtime.matchers
      * /org.eclipse.viatra.query.runtime.rete
      * /org.eclipse.viatra.query.runtime.rete.recipes
      * /org.eclipse.viatra.transformation.evm
      * /org.eclipse.viatra.transformation.runtime.emf
   * From [EMF Diff/Merge repo](https://git.eclipse.org/r/#/admin/projects/diffmerge/org.eclipse.emf.diffmerge.core)
      * /org.eclipse.emf.diffmerge
      * /org.eclipse.emf.diffmerge.connector.core
      * /org.eclipse.emf.diffmerge.connector.git
      * /org.eclipse.emf.diffmerge.gmf  
      * /org.eclipse.emf.diffmerge.sirius
      * /org.eclipse.emf.diffmerge.ui
      * /org.eclipse.emf.diffmerge.ui.gmf
      * /org.eclipse.emf.diffmerge.ui.sirius
   * From [Model Patches repo](https://git.eclipse.org/r/#/admin/projects/diffmerge/org.eclipse.emf.diffmerge.patch)
      * /org.eclipse.emf.diffmerge.patch
      * /org.eclipse.emf.diffmerge.patch.persistence.emf
      * /org.eclipse.emf.diffmerge.patch.persistence.emf.edit
      * /org.eclipse.emf.diffmerge.patch.persistence.json
      * /org.eclipse.emf.diffmerge.patch.root
      * /org.eclipse.emf.diffmerge.patch.runtime
      * /org.eclipse.emf.diffmerge.patch.ui
   * From [Capella repo](https://git.polarsys.org/r/#/admin/projects/capella/capella)
      * /core/plugins/org.polarsys.capella.core.compare
1. Open org.eclipse.viatra.query.runtime.rete.recipes/model/rete-recipes.genmodel and Generate Model code
1. Don't worry about the API tools errors on VIATRA projects
1. Start a runtime eclipse
1. Import the projects in this repository
1. Switch to the Capella perspective
