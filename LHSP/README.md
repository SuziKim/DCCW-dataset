LHSP (Lin and Hanrahan Similarity Palettes) Dataset
===

[Dynamic Closest Color Warping to Sort and Compare Palettes](https://doi.org/10.1145/3450626.3459776)  
[Suzi Kim](https://kimsuzi.com/cv) and Sunghee Choi  
[Geometric Computing Lab.](https://gclab.kaist.ac.kr), [School of Computing](https://cs.kaist.ac.kr), [KAIST](https://kaist.ac.kr)  
Presented at [ACM SIGGRAPH 2021](https://s2021.siggraph.org/)

## 1. Description
- LHSP is a dataset to measure the palette similarity.
- For each query palette, we test how many sibling palettes are found.

## 2. Structure
### 2-1. Tree

```
/LHSP
├── /swatches
└── /LHSP_k%d_jitter%d_replacement%d
	├── query-palettes.csv
	├──/query-palettes-images
	│   ├── 0-{1st query palette' source image name}.png
	│   ├── 1-{2nd query palette' source image name}.png
	│   ├── ...
	│   └── n-{(n+1)-th palette's source image name}.png
	├── retrieval-palettes.csv
	└──/retrieval-palettes-images
		├── 0-{1st retrieval palette's source image name}.png
		├── 1-{2nd retrieval palette's source image name}.png
		├── ...
		└── m-{(m+1)-th retrieval palettes source image name}.png
```

#### **/swatches** 
- This includes original swatches from Lin and Hanrahan's. It is the set of the swatches that participants and artists can choose from.

#### **/LHSP_k%d_jitter%d_replacement%d** 

| parameter 	|  description 												|
|---------------|-----------------------------------------------------------|
| k 			| length of palette 										|
| jitter 		| jittering offset (alpha in RGB space)						|
| replacement 	| count of new colors replaced from the original swatches	|


### 2-2. Structure of each CSV file
#### query_palettes.csv
- List of query palettes
- Structure of each query: 
	- {query's source image} {lenght of the query palette} {hex colors}

#### retrieval_palettes.csv
- List of retrieval palettes
- Structure of each target:
	- {target's source image} {lenght of the query palette} {hex colors}


## 3. Credits of base color schemes and swatches
- Modeling How People Extract Color Themes from Images (Sharon Lin and Pat Hanrahan, CHI 2013)
	- Link: https://www.sharondlin.com/papers/colorThemes-dataset.zip

## 4. Publication
Our paper is available at [ACM Digital Library](https://doi.org/10.1145/3450626.3459776). Please cite with the following Bibtex code:  

```bibtex
@article{kim2021dynamic,
    title = {Dynamic Closest Color Warping to Sort and Compare Palettes},
    author = {Kim, Suzi and Choi, Sunghee},
    year = {2021},
    journal = {ACM Transactions on Graphics (Proceedings SIGGRAPH)},
    volume = {40},
    number = {4},
    articleno = {95},
    address = {New York, NY, USA},
    doi = {10.1145/3450626.3459776},
}
```

## 5. Acknowledgements
This work was supported by [Institute of Information & communications Technology Planning & Evaluation (IITP)](https://www.iitp.kr/) grant funded by the Korea government(MSIT) (No.2019-0-01158, Development of a Framework for 3D Geometric Model Processing)
