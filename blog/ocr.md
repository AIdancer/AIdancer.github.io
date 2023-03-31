## 使用tesseract进行图片文字识别

  - 下载tesseract（这里使用了windows版本）：https://github.com/UB-Mannheim/tesseract/wiki
  - 安装过程住注意下载语言库：chi-sim
  - 设置环境变量：tesseract的安装目录
  - 安装Python依赖：pip install pytesseract

  一段简单的识别代码：  

```python
from PIL import Image
import pytesseract

if __name__ == "__main__":
    image = Image.open(r"test004.png")
    result = pytesseract.image_to_string(image, "chi_sim")
    # 输出识别内容
    print(result)
```


