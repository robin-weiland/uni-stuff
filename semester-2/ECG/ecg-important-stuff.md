Robin Weiland


ECG important stuff
================

---

[TOC]

---

<div style="page-break-after: always; break-after: page;"></div> 


# Transformation classes

<img src="res\important stuff\transformation-classes.png" alt="transformation classes" style="zoom:50%;" align="left"/>

| transformation  |                                                             |
| :-------------- | :---------------------------------------------------------- |
| Rigid/Euclidean | preserve distances<br />preserve angles                     |
| Similarity      | preserve angles                                             |
| Linear          | $L(p + q) = L(p) + L(q)$<br />$L(ap) = aL(p)$<br />$L(0)=0$ |
| Affine          | preserve parallel lines                                     |

# DirectX 10 class hardware pipeline

```mermaid
graph TB
	in{{Input Data}}
	
	ia["Input Assembler Stage (IA)"]
	
	vs["Vertex Shader Stage (VS)"]
	
	gs["Geometry Shader Stage (GS)"]
	
		so["Stream Output Stage (SO)"]
	
	rs("Rasterizer Stage (RS)")
	
	ps("Pixel Shader Stage (PS)")
	
	om("Output Merger Stage (OM)")
	
	out{{Output Data}}
	
	memory[Memory]
	
	
	memory-- Buffer -->ia
	memory-- Texture, Constant Buffer -->vs
	memory-- Texture, Constant Buffer -->gs
	memory-- Texture, Constant Buffer -->ps
	gs-->so-- Buffer -->memory
	in-->ia-->vs-->gs-->rs-->ps-->om-->out
	
	

	
```



<div style="page-break-after: always; break-after: page;"></div> 

