GoldoreCore
GoldoreCore is the foundational software that connects to the GoldoreCoin peer-to-peer network. It enables the downloading and full validation of blocks and transactions. It includes a robust suite of functionalities including a wallet and a graphical user interface, which are optional components.

What is GoldoreCore?
GoldoreCore is an innovative adaptation of Bitcoin Core, customized for the GoldoreCoin network. Each block in the chain symbolizes a block of gold, emphasizing the rarity and value of the mined blocks, much like the real process of gold mining.

Mining Simulation
The mining process in GoldoreCore is inspired by the real-world dynamics of gold extraction:

Mining Duration: Gold has been mined for approximately 7,000 years.
Annual Production: Historically, about 30.37 tonnes of gold are mined annually over this period, with modern figures ranging from 2,500 to 3,000 tonnes.
Mining Rate: Every 10 minutes, about 0.057 tonnes of virtual gold is 'mined', mirroring the Bitcoin block time.
Scientific Background
The simulation includes melting and solidification processes, critical to understanding the transformation of gold:

c++
Copy code
const double meltingPoint = 1064; // Celsius
const double specificHeat = 0.129; // J/g°C
const double heatOfFusion = 64.5; // J/g

double energyToMelt(double mass) {
    return mass * heatOfFusion;
}

bool simulateHeating(double initialTemp, double energy, double mass) {
    double temperatureIncrease = energy / (mass * specificHeat);
    double finalTemp = initialTemp + temperatureIncrease;
    return finalTemp >= meltingPoint;
}
Additional Information
Project Website: https://goldorecoincore.org
Download: For an immediately usable, binary version of the GoldoreCore software, visit https://goldorecoincore.org/en/download/.
Development Process
The master branch is regularly built and tested (refer to doc/build-*.md for build instructions). Releases are tagged from stable branches as new versions.

GUI Development
The GUI development takes place in a separate repository: https://github.com/goldorecoin-core/gui. This ensures a focused environment for enhancing user interactions.

Contributions
See CONTRIBUTING.md for how to help out. Unit tests and code reviews are particularly valued, ensuring reliability and security.

Testing
GoldoreCore undergoes rigorous testing to ensure stability and reliability:

Automated Testing: Developers are encouraged to write and run unit tests (make check).
Manual QA Testing: Important changes are validated independently by a second party.
Integration Testing: Comprehensive tests in Python are available in test/functional/.
Translations
Translation contributions can be made on the Transifex page dedicated to GoldoreCore. Visit the translation process documentation for more details.

Note: Translation changes should not be submitted through GitHub as they will be overwritten by the next sync from Transifex.

License
GoldoreCore is released under the MIT license. For more information, see COPYING in the repository.
