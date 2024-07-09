# IBM-MBQC

## Requirements
- Python3 environment with the following libraries:
    - numpy
    - matplotlib
    - scipy
    - sympy
    - json
    - datetime
    - qiskit
    - qiskit_aer
    - qiskit_ibm_runtime
    - mthree
    - qiskit_ibm_provider (deprecated, needed for some analysis of older data)
- Access to a device with $\geq 11$ qubits (for running experiments)

## Navigating experimental data

### VQE
- 8 jobs of 250 circuits, 5k shots
- Qubits used: [2, 64, 105, 12, 13, 27, 28, 40, 41, 116, 117]
- M3 measurement calibration matrices in `calibrations/VQE_cals_0326.json`
- Full IBM calibration data in `calibrations/VQE_IBM_calibrations.json` (all jobs)
- Raw results in `raw_data/VQE_(jobname).json` files
    - ["cr1xfmyk5z70008951qg", "cr1xm9s8gdp0008g3qj0", "cr1xs4mk5z7000895520", "cr1xwn2dvs8g008jdt0g", "cr1y0yvk5z70008957y0", "cr1y6ehdvs8g008jdvz0", "cr1y9d5s9z7g008dyjjg", "cr1ycr3s9z7g008dyk80"]
- Processed results in `processed_data/VQE_(...).npz` files
- Circuit construction/running and data processing/visualization in `vqe.ipynb`

### COP Measurements
- 8 jobs of 180 circuits, 10k shots
- Qubits used: [9, 8, 16, 26, 25]
- Full IBM calibration data in `calibrations/COP_IBM_calibrations_.json` (all jobs)
- Raw results in `raw_data/COP_(jobname).json` files
    - ["csk5tvvea560008f5yrg", "csk5vhpvnxy0008d3kgg", "csk5w7gea560008f5yw0", "csk5wxk1k2e0008nw9f0", "csk5xkpea560008f5z00", "csk5yah1k2e0008nw9p0", "csk5z14p1vzg008a1sdg", "csk5zqpvwqp0008as4s0"]
- Processed results in `processed_data/COP_(...).npz` files
- Circuit construction/running and data processing/visualization in `sopcop.ipynb`

### Divide and Conquer
#### Coarse
- 3 jobs of 288 circuits, 10k shots
- Qubits used: [10, 11, 12, 17, 30, 31, 32, 36, 51]
- Full IBM calibration data in `calibrations/DaC_coarse_IBM_calibrations.json` (all jobs)
- Raw results in `raw_data/DaC_coarse_(jobname).json` files
    - ["csn2qfnea560008fdmm0", "csn2rn2ea560008fdmsg", "csn2st7vwqp0008b0jpg"]
- Processed results in `processed_data/DaC_(...).npz` files
- Circuit construction/running and data processing/visualization in `divideandconquer.ipynb`

#### Fine
- 20 jobs of 288 circuits, 10k shots
- Qubits used: [10, 11, 12, 17, 30, 31, 32, 36, 51]
- Full IBM calibration data in `calibrations/DaC_fine_IBM_calibrations_1/2/3/4/5.json`
- Raw results in `raw_data/DaC_fine_(jobname).json` files
    - ["csn2v0mvnxy0008dba60", "csn2w91ea560008fdngg", "csn2xdnvnxy0008dbakg", "csn2yja0c2pg008bze8g", "csn2zqpea560008fdp70", "csn30ybvwqp0008b0kxg", "csn3248vwqp0008b0m60", "csn33bn0c2pg008bzfag", "csn34gtvwqp0008b0mh0", "csn35myea560008fdqcg", "csn36vbvnxy0008dbc5g", "csn38180c2pg008bzg5g", "csn39850c2pg008bzg8g", "csn3aehvnxy0008dbcmg", "csn3bky1k2e0008p4350", "csn3crvvwqp0008b0ncg", "csn3dyq0c2pg008bzgzg", "csn3f3wp1vzg008a9js0", "csn3gas0c2pg008bzhf0", "csn3hheea560008fdrvg", "csn3jrv0c2pg008bzhq0", "csn3kzf1k2e0008p445g", "csn3n64p1vzg008a9kh0", "csn3pe9vnxy0008dbe80", "csn3qrzp1vzg008a9kz0", "csn3rzvvnxy0008dberg", "csn3t5gvwqp0008b0qcg", "csn3vbn0c2pg008bzkyg", "csn3wha0c2pg008bzm5g", "csn3xppp1vzg008a9n2g", "csn3ywkea560008fdvt0", "csn4020vwqp0008b0r8g", "csn417w1k2e0008p463g", "csn42dhea560008fdw80", "csn43m6vnxy0008dbftg", "csn44s3vnxy0008dbfyg", "csn460rp1vzg008a9ny0", "csn47851k2e0008p4710", "csn48dhvwqp0008b0sj0", "csn49je1k2e0008p47fg", "csn4as30c2pg008bzp2g", "csn4bzz0c2pg008bzpc0", "csn4d6wea560008fdxx0", "csn4ee1p1vzg008a9q6g", "csn4fnyvnxy0008dbh4g", "csn4gy30c2pg008bzq5g", "csn4j4gea560008fdyvg", "csn4kd51k2e0008p48vg", "csn4mn20c2pg008bzqy0", "csn4ntzvnxy0008dbj2g", "csn4q4wea560008fdzn0", "csn4rd11k2e0008p49c0", "csn4sjeea560008fe02g", "csn4tsb0c2pg008bzs00", "csn4w10vwqp0008b0vng", "csn4x74p1vzg008a9sh0", "csn4ycs1k2e0008p4abg", "csn4zjp1k2e0008p4ah0", "csn50rb1k2e0008p4amg", "csn51yf1k2e0008p4asg"]
    - First 40 have calibrations `1`, Next 20 have calibrations `2`.
- Processed results in `processed_data/DaC_(...).npz` files
- Circuit construction/running and data processing/visualization in `divideandconquer.ipynb`

### Counterintuitive Regime
#### String Order Parameters
- 6 jobs of 144/288 circuits, 10k shots
- Qubits used: [43, 44, 45, 46]
- Full IBM calibration data in `calibrations/CI_SOP_IBM_calibrations.json` (all jobs)
- Raw results in `raw_data/CI_SOP_(jobname).json` files
    - ["csxsrr3fhyd0008kak90", "csxsrrvyn5c0008bwmgg", "csxsrsbyn5c0008bwmhg", "csxt4k2faem0008wyp5g", "csxt4kje88ng008q6n8g", "csxt4ma8cwag008wpa1g"]
- Processed results in `processed_data/CI_SOPs.npz`
- Circuit construction/running and data processing/visualization in `counterintuitive-sops.ipynb`

#### Purities
- 60 jobs of 288 circuits, 10k shots
- Qubits used: [8, 9, 10, 11, 12, 17, 30, 31, 32, 36, 51]
- Full IBM calibration data in `calibrations/CI_IBM_calibrations_1/2/3/4/5.json`. 
- Raw results in `raw_data/CI_(jobname).json` files
    - ["csfkxm69as1g0081dacg", "csfkz4c9as1g0081dadg", "csfm0r30a9s0008e1x9g", "csfm29s6nagg008qdax0", "csfm3w76nagg008qdazg", "csfm5bx6nagg008qdb30", "csfm6yk6nagg008qdb8g", "csfm8jtpvsk0008rcnng", "csfma5r0a9s0008e1y40", "csfmbq6pvsk0008rcnr0", "csfmd7wbm6a0008970ng", "csfmept6nagg008qdc1g", "csfmg5rjm3kg008qzf4g", "csfmhpybm6a0008970yg", "csfmk7c6nagg008qdc70", "csfmmr39as1g0081dc6g", "csfmp91jm3kg008qzfc0", "csfmqsqpvsk0008rcpbg", "csfmsan6nagg008qdcgg", "csfmtv30a9s0008e1yy0", "csjd7j61k2e0008nr7t0", "csjd8vkea560008f2vb0", "csjda5g3fxq0008c2mt0", "csjdbexp1vzg0089ygx0", "csjdcrv3fxq0008c2n60", "csjde28vnxy0008czaw0", "csjdfbnvwqp0008anwh0", "csjdgn2vnxy0008czb0g", "csjdhyq1k2e0008nr89g", "csjdk85vnxy0008czb40", "csjdmj2p1vzg0089yhsg", "csjdntqvnxy0008czb80", "csjdq4cp1vzg0089yj2g", "csjdrd9p1vzg0089yjag", "csjdsny3fxq0008c2pc0", "csjdty3vnxy0008czbs0", "csjdw4gea560008f2wqg", "csjdxb53fxq0008c2q5g", "csjdykjp1vzg0089ykg0", "csjdzw7vnxy0008czcdg", "csjmh3c1k2e0008ns6s0", "csjmjr33fxq0008c3r6g", "csjmm993fxq0008c3sj0", "csjmnv73fxq0008c3tq0", "csjmqan3fxq0008c3w40", "csjmrsv3fxq0008c3xa0", "csjmt913fxq0008c3yv0", "csjmvpp3fxq0008c4090", "csjmx443fxq0008c41h0", "csjmyh23fxq0008c42tg", "csjmzzfvnxy0008d0re0", "csjn1e5vwqp0008aq0sg", "csjn2wbvwqp0008aq1zg", "csjn4asp1vzg0089zv6g", "csjn5sf1k2e0008nsstg", "csjn77wea560008f4650", "csjn8ptp1vzg0089zxfg", "csjna58p1vzg0089zxk0", "csjnbkp3fxq0008c4agg", "csjnd2cea560008f46tg", "csjxnt7p1vzg008a0krg", "csjxqp6vnxy0008d22h0", "csjxt503fxq0008c5dqg", "csjxw58vwqp0008aqtb0", "csjxyx33fxq0008c5e30", "csjy1nyp1vzg008a0m8g", "csjy3hep1vzg008a0mfg", "csjy574vwqp0008aqtwg", "csjy6wb1k2e0008ntx7g", "csjy8g2vwqp0008aqvn0", "csjya68p1vzg008a0nc0", "csjybxqvnxy0008d24eg", "csjydme1k2e0008ntxt0", "csjyfadvnxy0008d250g", "csjygzv1k2e0008nty40", "csjyjpap1vzg008a0phg", "csjymcs1k2e0008ntykg", "csjyp381k2e0008ntyr0", "csjyqqe1k2e0008ntz00", "csjysdnp1vzg008a0qe0"]
    - First 20 have calibrations `1`, next 20 have calibrations `2`, next 20 have calibrations `3`, final 20 have calibrations `4`.
- Processed results in `processed-data/CI_purities_(...).npz`
- Circuit construction/running and data processing/visualization in `counterintuitive.ipynb`