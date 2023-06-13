import numpy as np

import matplotlib.pyplot as plt

def fermi_dirac(energy, temperature, fermi_energy):

    return 1 / (np.exp((energy - fermi_energy) / (temperature)) + 1)

def plot_fermi_dirac(temperature, fermi_energy):

    energy = np.linspace(-10, 10, 1000)

    distribution = fermi_dirac(energy, temperature, fermi_energy)

    

    plt.plot(energy, distribution)

    plt.xlabel('Energy')

    plt.ylabel('Occupancy Probability')

    plt.title('Fermi-Dirac Distribution')

    plt.grid(True)

    plt.show()

# Set the temperature and Fermi energy

temperature = 300  # in Kelvin

fermi_energy = 0   # in arbitrary units

# Plot the Fermi-Dirac distribution function

plot_fermi_dirac(temperature, fermi_energy)





