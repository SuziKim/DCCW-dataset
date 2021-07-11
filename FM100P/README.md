FM100P (Farnsworth-Munsell 100 hue test palette) Dataset
===

[Dynamic Closest Color Warping to Sort and Compare Palettes](https://doi.org/10.1145/3450626.3459776)  
[Suzi Kim](https://kimsuzi.com/cv) and Sunghee Choi  
[Geometric Computing Lab.](https://gclab.kaist.ac.kr), [School of Computing](https://cs.kaist.ac.kr), [KAIST](https://kaist.ac.kr)  
Presented at [ACM SIGGRAPH 2021](https://s2021.siggraph.org/)

## 1. Description
- FM100P is a dataset to evaluate the single palette sorting.

## 2. Structure
### 2-1. Tree

```
/FM100P-k%d
├──/FM100P-k%d-csv : This includes test palettes in format of csv.
│   ├── FM100P-k%d-p0.csv
│   ├── FM100P-k%d-p1.csv
│   ├── ...
│   └── FM100P-k%d-p99.csv
├──/FM100P-k%d-image : This includes test palettes' images.
│   ├── FM100P-k%d-p0.png 		 : 1st palette's image in shuffled order
│   ├── FM100P-k%d-p0-sorted.png : 1st palette's image in correctly sorted order
│   ├── ...
│   ├── FM100P-k%d-p99.png
│   └── FM100P-k%d-p99-sorted.png
└──/FM100P-k%d-image-wbox : This includes test palettes' images with white boundary between adjacent colors.
	├── FM100P-k%d-p0.png 		 : 1st palette's image in shuffled order with white boundary between adjacent colors
	├── FM100P-k%d-p0-sorted.png : 1st palette's image in sorted order with white boundary between adjacent colors
	├── ...
	├── FM100P-k%d-p99.png
	└── FM100P-k%d-p99-sorted.png
```

- k indicates the length of palette with a range from 10 to 40.

### 2-2. Structure of the CSV file
- The name of each file follows _FM100P-k%d-p%d.csv_.

	| parameter	|  description 		|
	|-----------|-------------------|
	| k			| length of palette	|
	| p			| palette's no.		|

- Each CSV file presents a single test palette, and the order is shuffled.
- Structure of each row: 
    - {color's original index in the Farnsworth-Munsell 100 hue test palette} {hex color}


## 3. Publication
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

## 4. Acknowledgements
This work was supported by [Institute of Information & communications Technology Planning & Evaluation (IITP)](https://www.iitp.kr/) grant funded by the Korea government(MSIT) (No.2019-0-01158, Development of a Framework for 3D Geometric Model Processing)
