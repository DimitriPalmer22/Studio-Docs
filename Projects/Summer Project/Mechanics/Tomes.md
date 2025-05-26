Tomes themselves are blueprints. The mesh / materials they use can be configured.

# Primary Attack
- The primary attacks are all components that derive from the same base class

### Types of Primary Attack

- Single Fire (Semi-Automatic)
- Burst
- Automatic (Magazine Size)
- Shotgun
- Charge Single Fire
- Charge Burst

![Test](<../../../_Meta/Attachments/Pasted image 20250509175042.png>)

# Tome Ability Data Asset

This is a data asset that contains all the unchanging information about an ability in the game.

They derive from one base class: `TomeAbilityDataAsset`.
- This is used to define the ability's name, description, icon, and other static information.

The child classes of `TomeAbilityDataAsset` define the categories types of abilities.
- `PrimaryAttackDataAsset`
- `SecondaryAttackDataAsset`
- `PassiveAbilityDataAsset`
- `UltimateAbilityDataAsset`
- `TransformAbilityDataAsset`

# Tome Ability Modifier Info

This is a struct that is responsible for holding the information for an ability, as well as all the current modifiers applied to it.

It stores the tome ability data asset and other things such as
- Damage modifier (If applicable)
- Cooldown modifier
- Duration modifier (if I can do this)
