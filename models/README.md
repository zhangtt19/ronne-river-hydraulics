# Model archive and four scenarios / 工程与四组情景

Download and extract [baseline-archive.zip](baseline-archive.zip). Open `toturial.prj` in a compatible HEC-RAS installation; the archived plan records version 6.70. Keep the extracted folder structure, including `condition1/` and `Terrain/`.

The saved flow file contains the baseline: Q = 100 m³/s and downstream known WSE = 0.5 m. All four reported scenarios used the same geometry; boundary values were changed between runs. Four separate historical project files were not required or retained.

| Scenario | Q at the existing flow-change locations (m³/s) | Downstream known WSE (m) |
|---|---:|---:|
| PF1 | 100 | 0.5 |
| PF2 | 100 | 1.0 |
| PF3 | 160 | 0.5 |
| PF4 | 160 | 1.0 |

Work on a copy. Preserve geometry, roughness and the subcritical regime. In steady-flow data, enter the chosen discharge at the existing flow-change locations and set the downstream known water level. Save each flow/plan under a distinct name, compute, and compare the two target sections and longitudinal profiles. Do not overwrite the archive when saving new runs.

原工程保存的是 PF1。其余情景通过修改同一基底的流量与下游水位完成；表格给出设置组合。分别保存计算方案后，可逐一比较 RS 2422、RS 7107 的水位、水深和流速。结果表来自原分析，并非本次新运行输出。

[manifest.json](manifest.json) records archive members and hashes. Archive extraction has been checked; opening and solving in HEC-RAS have not been retested for this release. Local layer paths may need relinking if a different installation cannot resolve them.
