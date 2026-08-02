# AeroBlade 2.1.3 third-party notices

This notice applies to the official Windows x64 portable distribution. It does
not change the proprietary license of the AeroBlade-owned application code,
interface, documentation, or branding. Each third-party component remains
available under its own terms. Full license texts and the dependency
report are distributed in the `LICENSES` directory.

## Python runtime

The portable package contains CPython and standard-library/runtime files.
Python is Copyright © Python Software Foundation and other contributors and is
distributed under the Python Software Foundation License and the additional
notices reproduced in `LICENSES/PYTHON-LICENSE.txt`.

## Qt for Python: PySide6 and Shiboken6

The graphical interface uses the official Qt for Python bindings and dynamically
loaded Qt libraries. The release is prepared under the GNU Lesser General Public
License version 3 option for these unmodified libraries. The application does
not statically link Qt. The libraries remain separate DLL/PYD files in
`_internal/PySide6` and can be replaced by a technically compatible build.

The proprietary AeroBlade license does not prohibit reverse engineering where
it is necessary to debug a modification to an LGPL-covered component. The full
LGPLv3 text is included in `LICENSES/LGPL-3.0.txt`.

Qt modules that are unnecessary for AeroBlade and available only under GPL or a
commercial Qt license are excluded from the final package. In particular,
`Qt6VirtualKeyboard.dll` and its platform-input-context plugin must not be
present in an academic/proprietary AeroBlade release.

Qt and Qt for Python are Copyright © The Qt Company Ltd. and their contributors.
Official licensing information: https://doc.qt.io/qt-6/licensing.html and
https://doc.qt.io/qtforpython-6/.

## NumPy, Matplotlib and transitive Python packages

AeroBlade uses NumPy and Matplotlib together with transitive runtime packages
selected by the isolated release environment. These components use permissive
open-source licenses and retain their respective copyright notices. The exact
resolved versions and license texts are recorded at build time in:

- `DEPENDENCIES.txt`
- `LICENSES/THIRD-PARTY-LICENSES.txt`
- the package-specific license files collected by PyInstaller

Matplotlib font resources retain the DejaVu and STIX notices included with the
Matplotlib distribution.

## PyInstaller

The portable application is assembled with PyInstaller. PyInstaller itself is
GPL-2.0-or-later with a special exception that permits building and distributing
non-free applications. Its license/exception text is included in
`LICENSES/PYINSTALLER-COPYING.txt`. PyInstaller is a build tool and does not
license the AeroBlade-owned program under the GPL.

## OpenSSL and Microsoft runtime libraries

Python/Qt networking support can cause OpenSSL runtime libraries to be collected
in the portable directory even though AeroBlade does not provide an online
service. OpenSSL 3 is licensed under Apache License 2.0; the license text is
included in `LICENSES/APACHE-2.0.txt`. Microsoft runtime libraries retain their
Microsoft terms and signatures where supplied by the platform/runtime package.

## XFOIL 6.99

AeroBlade bundles the unmodified Windows XFOIL 6.99 executable for local
two-dimensional airfoil analysis and launches it as a separate process. XFOIL
was created by Mark Drela and Harold Youngren and is licensed under the GNU
General Public License version 2 or later.

The portable release includes:

- the XFOIL GPL text in `LICENSES/XFOIL.txt`;
- the complete official XFOIL 6.99 source archive in
  `LICENSES/THIRD_PARTY_SOURCE/xfoil6.99.tgz`; and
- the upstream page at https://web.mit.edu/drela/OldFiles/Public/web/xfoil/.

The GPL applies to XFOIL, not to the independent AeroBlade application that
communicates with it through input/output files and a separate operating-system
process.

## QBlade reference boundary

QBlade Community Edition was used only as an engineering reference for model
families and expected steady-HAWT controls. No QBlade source file, library,
controller, image, interface asset, or executable is distributed with
AeroBlade. AeroBlade's implementations of published analytical equations are
independent. No numerical identity or endorsement by the QBlade team is claimed.

## License questions

The third-party report is an engineering compliance aid and should be
reviewed with the release manifest before publication. Questions about the
proprietary AeroBlade license or commercial use should be sent to
abdelhamid.bouhelal@g.enp.edu.dz.
