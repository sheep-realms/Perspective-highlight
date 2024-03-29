# 设计指南

## 纹理
透视与高亮资源包是一款基于 Minecraft 原版纹理修改的资源包，纹理的设计主要遵循以下原则：

1. 以实用作为首要目标；
2. 与 Minecraft 原版风格融合；
3. 对原版纹理的破坏尽可能降到最低；
4. 使用简单纯粹的颜色表达信息。 

## GUI
透视与高亮资源包有一套基于 Fallen Homes UI in Upperworld[^1] 演化而来的独特的 GUI 设计，从实用角度出发，添加适当的装饰，以冷淡、扁平、锐利作为核心设计理念。

### 配色
#### 基础色
| 名称 | HEX | 预览 |
| - | - | - |
| Primary | #FFFFFF | <span class="color-show" style="background-color: #FFFFFF;"></span> |
| Regular | #BFBFBF | <span class="color-show" style="background-color: #BFBFBF;"></span> |
| Secondary | #A6A6A6 | <span class="color-show" style="background-color: #A6A6A6;"></span> |

#### 功能色
| 名称 | HEX | 预览 |
| - | - | - |
| Success | #BFFFBF | <span class="color-show" style="background-color: #BFFFBF;"></span> |
| Danger | #FF6940 | <span class="color-show" style="background-color: #FF6940;"></span> |

### 边界与窗口
各个功能区的边界采用细线条描边，角落不做特别处理，使用直角作为拐角。

对于窗口元素来说，右上角会放置一个淡绿色小方块，就如同 LOGO 上的元素一样。

![窗口设计](../image/design/gui/window.png){ .pixel .center }

### 可交互元素
为了区分可交互元素，元素右上角设计了一个倒角。可交互元素被选中或鼠标进入时，边框会加粗强调。

![按钮设计](../image/design/gui/button.png){ .pixel .center }

### 物品格
有时一些颜色较深的物品放置在物品格中不易察觉，为了改善这一缺陷，物品格中心设计了一道斜线，表明该物品格为空。这道斜线可被大多数物品完全覆盖，当您看不到这道斜线时，即说明该物品格中存在物品。

![物品格](../image/design/gui/item.png){ .pixel .center }

[^1]: Fallen Homes UI in Upperworld 设计文档<br>[https://sheep-realms.github.io/Fallen-Homes-UI-in-Upperworld/design.html](https://sheep-realms.github.io/Fallen-Homes-UI-in-Upperworld/design.html)