
[![issues](https://img.shields.io/github/issues/IKEA/IKEA3DassemblyDataset.svg?color=green&style=flat-square&logo=appveyor)](https://github.com/IKEA/IKEA3DassemblyDataset/issues)
[![stars](https://img.shields.io/github/stars/IKEA/IKEA3DassemblyDataset.svg?color=yellow&style=flat-square&logo=appveyor)](https://github.com/IKEA/IKEA3DassemblyDataset)
[![forks](https://img.shields.io/github/forks/IKEA/IKEA3DassemblyDataset.svg?color=orange&style=flat-square&logo=appveyor)](https://github.com/IKEA/IKEA3DassemblyDataset)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg?style=flat-square&logo=appveyor)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

Copyright © Inter IKEA Systems B.V. 2021

- [IKEA 3D Assembly Dataset](#ikea-3d-assembly-dataset)
  - [Key Features](#key-features)
  - [Products in the dataset](#products-in-the-dataset)
  - [Dataset Format](#dataset-format)
  - [Version](#version)
  - [License](#license)
  - [Citations](#citations)
  - [Disclaimer of Warranties and Limitation of Liability](#disclaimer-of-warranties-and-limitation-of-liability)
  - [Contact](#contact)

# IKEA 3D Assembly Dataset

The IKEA 3D Assembly Dataset is made available by Inter IKEA Systems B.V., to encourage research related to assembly instructions. Providing  3D files for products, which have been prepared so that each part that a user interacts with during assembly, should be easy to manipulate in 3D.

## Key Features

- IKEA 3D models corresponding to 5 IKEA products in final assembly state, where all parts a customer interact with during assembly is included.
- Base color/material assigned to the product parts.
- The corresponding assembly instruction document, in the current versions at the time of sharing*.

*We will not monitor for newer versions and update the dataset to match by default.

## Products in the dataset

| Image | Product Description |
| :--- | :--- |
| ![30449908 LACK 55x55 in white - A side table](/Dataset/LACK_30449908_55x55/LACK_30449908.jpg) | [30449908](https://www.ikea.com/nl/en/p/lack-side-table-white-30449908/) <br/><br/>**LACK**<br/> 55x55 in white - A side table |
| ![70332124 EKET 35x25x35 in white A small cabinet.](/Dataset/EKET_70332124_35x25x35/EKET_70332124.jpg) | [70332124](https://www.ikea.com/nl/en/p/eket-cabinet-white-70332124/)<br/><br/>**EKET**<br/> 35x25x35 in white - A small cabinet. |
| ![00333947 EKET 70x35x35 in white A cabinet with 2 drawers.](/Dataset/EKET_00333947_70x35x35/EKET_70332124.jpg) | [00333947](https://www.ikea.com/nl/en/p/eket-cabinet-with-2-drawers-white-00333947/) <br/><br/>**EKET**<br/> 70x35x35 in white - A cabinet with 2 drawers. |
| ![40463852 BEKVÄM in black - A step stool](/Dataset/BEKV%C3%84M_40463852/BEKV%C3%84M_40463852.jpg) | [30178884](https://www.ikea.com/pt/en/p/bekvaem-step-stool-black-30178884/) <br/> [40463852](https://www.ikea.com/nl/en/p/bekvaem-step-stool-black-30178884/) <br/><br/>**BEKVÄM**<br/> in black - A step stool <br/>| 
| ![60155602 DALFRED in black - A bar stool](/Dataset/DALFRED_60155602/DALFRED_60155602.jpg) | [60155602](https://www.ikea.com/nl/en/p/dalfred-bar-stool-black-60155602/) <br/><br/>**DALFRED**<br/> in black - A bar stool |

Please note:
> The models in the dataset is referring to article numbers sold in Europe.
> You might need *another article number* if purchasing from a store outside Europe.
> Ask the staff in your local IKEA store to help you find a match.
> For BEKVÄM, we are providing 2 models due to construction variations in different markets. We have not included a model for BEKVÄM and the North American market.
> The table below can help you identify which model you should use, depending on the product available in your market.

| Article number  | Product name              | Assembly document number       |Model to use|
| :---------- |:----------------------------------| :-------------------------------- |:----------|
| 30178884 | BEKVÄM step stool 50 black | AA-444158-9                       | 30178884 |
| 00363722 | BEKVÄM step stool 50 black AP  | AA-444158-9                       | 30178884 |
| 40463852 | BEKVÄM step stool 50 black EU | AA-323406-7                       | 40463852 |

> At the time of releasing the dataset in 2021, the products were sold globally, which can change with time. If the links above are not leading to a product page, it could be that the article was removed from the active product range.
The assembly document can get updates during the time the product is in IKEAs product range. Compare the assembly document number (ex AA-444158-9) shared in this repository with the assembly instruction document (last page, bottom of the page) found when opening the product package. If the number at the end is higher (ex. AA-44158-10) or lower (ex. AA-44158-8) there could be differences in the assembly procedure.

## Dataset Format

Each product has
| Filetype   | Description | Unit |
| :---------- | :----------- | :----------- |
|.glb/glTF   | in final assembled state with materials| __M meter__ according to glTF spec everything is defined in metric meter unit |
|.obj   | in final assembled state with base color materials only| __mm millimeter__ we exported the geometry in metric mm unit |
|.pdf   | the assembly instruction ||

Please note: For the glTF files we are using an extension called [KHR_Texture_Transform](https://github.com/KhronosGroup/glTF/tree/master/extensions/2.0/Khronos/KHR_texture_transform) to support individual tile-values for every texture. If you are using a software or library that is not supporting KHR_Texture_Transform you will end up with materials looking wrong since the textures will tile incorrect.

## Version

Version numbers are expressed as `major.minor`. `minor` changes are changes to the logic of the format that are not breaking changes, i.e., additions that build upon a previous version. `major` changes are breaking changes that alter the logic of a previous version.

`major` - If we add new models, delete models. Change materials, hierarchy in the 3D scene or UV fixes in previously shared models.

`minor` - If we open the previously shared models, change names of parts in the scene hierarchy or change the name of a texture.

## License

The IKEA 3D Assembly Dataset contained in the [BEKVAM_30178884.glb, BEKVAM_30178884.obj. BEKVÄM_40463852.glb, BEKVAM_40463852.obj, DALFRED_60155602.glb, DALFRED_60155602.obj, EKET_00333947_70x35x35.glb, EKET_00333947_70x35x35.obj, EKET_70332124_35x25x35.glb, EKET_70332124_35x25x35.obj, LACK_30449908_55x55.glb, LACK_30449908_55x55.obj] (the “Licensed Material”) is licensed by Inter IKEA Systems B.V. (“IKEA”) under the Creative Commons, Attribution-NonCommercial-ShareAlike 4.0 International ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)) for the purpose to enable research regarding assembly of furniture using the shared 3D data. The Licensed Material is limited to 3D modelling data/technology and does not include any IKEA products/objects. IKEA reserves the exclusive rights to the design, copyright and other intellectual property rights in the Licensed Materials as well as in its products/objects.

A [copy](/LICENSE.md) of the license is available in this repository.

## Citations

This dataset first appeared in the paper IKEA Object State Dataset: A 6DoF object pose estimation dataset and benchmark for multi-state assembly objects.
You can download the RGBD video of the assembly process, the 6DoF pose of furniture parts and their bounding box from [IKEAObjectStateDataset](https://github.com/mxllmx/IKEAObjectStateDataset).

If you found this dataset useful, please cite it as follows:

```text
@misc{su2021ikea,
       title={IKEA Object State Dataset: A 6DoF object pose estimation dataset and benchmark for multi-state assembly objects},
       author={Yongzhi Su and Mingxin Liu and Jason Rambach and Antonia 
Pehrson and Anton Berg and Didier Stricker},
       year={2021},
       eprint={2111.08614},
       archivePrefix={arXiv},
       primaryClass={cs.CV}
}
```

## Disclaimer of Warranties and Limitation of Liability

Unless otherwise separately undertaken by the Licensor, to the extent possible, the Licensor offers the Licensed Material as-is and as-available, and makes no representations or warranties of any kind concerning the Licensed Material, whether express, implied, statutory, or other. This includes, without limitation, warranties of title, merchantability, fitness for a particular purpose, non-infringement, absence of latent or other defects, accuracy, or the presence or absence of errors, whether or not known or discoverable. Where disclaimers of warranties are not allowed in full or in part, this disclaimer may not apply to You.

To the extent possible, in no event will the Licensor be liable to You on any legal theory (including, without limitation, negligence) or otherwise for any direct, special, indirect, incidental, consequential, punitive, exemplary, or other losses, costs, expenses, or damages arising out of this Public License or use of the Licensed Material, even if the Licensor has been advised of the possibility of such losses, costs, expenses, or damages. Where a limitation of liability is not allowed in full or in part, this limitation may not apply to You.

## Contact

For questions and/or feedback concerning the dataset create an issue on the repo. Read more about how to [here](https://github.com/IKEA/IKEA3DAssemblyDataset/blob/main/CONTRIBUTING.md)
