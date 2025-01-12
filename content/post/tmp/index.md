+++ 
author = "Husky"
title = "tmp"
date = "2025-01-12"
categories = [
    "Blog"
]
+++
```json
{   "nodes": [     {"id": 1, "label": "point O", "attributes": {"color": "black"}},    
              	   {"id": 2, "label": "point A", "attributes": {"color": "black"}},
             	   {"id": 3, "label": "point B", "attributes": {"color": "black"}},
              {"id": 4, "label": "point C", "attributes": {"color": "black"}},
              {"id": 5, "label": "point P", "attributes": {"color": "black"}},
              {"id": 6, "label": "sector", "attributes": {"color": "black"}},
              {"id": 7, "label": "line OP", "attributes": {"color": "black"}},
              {"id": 8, "label": "line CP", "attributes": {"color": "black"}},
              {"id": 9, "label": "line OA", "attributes": {"color": "black"}},
              {"id": 10, "label": "line OB", "attributes": {"color": "black"}},
             ],   
 
 	"edges": [     {"source": 1, "target": 6, "relation": "at the center of sector"}, 
             	  {"source": 2, "target": 6, "relation": "one end on the act of the sector"},
				{"source": 3, "target": 6, "relation": "the other end on the act of the sector"},
              				{"source": 5, "target": 6, "relation": "a random location on the act of the sector"},
              				{"source": 4, "target": 9, "relation": "on a location of line"},
              				{"source": 8, "target": 10, "relation": "parallel"},
				
             ] }
```

![image-20241225221323827](tmp.assets/image-20241225221323827.png)

(Two-dimensional image, composed only of lines, pay attention to the marking of mathematical quantities in the figure) As shown in the figure, the sector AOB, the size of the central angle is equal to one-third of pi, the radius is 2, there is a moving  point C on the radius OA, and a straight line parallel to OA through point C intersects the arc at point P

![image-20241225222704402](tmp.assets/image-20241225222704402.png)

结果还是很差



暂时没有找到做自动生成canvas的方法，同时考虑场景图的生成，假定已经预训练好一个根据图像和文本生成场景图的模型

有没有真实的图像标签，如果有，直接利用真实图片生成场景图，将文本和场景图作为输入且不再改动场景图；如果没有真实图像便签，则使用预训练的场景图生成器来借助文本和扩散模型生成的图像生成初步的场景图，添加评判器评判



