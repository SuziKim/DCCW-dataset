KHTP (Kobayashi Hue & Tone 130 palette) Dataset
===

[Dynamic Closest Color Warping to Sort and Compare Palettes](https://doi.org/10.1145/3450626.3459776)  
[Suzi Kim](https://kimsuzi.com/cv) and Sunghee Choi  
[Geometric Computing Lab.](https://gclab.kaist.ac.kr), [School of Computing](https://cs.kaist.ac.kr), [KAIST](https://kaist.ac.kr)  
Presented at [ACM SIGGRAPH 2021](https://s2021.siggraph.org/)

## 1. Description
- KHTP is a dataset to evaluate the palette pair sorting.
- For each test palette, the naturalness and concurrency of the pair are measured.

## 2. Structure
### 2-1. Tree

```
/KHTP-interpolation%d-jitter%d
├──/KHTP-interpolation%d-jitter%d-csv : This includes test palette pair in format of csv.
│   ├── KHTP-p0.csv
│   ├── KHTP-p1.csv
│   ├── ...
│   └── KHTP-p99.csv
└──/KHTP-interpolation%d-jitter%d-image : This includes test palette pair's images.
    ├── KHTP-p0-0.png 		: image of the 1st palette of the first pair in shuffled order
  ├── KHTP-p0-0-sorted.png : image of the 1st palette of the first pair in sorted order
    ├── KHTP-p0-1.png 		: image of the 2nd palette of the first pair in shuffled order
  ├── KHTP-p0-1-sorted.png : image of the 2nd palette of the first pair in sorted order
    ├── ...
    ├── KHTP-p99-0.png 
  ├── KHTP-p99-0-sorted.png 
    ├── KHTP-p99-1.png 
    └── KHTP-p99-1-sorted.png 
```

- The name of each KHTP type follows _KHTP-interpolation%d-jitter%d_.

  | parameter 		| description 				|
  |-----------------|---------------------------|
  | interpolation 	| interpolated color count	|
  | jitter			| jittering offset			|


### 2-2. Structure of the CSV file
- The name of each file follows _KHTP-p%d.csv_.

  | parameter	|  description 		|
  |-------------|-------------------|
  | p			| palette's no.		|

- Each CSV file presents a test palette pair, and the order is shuffled.
- A palette pair consists of two palettes P1 and P2.

  | row no.	|  description 									|
  |---------|-----------------------------------------------|
  | 1		| original order of hex color in the sorted P1	|
  | 2		| shuffled hex colors of the P1					|
  | 3		| original order of hex color in the sorted P2	|
  | 4		| shuffled hex colors of the P2					|


- Example:
  ``` bash
  > cat example.csv
  0	7	8	3	9	1	4	6	2	5
  #e76c56	#cbd7e8	#b8bebd	#a2b324	#cd9a95	#f1b066	#129a2f	#7ebcd1	#e3bd1c	#2b9759
  0	6	8	2	7	5	3	4	1	9
  #cf2e31	#00939f	#b8bebd	#e1c808	#a5b8c7	#068654	#aac61b	#58ab2d	#f1b066	#a09383
  ``` 

    - Sorted hexes of first palette: 
    	- #e76c56 #f1b066 #e3bd1c #a2b324 #129a2f #2b9759 #7ebcd1 #cbd7e8 #b8bebd #cd9a95
    	
    - Sorted hexes of second palette:
    	- #cf2e31 #f1b066 #e1c808 #aac61b #58ab2d #068654 #00939f #a5b8c7 #b8bebd #a09383
    
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
