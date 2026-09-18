# Field Workstation and Software

## Community Frequency — Peru 2026 Field Research

**Status:** Prepared for Phase 0 field research
**Platform:** ASUS X556UAK
**Operating System:** Ubuntu 26.04.1 LTS
**Architecture:** x86-64
**Purpose:** Portable field workstation for communications, RF, GPS/GNSS, sensor, mapping, data collection, and analysis.

---

## 1. Workstation

The field workstation is an ASUS X556UAK laptop prepared as a portable research and data-analysis platform for Community Frequency field work.

Current system baseline:

- CPU platform: x86-64
- RAM: approximately 8 GB usable
- Storage: approximately 240 GB SSD
- Firmware: X556UAK.317
- Boot mode: UEFI/GPT
- Ubuntu: 26.04.1 LTS
- Kernel: Linux 7.0.0-31-generic

The laptop is intended to remain a general-purpose research workstation rather than a dedicated single-purpose radio computer.

---

## 2. Core Development and Data Tools

Installed software includes:

- Git
- Python 3
- SQLite
- jq
- ripgrep
- tree
- rsync
- zip / unzip

Python environments are kept separate where appropriate.

The primary Community Frequency Python environment is:



An isolated ESP32/PlatformIO environment is maintained at:



---

## 3. Meshtastic

The Meshtastic Python CLI is installed in the Community Frequency research environment.

Current version:



The workstation is prepared for USB and serial communication with field radios.

Serial-device permissions include the  and  groups.

No field radio configuration is changed merely by connecting the workstation. Initial hardware inspection should be read-only whenever possible.

---

## 4. MeshCore

MeshCore CLI is installed separately using usage: pipx [-h] [--quiet] [--verbose] [--global] [--version]
            {install,install-all,uninject,inject,pin,unpin,upgrade,upgrade-all,upgrade-shared,uninstall,uninstall-all,reinstall,reinstall-all,list,interpreter,run,runpip,ensurepath,environment,completions} ...

Install and execute apps from Python packages.

Binaries can either be installed globally into isolated Virtual Environments
or run directly in a temporary Virtual Environment.

Virtual Environment location is /home/renato/.local/share/pipx/venvs.
Symlinks to apps are placed in /home/renato/.local/bin.
Symlinks to manual pages are placed in /home/renato/.local/share/man.

optional environment variables:
  PIPX_HOME              Overrides default pipx location. Virtual Environments
                        will be installed to $PIPX_HOME/venvs.
  PIPX_GLOBAL_HOME       Used instead of PIPX_HOME when the `--global` option
                        is given.
  PIPX_BIN_DIR           Overrides location of app installations. Apps are
                        symlinked or copied here.
  PIPX_GLOBAL_BIN_DIR    Used instead of PIPX_BIN_DIR when the `--global`
                        option is given.
  PIPX_MAN_DIR           Overrides location of manual pages installations.
                        Manual pages are symlinked or copied here.
  PIPX_GLOBAL_MAN_DIR    Used instead of PIPX_MAN_DIR when the `--global`
                        option is given.
  PIPX_DEFAULT_PYTHON    Overrides default python used for commands.
  PIPX_USE_EMOJI         Overrides emoji behavior. Default value varies based
                        on platform.
  PIPX_HOME_ALLOW_SPACE  Overrides default warning on spaces in the home path

options:
  -h, --help            show this help message and exit
  --quiet, -q           Give less output. May be used multiple times
                        corresponding to the ERROR and CRITICAL logging
                        levels. The count maxes out at 2.
  --verbose, -v         Give more output. May be used multiple times
                        corresponding to the INFO, DEBUG and NOTSET logging
                        levels. The count maxes out at 3.
  --global              Perform action globally for all users.
  --version             Print version and exit

subcommands:
  Get help for commands with pipx COMMAND --help

  {install,install-all,uninject,inject,pin,unpin,upgrade,upgrade-all,upgrade-shared,uninstall,uninstall-all,reinstall,reinstall-all,list,interpreter,run,runpip,ensurepath,environment,completions}
    install             Install a package
    install-all         Install all packages
    uninject            Uninstall injected packages from an existing Virtual
                        Environment
    inject              Install packages into an existing Virtual Environment
    pin                 Pin the specified package to prevent it from being
                        upgraded
    unpin               Unpin the specified package
    upgrade             Upgrade a package
    upgrade-all         Upgrade all packages. Runs `pip install -U <pkgname>`
                        for each package.
    upgrade-shared      Upgrade shared libraries.
    uninstall           Uninstall a package
    uninstall-all       Uninstall all packages
    reinstall           Reinstall a package
    reinstall-all       Reinstall all packages
    list                List installed packages
    interpreter         Interact with interpreters managed by pipx
    run                 Download the latest version of a package to a
                        temporary virtual environment, then run an app from
                        it. Also compatible with local `__pypackages__`
                        directory (experimental).
    runpip              Run pip in an existing pipx-managed Virtual
                        Environment
    ensurepath          Ensure directories necessary for pipx operation are in
                        your PATH environment variable.
    environment         Print a list of environment variables and paths used
                        by pipx.
    completions         Print instructions on enabling shell completions for
                        pipx.

Current version:



The MeshCore workflow is maintained as a separate research track from Meshtastic.

The project does not assume in advance that either platform is the final solution. Field evidence will determine whether and where each technology is useful.

---

## 5. ESP32 Development

PlatformIO is installed for ESP32 development and sensor prototyping.

Current baseline:

- PlatformIO: 6.2.0
- Espressif32 platform: 7.1.3
- esptool: 4.11.0

A basic ESP32 test project has been successfully built.

An ESP32-C3 test board has also been detected and successfully programmed. Serial-console behavior is still being investigated separately from the field-radio workflow.

ESP32 development is intended primarily for sensor and experimental telemetry work.

---

## 6. RF and SDR Tools

Installed RF-related software includes:

- Wireshark
- RTL-SDR utilities
- GQRX
- tcpdump
- Nmap
- iperf3
- mtr
- arp-scan
- iw
- traceroute
- netcat

Wireshark non-superuser packet capture has been enabled.

An RTL-SDR is available for field RF observation. The SDR is treated as an observation instrument rather than a substitute for the Meshtastic/MeshCore radios.

---

## 7. GPS/GNSS

Installed GPS/GNSS software includes:

- GPSD
- cgps
- GPSBabel

The workstation is prepared to ingest GPS/GNSS data for field observations, tracks, and waypoint collection.

GPSD is not permanently attached to a serial device until the specific field receiver is identified. This avoids unnecessary conflicts with radio and USB serial devices.

---

## 8. GIS and Offline Mapping

Installed GIS and geospatial tools include:

- QGIS
- GDAL
- PROJ
- GEOS
- SpatiaLite
- osmium

The workstation supports offline preparation and analysis of:

- OpenStreetMap data
- roads and access routes
- settlements
- waterways
- infrastructure
- terrain/elevation
- slope
- hillshade
- GPS tracks
- field sites
- RF observations
- sensor observations

Large mapping datasets remain outside the public Git repository.

---

## 9. Field Data Organization

The working field-data environment is maintained separately from the public source repository:



The workspace includes dedicated areas for:

- experiments
- field notes
- raw data
- processed data
- Meshtastic
- MeshCore
- SDR observations
- GPS/GNSS
- sensors
- photos
- exports
- maps

Raw evidence should be preserved before processing or filtering whenever practical.

---

## 10. Research Data Principle

The workstation is configured around the Community Frequency research principle:

> Research the need. Test the technology. Let the evidence shape the solution.

The technical workflow is:

**Research → Test → Observe → Document → Learn → Decide**

The workstation therefore supports multiple observation and communications technologies rather than assuming a predetermined deployment architecture.

---

## 11. Field Readiness

The workstation is intended to support the following Phase 0 activities:

1. Prepare and inspect field radios.
2. Collect GPS/GNSS observations.
3. Conduct Meshtastic and MeshCore experiments.
4. Record packet and message behavior.
5. Perform RF observations with SDR equipment.
6. Collect environmental and sensor data.
7. Record routes, locations, terrain, and access conditions.
8. Maintain experiment records.
9. Preserve raw evidence.
10. Produce maps, tables, and research reports.

This workstation configuration is a preparation baseline. Individual field equipment and software configurations should be documented as they are introduced.

---

## 12. Reproducibility

The public repository documents the methodology and software environment.

Large datasets, raw captures, generated raster products, local virtual environments, and machine-specific operational files remain outside the public repository.

This separation keeps the public project lightweight while preserving the ability to reproduce the processing workflow from documented source data and commands.

**Last updated:** September 2026
