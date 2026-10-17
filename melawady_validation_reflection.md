# Validation Reflection — melawady

I validated mjohn326's ten MiniProject2 projects, and she validated mine. Of the 100 records we compared, 93 agreed before discussion and all 100 agreed after. Agreement differed a lot by field. CurrentStatus and WhyRecovered agreed completely: CurrentStatus is a mechanical rule (any commit after 2025-04-01), and for WhyRecovered we accepted each other's reasons when they matched the commits. HasRecovered (90%, κ = 0.62 before discussion) and especially ActivityPattern (80%, κ = 0.73) were where we disagreed. Four of the seven disagreements were about ActivityPattern, which is the most subjective label in the coding guide.

The adjudicated labels show a few patterns. Long gaps were usually preceded by maintenance work rather than abandonment. Before their gaps, projects such as falkon, tinfour and pyhsmm were doing bug fixes, dependency bumps and release preparation, so the gap looks like "the software works, nothing urgent to do" rather than a failure. Recovery had three typical triggers:
- the original maintainer returning for a rewrite or a new version (Manopt.jl in 2018, pyvinecopulib re-initialized as Python bindings in 2019, IB2d in 2024);
- outside pressure from users through issues and PRs (tinfour's "Issue 84/89/96" commits, xrt answering issues #176–#180, nmslib's outside PRs);
- breakage in dependencies or CI that forced a maintenance release (falkon's July 2025 burst after a KeOps change).

Gaps also often did not mean the project had died. elfi, Manopt.jl and pyvinecopulib each had multi-month gaps and then hundreds or thousands more commits. The opposite case also exists: pyhsmm had commits after its 26-month gap, but the only real one added a README notice saying the package is no longer maintained.

The main interpretation pitfalls were:
- treating any post-gap commit as recovery without reading it (pyhsmm);
- recording a value that contradicts the numbers (elfi marked "not recovered" with 1,132 later commits);
- underweighting long-term trends. On my own projects, I labeled CARTA as steady and pytorch/audio as irregular because recent years looked flat or bounced back. My teammate pointed out that both sit far below their 2021 peaks, and I accepted *declining*. MUMmer, which I had called irregular, shows a repeating fall uptick, so we recorded it as cyclical;
- using labels outside the codebook ("seasonal" had to be mapped to cyclical).

Most of these were resolved by comparing yearly commit counts against the plot rather than relying on our first impression. RecentThemes had a smaller version of the same problem: merge and build-configuration commits can reasonably be read as "Other" or as documentation and maintenance work, and for nmslib we settled on Bug fixes:Documentation updates.

For future coding I would make two changes: write WhyRecovered as a cause backed by a commit quote rather than a date or "not sure", and add yearly counts next to every ActivityPattern label. Most of our disagreements came from vague reasons and from reading plot shapes, and all seven were easy to settle once we looked at the numbers together.
