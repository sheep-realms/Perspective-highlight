# 楼梯
和台阶不同的是，楼梯不存在混用模型的情况，因此不需要修改方块状态文件。然而原版的楼梯模型文件并没有为其完整面赋予额外的纹理，因此需要对楼梯的模型进行修改。

楼梯的模型有三种，分别为默认、内角（Inner）和外角（Outer）。

在本资源包中，为了实现在楼梯完整面使用其他纹理，创建了三个新模型：

``` json title="models/block/stairs_all.json" linenums="1" hl_lines="26 31 42"
{   "parent": "block/block",
    "display": {
        "gui": {
            "rotation": [ 30, 135, 0 ],
            "translation": [ 0, 0, 0],
            "scale":[ 0.625, 0.625, 0.625 ]
        },
        "head": {
            "rotation": [ 0, -90, 0 ],
            "translation": [ 0, 0, 0 ],
            "scale": [ 1, 1, 1 ]
        },
        "thirdperson_lefthand": {
            "rotation": [ 75, -135, 0 ],
            "translation": [ 0, 2.5, 0],
            "scale": [ 0.375, 0.375, 0.375 ]
        }
    },
    "textures": {
        "particle": "#side"
    },
    "elements": [
        {   "from": [ 0, 0, 0 ],
            "to": [ 16, 8, 16 ],
            "faces": {
                "down":  { "uv": [ 0, 0, 16, 16 ], "texture": "#after", "cullface": "down" },
                "up":    { "uv": [ 0, 0, 16, 16 ], "texture": "#top" },
                "north": { "uv": [ 0, 8, 16, 16 ], "texture": "#side", "cullface": "north" },
                "south": { "uv": [ 0, 8, 16, 16 ], "texture": "#side", "cullface": "south" },
                "west":  { "uv": [ 0, 8, 16, 16 ], "texture": "#side", "cullface": "west" },
                "east":  { "uv": [ 0, 8, 16, 16 ], "texture": "#after", "cullface": "east" }
            }
        },
        {   "from": [ 8, 8, 0 ],
            "to": [ 16, 16, 16 ],
            "faces": {
                "down":  { "uv": [ 8, 0, 16, 16 ], "texture": "#bottom", "cullface": "down" },
                "up":    { "uv": [ 8, 0, 16, 16 ], "texture": "#top", "cullface": "up" },
                "north": { "uv": [ 0, 0,  8,  8 ], "texture": "#side", "cullface": "north" },
                "south": { "uv": [ 8, 0, 16,  8 ], "texture": "#side", "cullface": "south" },
                "west":  { "uv": [ 0, 0, 16,  8 ], "texture": "#side" },
                "east":  { "uv": [ 0, 0, 16,  8 ], "texture": "#after", "cullface": "east" }
            }
        }
    ]
}
```

``` json title="models/block/inner_stairs_all.json" linenums="1" hl_lines="9 12 14 23 25 34 36"
{
    "textures": {
        "particle": "#side"
    },
    "elements": [
        {   "from": [ 0, 0, 0 ],
            "to": [ 16, 8, 16 ],
            "faces": {
                "down":  { "uv": [ 0, 0, 16, 16 ], "texture": "#after", "cullface": "down" },
                "up":    { "uv": [ 0, 0, 16, 16 ], "texture": "#top" },
                "north": { "uv": [ 0, 8, 16, 16 ], "texture": "#side", "cullface": "north" },
                "south": { "uv": [ 0, 8, 16, 16 ], "texture": "#after", "cullface": "south" },
                "west":  { "uv": [ 0, 8, 16, 16 ], "texture": "#side", "cullface": "west" },
                "east":  { "uv": [ 0, 8, 16, 16 ], "texture": "#after", "cullface": "east" }
            }
        },
        {   "from": [ 8, 8, 0 ],
            "to": [ 16, 16, 16 ],
            "faces": {
                "down":  { "uv": [ 8, 0, 16, 16 ], "texture": "#bottom", "cullface": "down" },
                "up":    { "uv": [ 8, 0, 16, 16 ], "texture": "#top", "cullface": "up" },
                "north": { "uv": [ 0, 0,  8,  8 ], "texture": "#side", "cullface": "north" },
                "south": { "uv": [ 8, 0, 16,  8 ], "texture": "#after", "cullface": "south" },
                "west":  { "uv": [ 0, 0, 16,  8 ], "texture": "#side" },
                "east":  { "uv": [ 0, 0, 16,  8 ], "texture": "#after", "cullface": "east" }
            }
        },
        {   "from": [ 0, 8, 8 ],
            "to": [ 8, 16, 16 ],
            "faces": {
                "down":  { "uv": [ 0, 0,  8,  8 ], "texture": "#bottom", "cullface": "down" },
                "up":    { "uv": [ 0, 8,  8, 16 ], "texture": "#top", "cullface": "up" },
                "north": { "uv": [ 8, 0, 16,  8 ], "texture": "#side" },
                "south": { "uv": [ 0, 0,  8,  8 ], "texture": "#after", "cullface": "south" },
                "west":  { "uv": [ 8, 0, 16,  8 ], "texture": "#side", "cullface": "west" },
                "east":  { "uv": [ 0, 0,  8,  8 ], "texture": "#after", "cullface": "east" }
            }
        }
    ]
}
```

``` json title="models/block/outer_stairs_all.json" linenums="1" hl_lines="9"
{
    "textures": {
        "particle": "#side"
    },
    "elements": [
        {   "from": [ 0, 0, 0 ],
            "to": [ 16, 8, 16 ],
            "faces": {
                "down":  { "uv": [ 0, 0, 16, 16 ], "texture": "#after", "cullface": "down" },
                "up":    { "uv": [ 0, 0, 16, 16 ], "texture": "#top" },
                "north": { "uv": [ 0, 8, 16, 16 ], "texture": "#side", "cullface": "north" },
                "south": { "uv": [ 0, 8, 16, 16 ], "texture": "#side", "cullface": "south" },
                "west":  { "uv": [ 0, 8, 16, 16 ], "texture": "#side", "cullface": "west" },
                "east":  { "uv": [ 0, 8, 16, 16 ], "texture": "#side", "cullface": "east" }
            }
        },
        {   "from": [ 8, 8, 8 ],
            "to": [ 16, 16, 16 ],
            "faces": {
                "down":  { "uv": [ 8, 0, 16,  8 ], "texture": "#bottom", "cullface": "down" },
                "up":    { "uv": [ 8, 8, 16, 16 ], "texture": "#top", "cullface": "up" },
                "north": { "uv": [ 0, 0,  8,  8 ], "texture": "#side" },
                "south": { "uv": [ 8, 0, 16,  8 ], "texture": "#side", "cullface": "south" },
                "west":  { "uv": [ 8, 0, 16,  8 ], "texture": "#side" },
                "east":  { "uv": [ 0, 0,  8,  8 ], "texture": "#side", "cullface": "east" }
            }
        }
    ]
}
```

上面的模型中，定义了新的纹理 `#after`，表示楼梯的完整面。随后在子模型中使用它，以橡木楼梯为例：

``` json title="models/block/oak_stairs.json" linenums="1" hl_lines="7"
{
    "parent": "block/stairs_all",
    "textures": {
        "bottom": "block/oak_planks",
        "top": "block/oak_planks",
        "side": "block/oak_planks",
		"after": "block/oak_planks_stairs"
    }
}
```

``` json title="models/block/oak_stairs_inner.json" linenums="1" hl_lines="7"
{
    "parent": "block/inner_stairs_all",
    "textures": {
        "bottom": "block/oak_planks",
        "top": "block/oak_planks",
        "side": "block/oak_planks",
		"after": "block/oak_planks_stairs"
    }
}
```

``` json title="models/block/oak_stairs_outer.json" linenums="1" hl_lines="7"
{
    "parent": "block/outer_stairs_all",
    "textures": {
        "bottom": "block/oak_planks",
        "top": "block/oak_planks",
        "side": "block/oak_planks",
		"after": "block/oak_planks_stairs"
    }
}
```

上面的模型指定了一个新纹理 `oak_planks_stairs.png`。