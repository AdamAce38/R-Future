Pre-compiled binary packages for R-4.3.x for Windows
=====================================================

This collection is unsupported. Please compile from sources yourself 
in case of any problems. Please ask the package maintainer in case of 
any questions.

Building binary versions of the contributed packages on CRAN has been
automated. Binary packages will be available on CRAN about 1-3 days
after the sources have been published. Please do *not* submit binary
versions of any packages, because that needs manual intervention by
this collection's maintainer (hence it is time consuming).

Some packages have been working in a former version, but do no longer
compile on Windows or do not pass "R CMD check". The last `working'
versions are still available in the repository, but outdated.

Packages that do not compile out of the box or do not pass 
"R CMD check" with "OK" or at least a "WARNING" will *not* be
published. The results of "R CMD check" are given in
https://cran.r-project.org/web/checks/check_summary_by_package.html
In case of a "WARNING" or an "ERROR", please check the 
corresponding check.log files in subdirectory ./check.

Possible reasons for not-compiling or not-passing the checks:
 - I do not have some other software the package depends on
 - The package needs manual configuration
 - Any other reason I do not want to discover

Packages
	RWinEdt, caRpools, Rcplex
are checked with "--install:fake" for various reasons - most of them 
due to GUI interactions.

Packages
	ASMap, BASS, BIOMASS, BTYDplus, CFC, DClusterm, DLMtool, DOBAD, EML,
	Epi, FRK, GPareto, GPoM, HSAUR, HSAUR2, HSAUR3, HTSSIP,
	InformativeCensoring, NITPicker, PLmixed, PerformanceAnalytics,
	PortfolioAnalytics, PowerTOST, SCGLR, SamplingStrata, TSdata,
	TropFishR, adept, amen, argparse, babel, bdots, bunchr, caret,
	clustvarsel, copula, coxme, crawl, crmPack, crs, ctmm, ctsem,
	ctsemOMX, deBInfer, dendroTools, dismo, dtwSat, fitbitScraper,
	fxregime, gamlss.inf, glmmTMB, hetGP, icosa, ivmte, laGP, lolog,
	mboost, mcemGLM, merTools, metaRNASeq, micEconCES, misreport, mizer,
	mkin, morse, ndtv, netdiffuseR, ordinalgmifs, optparse, patchDVI,
	phylin, plotdap, pmc, psycho, psychomix, rentrez, skm, smooth,
	sommer, spikeSlabGAM, surveillance, tergm, tsna, twang, viridis,
	webshot
are checked with "--no-vignettes" due to their long-running checks 
or (for SHARE) non-reproducible vignette issues.

Packages
	ASMap, BIEN, BuyseTest, LatticeKrig, brms, climdex.pcic,
	clusternomics, ecd, ergm, np, personalized, restfulr,
	robCompositions, rstanarm, runjags, spatstat.core, symbolicDA, tgp
are checked with "--no-tests --no-examples --no-vignettes" due to 
their long-running checks, strange buffering issues, or due to other 
dependencies I do not have.

Some package are Unix only, including
	doMC, nice

Packages related to many database system must be linked to the exact 
version of the database system the user has installed, hence it does 
not make sense to provide binaries for packages
	ROracle, ora
although it is possible to install such packages from sources by
	install.packages('packagename', type='source')
after reading the manual 'R Installation and Administration'.

Packages
	OpenCL, ROI.plugin.cplex, Rcplex, cplexAPI
or their dependencies also require additional libraries / software to
build on Windows I do not have (and may not even exist in versions 
for Windows).

For some packages, additional third party libraries or programs are
required in your path, see the corresponding SystemRequirements statements 
in the DESCRIPTION files of those packages.
Please drop me a note for additional requirements we should make available 
on the build/check platform.

The toolchain used is Rtools43 <https://cran.r-project.org/bin/windows/Rtools/rtools43/rtools.html>.
That web page also links to the sources of third party components that may be included in binaries.

Uwe Ligges
Uwe.Ligges@R-project.org
