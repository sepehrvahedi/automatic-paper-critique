# Limitations Extraction Results

## EXTRACTED_LIMITATIONS

**Item 1:**
- Title: Limited Cost Metrics  
- Content: The study’s primary metric—percentage of builds saved—does not directly quantify real CI costs such as compute time, energy consumption, or resource utilization. While wall-clock time estimates were computed for 41 projects, these relied on approximating batch build duration by the last commit’s time plus bisection overhead, which may misrepresent actual CI savings and could affect conclusions on time efficiency.  
- Source: Response 1

**Item 2:**
- Title: Narrow Dataset and Tooling Scope  
- Content: By focusing exclusively on large, Java-based open-source projects using TravisCI (with ≥2,000 commits), the findings may not generalize to smaller or proprietary codebases, other programming languages, or alternative CI platforms (e.g., Jenkins, GitHub Actions). The specificity of CI-Skip rules to Java also limits applicability, as skip heuristics may differ across ecosystems.  
- Source: Response 1

**Item 3:**
- Title: Single-Author Implementation Risk  
- Content: All simulation, data analysis, and scripting were performed by a single author, exposing the study to potential human error or bias. Although the authors mitigated this by reusing prior replication packages, a multi-researcher validation or independent reimplementation would strengthen internal validity.  
- Source: Response 1

**Item 4:**
- Title: Limited Generalizability Due to Dataset Specificity  
- Content: The study’s focus on Java-based projects sourced from a specific TravisTorrent data dump (January 25, 2017) and filtered for projects with over 2,000 commits presents a significant limitation to the generalizability of the results. The LWD approach was tailored around Java CI-Skip rules. The paper acknowledges that these Java-specific rules may not translate directly to other languages. Furthermore, the restriction to large, open-source projects might not accurately reflect the characteristics and build patterns of smaller projects or proprietary codebases, which could exhibit different commit frequencies, failure rates, and build complexities.  
- Source: Response 2

**Item 5:**
- Title: Reliance on “Percentage of Builds Saved” as the Primary Metric  
- Content: While the "percentage of builds saved" is a useful metric for quantifying the reduction in CI build scheduling, it does not fully capture the overall cost savings associated with different batching techniques. The paper acknowledges that this metric does not directly represent the time, computing resources, or energy conserved. Although the authors estimated wall-clock time saved for a subset of the projects, this estimation relied on simplifying assumptions (e.g., approximating batch build duration based on the last commit's time), potentially introducing inaccuracies. A more comprehensive cost analysis, considering factors such as CPU utilization, memory consumption, and energy usage, would provide a more holistic assessment of the economic benefits of LWD.  
- Source: Response 2

**Item 6:**
- Title: Lack of Significant Improvement with CI-Skip Integration  
- Content: The study’s finding that the addition of CI-Skip rules to dynamic batching techniques (both LWD and baseline dynamic) did not result in significant additional build savings raises concerns about the effectiveness of this integration strategy. While CI-Skip rules alone did save a median of 5.51% of builds, their combination with batching only added a median of 0.87% to the savings. This suggests that the benefits of CI-Skip rules are largely redundant when combined with dynamic batching. This warrants further investigation into alternative approaches for integrating commit-skipping techniques with batching or a deeper understanding of why the current integration method is not more effective. It questions the added complexity of combining the techniques.  
- Source: Response 2

**Item 7:**
- Title: Restricted Dataset Generalizability  
- Content: The study is confined to 50 large, open-source Java projects from TravisTorrent (filtered to >2,000 commits, master branch), with failure rates from 5.84% to 98.32%. This focus limits external validity, as results may not extend to smaller projects, non-Java languages, proprietary codebases, or other CI tools beyond TravisCI. For instance, CI-Skip rules are Java-specific, potentially skewing the finding of minimal additional savings (0.87%) when combined with batching, which matters because it could misrepresent LWD's performance in diverse ecosystems.  
- Source: Response 3

**Item 8:**
- Title: Incomplete Resource Cost Metrics  
- Content: The primary metric, percentage of builds saved (e.g., LWD's median 37.38%–48.86%), does not fully capture time, energy, or computing costs; wall-clock time estimates were approximated for only 41 projects (using last commit duration plus bisection), introducing inaccuracies. This weakness is significant, as the paper notes baseline dynamic batching sometimes saves more time despite equivalent build savings, potentially leading to overstated benefits if organizations prioritize runtime over build count.  
- Source: Response 3

**Item 9:**
- Title: Potential Bias from Single-Author Implementation  
- Content: All simulation, data processing, and analysis were conducted by one author, raising internal validity risks like human error or bias in scripts, despite mitigation via prior replication packages. This could affect reliability of results, such as variant comparisons (e.g., Linear-4 BatchStop4's top performance at 45.57% median savings), and matters because it undermines confidence in the empirical claims without multi-author verification or automated checks.  
- Source: Response 3

**Item 10:**
- Title: Restricted Dataset Scope Limits Generalizability  
- Content: The study focuses exclusively on Java-based, large open-source projects with ≥2,000 commits, filtered from the TravisTorrent dataset (2017 release). While this ensures consistency with CI-Skip rules optimized for Java, it raises concerns about external validity. For example, projects in languages requiring stricter build dependencies (e.g., C++) or those using CI tools like Jenkins or GitHub Actions may exhibit different batching behaviors. The exclusion of smaller projects (n < 2,000 commits) further limits insights into LWD’s performance in early-stage or low-activity repositories. The authors acknowledge this in Section 6, noting that proprietary projects or non-Java ecosystems might yield divergent results, but no cross-language or industry validation is provided.  
- Source: Response 4

**Item 11:**
- Title: Over-Reliance on “Builds Saved” as a Proxy Metric  
- Content: The primary evaluation metric—“percentage of builds saved” compared to TestAll—omits critical real-world cost dimensions like wall-clock time, energy consumption, or developer wait times. While the authors attempt to estimate time savings for 41 projects, their approximation assumes batch durations equal the time of the last commit plus bisection overhead, which may not account for parallelized testing or dependencies between commits. For instance, LWD BatchBisect variants saved 10.71% more builds than static batching but did not guarantee faster feedback loops: the baseline dynamic batching algorithm sometimes outperformed LWD in wall-clock time savings (e.g., with BatchBisect). This gap leaves unanswered whether LWD’s build reductions translate into tangible operational cost savings for CI systems.  
- Source: Response 4

**Item 12:**
- Title: CI-Skip Integration Offers Marginal Gains  
- Content: The paper’s exploration of CI-Skip rules—a technique to skip builds for low-risk commits—reveals limited synergy with dynamic batching. While CI-Skip alone saves 5.51% of builds, combining it with LWD or state-of-the-art dynamic batching adds only 0.87% median savings. This suggests that dynamic batching primarily optimizes failure scenarios, where CI-Skip is inapplicable (since it targets successful commits). The authors attribute this to batching’s focus on reducing overhead during failure streaks, but the lack of deeper analysis into complementary commit-skipping strategies (e.g., machine learning-based skip rules) or alternative integration approaches (e.g., post-batching skipping) weakens the paper’s contribution to holistic CI optimization.  
- Source: Response 4