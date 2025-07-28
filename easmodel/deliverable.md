The goal of this project is to generate realistic particle data at sea level, resulting from atmospheric showers, using GAN models (Generative Adversarial Networks). For each energy range of the primary particle, a separate WGAN (Wasserstein-GAN) is trained, regularized using the gradient penalty method and based on convolutional architectures. The networks adopt a conditional variant (cWGAN), enabling the generation of showers conditioned on both the energy of the primary particle and the altitude of the first interaction in the atmosphere. The generator network incorporates self-attention layers to ensure global coherence among the particles generated within the same event.

Each shower event includes several particle types. For each type, the data is represented as a 4-dimensional array with shape (16, 16, 16, 8), corresponding to the physical quantities: px, py, pz, and r, where r is the transverse distance from the impact point of the primary on the reference plane at sea level. The value of each element in the array is given by:

log₁₀(N(px, py, pz, r) + 1),

where N(px, py, pz, r) represents the number of particles reaching the ground within a specific bin defined by:
    • Px < px < Px + ΔPx
    • Py < py < Py + ΔPy
    • log₁₀(Pz) < log₁₀(pz) < log₁₀(Pz) + Δlog₁₀(Pz)
    • log₁₀(R) < log₁₀(r) < log₁₀(R) + Δlog₁₀(R)

The bin widths ΔG (for each physical quantity G) are variable and depend both on the specific quantity and on the energy range of the event. For a fixed energy range, the extreme values of each binning range are determined from the data:
    • For px and py, a linear spacing is assumed within the interval [-PM, +PM], where PM is the 80th percentile of the distribution of maximum absolute values of px and py per event.
    • For r, a logarithmic spacing is used, with a maximum value RM equal to the 90th percentile of the distribution of maximum r values across events.
    • For pz, the maximum range PzM corresponds to the maximum of the distribution of the per-event maximum pz values. The minimum pz is fixed at the point where log₁₀(pz) = 0.
    
The choice to reduce the two transverse coordinates (x, y) to the single variable r is based on an approximation—validated on the available data—according to which the angle formed by the transverse momentum pT in the sea-level plane coincides with the angle defined by r, an assumption valid for particles produced near the primary trajectory.

The output of the generator network will thus be the number of particles falling within each bin of the space:
[Px, Px+ΔPx] × [Py, Py+ΔPy] × [log₁₀(Pz), log₁₀(Pz)+Δlog₁₀(Pz)] × [log₁₀(R), log₁₀(R)+Δlog₁₀(R)].
Once a coordinate in the (px, py, pz, r) space is assigned to each generated particle, it is then possible to reconstruct its spatial position by associating the same transverse angle from pT to the corresponding r value.
