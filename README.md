# AeroBlade 2.1.3

**AeroBlade** is a portable Windows application for preliminary steady horizontal-axis wind-turbine aerodynamic analysis, blade design, optimization, power and energy estimation, and aerodynamic CAD export.

This public repository distributes the compiled application and its scientific documentation. AeroBlade source code is not included.

## Download

Download the portable archive from the [v2.1.3 release](https://github.com/Abdelhamid-Bouhelal/AeroBlade/releases/tag/v2.1.3), verify its SHA-256 checksum, extract the complete archive to a writable folder, and run `AeroBlade.exe`.

System requirement: 64-bit Windows 10 or Windows 11. Python is not required.

## Main capabilities

- NACA four- and five-digit airfoils and imported Selig/Lednicer coordinates
- XFOIL polar generation and import, Reynolds-family interpolation, and Viterna extrapolation
- Steady blade-element/momentum rotor analysis with documented correction models
- Variable-speed power curves, pitch regulation, and Weibull annual-energy estimates
- Glauert and Schmitz inverse design and constrained blade optimization
- NREL UAE Phase II and Phase VI rotor templates
- Three-dimensional aerodynamic blade loft and ASCII STL export
- Portable project files and engineering plots

## Verification and validation

The release passed 16 numerical and regression tests, packaged graphical-interface startup testing, bundled XFOIL startup testing, archive-integrity testing, and numerical validation studies. The Himmelskamp Phase VI comparison reported an RMSE of 1.203 kW, a mean-normalized RMSE of 17.70%, and R² = 0.851 for the documented zero-yaw, 72 rpm, 3°-pitch benchmark.

Read the [Verification and Validation Report](docs/AeroBlade-2.1.3-Verification-Validation-Report.pdf) before scientific use. The results define the tested scope; they do not constitute certification.

## Documentation

- [User Guide](docs/AeroBlade-2.1.3-User-Guide.pdf)
- [Verification and Validation Report](docs/AeroBlade-2.1.3-Verification-Validation-Report.pdf)
- [Release manifest](docs/AeroBlade-2.1.3-RELEASE-MANIFEST.json)
- [Build information](docs/AeroBlade-2.1.3-BUILD-INFO.txt)

## Scientific scope and limitations

AeroBlade supports preliminary steady, incompressible, axial-flow HAWT studies within the documented validation envelope. Deep stall, very low Reynolds number, yawed inflow, dynamic stall, strong turbulence, aeroelastic deformation, structural design, fatigue, acoustics, controls, certification, and safety assessment require suitable higher-fidelity methods and independent validation.

## License

AeroBlade is proprietary software distributed under the AeroBlade Academic and Research License v1.0. Version 2.1.3 may be used without charge for non-commercial research and teaching. Commercial, consultancy, paid-service, revenue-generating, and redistributed uses require prior written authorization. Third-party components retain their own licenses. See [LICENSE.txt](LICENSE.txt) and [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## Citation

Use the metadata in [CITATION.cff](CITATION.cff). The Zenodo DOI will be added after the archival record is published.

## Support

Scientific and support contact: [abdelhamid.bouhelal@g.enp.edu.dz](mailto:abdelhamid.bouhelal@g.enp.edu.dz). For reproducible problem reports, include the AeroBlade version, Windows version, steps, relevant inputs, expected result, observed result, and application log where available.
