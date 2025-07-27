# Suggestions Extraction Results

## EXTRACTED_SUGGESTIONS

**Item 1:**
- Title: Cross-Platform and Language Evaluation  
- Content: Extend the empirical study to include projects in other programming languages (e.g., JavaScript, Go) and CI systems (e.g., Jenkins, CircleCI). This would test LWD’s adaptability to different build tools, dependency management practices, and commit patterns, and could inform generalized CI-Skip rule sets beyond Java artifacts.  
- Source: Response 1

**Item 2:**
- Title: Dynamic Parameter Tuning Mechanisms  
- Content: Investigate automated, feedback-driven methods for adjusting LWD’s factor, retention limit, and fallback threshold during operation. For instance, integrate a lightweight online monitoring component that analyzes recent failure patterns to recalibrate parameters, potentially improving build savings over static experimental values.  
- Source: Response 1

**Item 3:**
- Title: Integration with Resource Consumption Metrics  
- Content: Enhance the build simulator to collect and analyze CPU utilization, memory usage, and energy consumption per build. By coupling LWD decisions with multi-dimensional resource metrics rather than solely build counts, future work can optimize batching strategies for holistic CI cost reduction—aligning scheduling decisions with real infrastructure constraints.  
- Source: Response 1

**Item 4:**
- Title: Explore Adaptive LWD Parameter Tuning  
- Content: Future research should investigate adaptive strategies for tuning LWD parameters dynamically based on project characteristics and build history. Instead of relying on fixed values for parameters like retention limit, fallback limit, and factor values, the system could automatically adjust these parameters based on performance metrics such as build success rate, build duration, and resource utilization. Machine learning techniques, such as reinforcement learning, could be employed to learn optimal parameter configurations for different project profiles and CI environments. This adaptive approach could further improve the efficiency and effectiveness of LWD by tailoring it to the specific needs of each project.  
- Source: Response 2

**Item 5:**
- Title: Investigate Language-Specific CI-Skip Rules and Their Integration with LWD  
- Content: Given the limited impact of the existing CI-Skip rules, future work should explore the development and integration of language-specific CI-Skip rules that are tailored to the characteristics of different programming languages and build tools. For example, CI-Skip rules for Python projects could focus on changes to documentation or whitespace, while rules for C++ projects could target header file modifications. Furthermore, research should investigate alternative strategies for combining CI-Skip rules with LWD that could lead to more significant build savings. For example, CI-Skip rules could be applied selectively based on the current batch size or build history.  
- Source: Response 2

**Item 6:**
- Title: Evaluate LWD in Diverse CI/CD Environments  
- Content: Future research should evaluate the performance of LWD in a wider range of CI/CD environments, including proprietary projects, cloud-based CI platforms (e.g., GitHub Actions, GitLab CI), and containerized build environments (e.g., Docker, Kubernetes). This would involve collecting data on build outcomes, resource consumption, and cost factors from diverse projects and CI/CD configurations. The results of these evaluations could provide valuable insights into the generalizability of LWD and identify potential areas for improvement. In particular, it would be beneficial to investigate how LWD performs in environments with highly variable build durations or resource constraints.  
- Source: Response 2

**Item 7:**
- Title: Evaluate on Diverse Languages and Project Scales  
- Content: Future work could extend LWD evaluation to non-Java projects (e.g., Python or C++) and smaller or proprietary repositories using datasets like GitHub Actions or Jenkins logs. This would assess generalizability, potentially revealing language-specific optimizations (e.g., adapting CI-Skip rules), and add value by providing broader evidence for LWD's effectiveness, addressing the current Java-centric bias.  
- Source: Response 3

**Item 8:**
- Title: Develop Adaptive Parameter Optimization Mechanisms  
- Content: Researchers could investigate machine learning or heuristic-based methods to dynamically tune LWD parameters (e.g., factors or thresholds) in real-time based on ongoing build metrics, rather than fixed values like factor 2 for exponential variants. This feasible extension, building on the customizability rule, would enhance performance during varying project phases, offering value through automated, context-aware batching that maximizes savings without manual intervention.  
- Source: Response 3

**Item 9:**
- Title: Analyze Broader Resource Impacts Beyond Builds  
- Content: A deeper study could measure LWD's effects on energy consumption and CPU usage using real CI hardware traces, comparing against baselines with precise metrics (e.g., integrating power profiling tools). This would address the metric limitation by quantifying holistic savings, providing valuable insights for sustainable CI practices in resource-constrained environments like cloud-based systems.  
- Source: Response 3

**Item 10:**
- Title: Cross-Language and Tool Evaluation of LWD  
- Content: The paper’s focus on Java and TravisCI necessitates validation across diverse programming ecosystems (e.g., Python, C++) and modern CI platforms (e.g., GitHub Actions). For instance, projects with different build failure patterns (e.g., machine learning repositories with frequent dependency changes) might benefit differently from LWD’s local feedback loop. This research direction aligns with the authors’ own future work proposals and would strengthen external validity by testing whether LWD’s principles—reliance on recent batch outcomes—are universally applicable or language/tool-specific.  
- Source: Response 4

**Item 11:**
- Title: Comprehensive Resource Efficiency Analysis  
- Content: Future studies should quantify LWD’s impact on wall-clock time, energy consumption, and compute resource utilization, not just build counts. The current wall-clock time analysis was limited to 41 projects and used approximations (e.g., batch duration = last commit’s build time), which may misrepresent parallelized CI systems where batch builds run faster than individual ones. A deeper analysis could leverage resource profiling tools to measure CPU/memory usage or model energy costs, as suggested in the paper’s future work, providing a holistic view of LWD’s value in resource-constrained environments.  
- Source: Response 4

**Item 12:**
- Title: Adaptive Hybridization of Batching and CI-Skip Strategies  
- Content: The paper’s CI-Skip integration applied skippable commit filtering before batching, but the limited gains (0.87% median) suggest a need for more nuanced combinations. Future work could explore dynamic prioritization: for instance, allowing CI-Skip rules to influence batching granularity (e.g., larger batches for skippable commits, smaller batches for non-skippable ones). Alternatively, integrating CI-Skip into fallback algorithms (e.g., skipping rebuilds for documentation-only commits during bisection) might amplify savings. This direction aligns with the authors’ call for enhanced CI-Skip integration and could bridge the observed gap in combined batching–CI-Skip performance.  
- Source: Response 4