# Changelog
All notable changes to this tsn ref sw  will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

NOTE: The ChangeLog is only included in the release starting v0.8.22.
For prior version, please refer to the tag commit message. Sorry guys.

## [0.8.22] - 2022-02-09
- Support for kernel 5.1x in the scripts
- Changes json config to support EHL 2-port opcua functionalities
  for kernel 5.10 and above.
- Configuration changes for vs1 for EHl kernel 5.10 and above

## [0.8.23] - 2022-02-18
- missing configuration for rpl opcua-pkt1 is added.
- vs1x rpl default configuration is changed.
- added check for gnuplot availability.
- check for log folder availability. Force creation if missing.

## [0.8.24] - 2022-03-08
- TBS calculation (avg and stddev)
- Additional column for U2U latency stddev
- GCL/taprio configuration printout
- timesync stat printout upon ptp4l/phc2sys logs availability
- XDP opcua queue change to q3 for adl2 and rpl2

## [0.8.25] - 2022-04-19
- Add README_faq.md (for tips on errors etc)
- Update all the other readme-s
- Add default shell checking, set up vlan interface, fix syntax error

## [0.8.26] - 2022-05-12
- ISDM: add CODEOWNERS and pull_request_template.md
- ADL-N enablement
- Additional column for U2U coefficient variance
- Additional column for TBS coefficient variance

## [0.8.27] - 2022-06-13
- ADL-X vs1 iperf speed change

## [0.8.28] - 2022-08-19
- RPL-P enablement
- Install scrub/filter to the raw data
- Improve logic for manage systemctl restart

## [0.8.29] - 2022-09-02
- Update TODO.md
- Code refactoring on napi deferral's part to increase performance
  (smaller latency) for each difference kernels

## [0.8.30] - 2022-09-28
- ADL-N support for SKU5 that only has 2 cores
- Change default gPTP settings for ADL-N to TI-PHY
- Change default gPTP settings for RPL-P to TI-PHY
- Change systemctl try-reload-or-restart to restart

## [0.9.0] - 2022-11-03
- Add support for no_xdp and no_xdp_tbs mode
- Publish data on af_packet when af_xdp is not available in vs1
- Decoupling XDP_TBS related configuration from OPC-UA server code

## [0.9.1] - 2022-11-16
- Merge dependencies installer to master branch
- Update DEPENDENCIES.md and README_install.md

## [0.9.2] - 2022-11-18
- Bug fix for non_xdp mode
- Update the tx_timeout value for i225

## [0.9.3] - 2022-12-27
- Update requirements.txt
- Code refactoring to fix bug
- Update README.md and rename installer
- Update Shebang in all file with extension .sh

## [0.9.4] - 2023-1-17
- I225 Fix packet routing for AF_PACKET TBS

## [0.9.5] - 2023-2-21
- Remove 5 second interval in napi switch on/off to avoid
  extra latency.

## [0.9.6] - 2023-6-23
- ADL-N support on SKU5 that only has 2 cores for i225
- Update deprecated pthread function in TXRX-AFXDP test script
- Update deprecated bpf_xdp function in TXRX-AFXDP test script
- Refactor xdp cleanup routine

## [0.9.7] - 2023-7-17
- Refactor AF_XDP execution flow to support on kernel 6.* and above
- Fix syntax error in build.sh for Ubuntu
- Introduce new package installer
- Update README.md
- Add an exception handler for binary file checking

## [0.9.8] - 2023-8-10
- Add EHL support for TI-PHY
- txrx-tsn: Add extra flush packets in TX thread
- txrx-tsn: Tuning NAPI Deferral to improve performance

## [0.9.9] - 2023-9-5
- Update i225 OPCUA-PKT1 mapping
- Add eth flowtype proto rx filter to json

## [0.9.10] - 2023-10-9
- Code enhancement to ease code viewing and understanding

## [0.9.11] - 2023-11-8
- Update libbpf symbolic link in packages installer

## [0.9.12] - 2023-12-15
- Update script to run in bash to avoid unexpected output on Ubuntu
- Add preliminary ASL support

## [0.9.13] - 2024-02-07
- Automate core configuration settings for i225 and stmmac
- Automate core configuration settings for ASL platform
- Add Intel security policy and guideline
- Mount temp_file_dir directory to tmpfs

## [0.9.14] - 2024-08-26
- Change vlan socket priority value to be limited to 4 for both stmmac and i226
- Added support for proxy server input via command line option
- Fixed description of board information in OPCUA json script runner
- Add iperf3 and linuxptp debian packages as dependencies on package_installer.sh
- Added ethtool, iproute2 and ubuntu RT dependencies with links to required patches in README.md
- Added note clarifying the usage of <PLAT> command line argument in README_json.md

## [0.9.15] - 2025-01-10
- Enable feature that disable EEE before test execution
- Change command from lscpu to nproc to get CPU count
- Make plot persist after tsq1a exits
- Update liveplot to use replot
