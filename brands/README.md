# Brands

Brand profiles live here, one file per brand.

A brand profile supplies the specific assets and voice for layer 6 of Design OS: typefaces, colors, logo, imagery, icons, tone, signature motion and distinctive assets. The rules for how a brand connects to the other layers are in [`archetypes/brand.md`](../archetypes/brand.md).

---

## Creating a brand profile

1. Copy [`templates/brand-profile.md`](../templates/brand-profile.md) to `brands/<brand-name>.md`.
2. Use lowercase and hyphens for the file name, for example `brands/example-brand.md`.
3. Fill in what the brand guidelines define. Leave the rest empty; empty sections fall back to the visual language and dial defaults.
4. Set the status:
   - `draft` while it is being filled in
   - `provisional` for a minimum viable brand, to be replaced later
   - `approved` when the brand owner has confirmed it
5. Record conflicts with the chosen visual language under "Known tensions" in the profile.

---

## Guidelines

- Keep structure and behavior out of brand profiles. Navigation, layout and states belong to other layers.
- Give every brand hue as a full scale, not a single swatch.
- Link to the source guidelines in the front matter, so the profile can be checked against them.
- Store large assets, such as font files, logos and imagery, where the project keeps assets, and reference them from the profile. Keep this folder to text.
- Client brands may be confidential. Keep them in project repositories rather than in the shared Design OS repository unless sharing is agreed.
