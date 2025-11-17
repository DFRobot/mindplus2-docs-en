
欢迎来到 Mind+ 常见问题解答页面！这里汇总了用户在使用 Mind+ 软件过程中遇到的各类问题及其解决方案。

## 🔍 快速导航

根据您遇到的问题类型，选择对应的分类进行查找：

### 程序设计

<div class="grid cards" markdown>

- **[实时模式](Coding/RealTimeMode/index.md)**  
    [![实时模式](img/cover1-1.png){width=400, style="display:block;margin: 10px auto"}](Coding/RealTimeMode/index.md)

- **[上传模式](Coding/UploadMode/index.md)**  
    [![上传模式](img/cover2-2.png){width=400, style="display:block;margin: 10px auto"}](Coding/UploadMode/index.md)

- **[Python积木模式](Coding/PythonBlockMode/index.md)**  
    [![Python积木模式](img/cover3-3.png){width=400, style="display:block;margin: 10px auto"}](Coding/PythonBlockMode/index.md)

- **[MicroPython积木模式](Coding/MicroPythonBlockMode/index.md)**  
    [![MicroPython积木模式](img/cover4-4.png){width=400, style="display:block;margin: 10px auto"}](Coding/MicroPythonBlockMode/index.md)

</div>

### 模型训练

<div class="grid cards" markdown>

- **[模型训练](AITools/index.md)**  
    [![模型训练](img/cover5-5.png){style="display:block;margin: 10px auto"}](AITools/index.md)
</div>

### 界面设计

<div class="grid cards" markdown>

- **[界面设计](ViewDesign/index.md)**  
    [![界面设计](img/cover6-6.png){style="display:block;margin: 10px auto"}](ViewDesign/index.md)

<!-- - **[扩展库](UserExtension/index.md)**  
    [![扩展库](img/cover7-7.png){style="display:block;margin: 10px auto"}](UserExtension/index.md) -->

</div>

## 💡 使用提示

- **快速搜索**：<button onclick="openSearch()" style="background: #1976d2; color: white; border: none; padding: 4px 12px; border-radius: 4px; cursor: pointer; font-size: 0.9em;">🔍 点击搜索</button> 
- **问题反馈**：如果没有找到您的问题，可以通过官方QQ群或论坛反馈  
- **持续更新**：我们会根据用户反馈持续更新常见问题库

<script>
function openSearch() {
    // 尝试多种搜索框选择器，适配不同的MkDocs主题
    const searchSelectors = [
        '[data-md-component="search-query"]',
        '.md-search__input',
        'input[type="search"]',
        '#mkdocs-search-query',
        '.md-header__option .md-icon'
    ];
    
    let searchElement = null;
    
    // 依次尝试找到搜索元素
    for (const selector of searchSelectors) {
        searchElement = document.querySelector(selector);
        if (searchElement) {
            if (searchElement.tagName === 'INPUT') {
                // 如果是输入框，直接聚焦
                searchElement.focus();
                searchElement.click();
            } else {
                // 如果是按钮或图标，点击它
                searchElement.click();
                // 等待搜索框出现后聚焦
                setTimeout(() => {
                    const input = document.querySelector('[data-md-component="search-query"], .md-search__input, input[type="search"]');
                    if (input) input.focus();
                }, 100);
            }
            break;
        }
    }
    
    // 如果都找不到，使用键盘快捷键
    if (!searchElement) {
        const event = new KeyboardEvent('keydown', {
            key: 'k',
            ctrlKey: true,
            bubbles: true
        });
        document.dispatchEvent(event);
    }
}
</script>