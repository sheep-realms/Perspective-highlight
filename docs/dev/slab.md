# 台阶
本资源包对不同状态的台阶制作了不同的模型。

以橡木台阶为例，其方块状态文件内容如下：

``` json title="blockstates/oak_slab.json" linenums="1" hl_lines="5"
{
    "variants": {
        "type=bottom": { "model": "block/oak_slab" },
        "type=top":    { "model": "block/oak_slab_top" },
        "type=double": { "model": "block/oak_slab_double" }
    }
}
```

相比于原版，此处对 `type=double` 也就是双台阶状态指定了新的模型。上面所使用的模型内容如下：

``` json title="models/block/oak_slab.json" linenums="1" hl_lines="4 5"
{
    "parent": "block/slab",
    "textures": {
        "bottom": "block/oak_planks_slab_bottom",
        "top":    "block/oak_planks_slab_bottom",
        "side":   "block/oak_planks"
    }
}
```

``` json title="models/block/oak_slab_top.json" linenums="1" hl_lines="4 5"
{
    "parent": "block/slab_top",
    "textures": {
        "bottom": "block/oak_planks_slab_top",
        "top":    "block/oak_planks_slab_top",
        "side":   "block/oak_planks"
    }
}

```

``` json title="models/block/oak_slab_double.json" linenums="1" hl_lines="4"
{
    "parent": "block/cube_all",
    "textures": {
        "all": "block/oak_planks_slab_double"
    }
}
```

上面的模型指定了以下新的纹理：

- `oak_planks_slab_top.png`
- `oak_planks_slab_bottom.png`
- `oak_planks_slab_double.png`