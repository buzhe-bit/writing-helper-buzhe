# writing-helper-buzhe

这是不遮的个人写作工作流仓库。它现在包含两类能力：

- `thought-article-workflow`: 主写作工作流，用来处理 Get 笔记初稿、公众号文章、小红书经验帖、标杆文章拆解和个人风格保持。
- `book-quote-skill`: 引用与原文搜索模块，用来给文章中的关键观点寻找书籍原文、作者表达或可嵌入的短引用。

## 推荐使用方式

优先使用 `skills/thought-article-workflow/SKILL.md` 作为主入口。

当主工作流诊断出某个观点“感觉对，但缺少支撑”时，再进入 `quote-support-guide.md` 判断是否需要调用 `book-quote-skill`。

简单说：

1. 先判断文章场景：公众号、小红书分享、小红书转化、标杆拆解。
2. 再诊断文章问题：观点、结构、证据、表达、人味。
3. 如果需要引用或原文支撑，再调用 `book-quote-skill` 找 2-3 个候选原文。
4. 最后把选中的引用嵌入文章，并检查它有没有破坏不遮自己的表达风格。

## 仓库结构

```text
SKILL.md
skills/
  book-quote-skill/
    SKILL.md
  thought-article-workflow/
    SKILL.md
    style-profile-memory.md
    style-profile-template.md
    benchmark-analysis-guide.md
    quote-support-guide.md
    case-study-ai-opportunity.md
    red-test-pack-ai-opportunity.md
    red-phase-runbook.md
    skill-spec.md
    test-scenarios.md
```

根目录的 `SKILL.md` 保留原来的引用助手，方便兼容旧用法；更推荐的新结构是从 `skills/thought-article-workflow/` 启动完整写作流程。

## 场景区分

这个仓库最重要的原则是：小红书不是一种单一文风。

- 小红书分享场景：真人感、真实细节、经验感、轻 CTA 或无 CTA。
- 小红书转化场景：痛点、利益点、行动引导、承接动作。
- 公众号场景：完整论证、概念铺垫、材料支撑、个人判断。
- 标杆拆解场景：分析哪里值得学，哪里不能照抄，再翻译成不遮自己的写法。

## 当前阶段

这是一个可以开始实际使用的 v1 版本。它已经沉淀了不遮目前确认过的写作偏好，尤其是“小红书分享帖不要写成营销转化稿”这一条。

后续每次使用时，如果出现“这不像我”“这个味儿不对”“这里太营销了”之类的反馈，都应该继续更新 `style-profile-memory.md`，让这个 Skill 越来越像不遮自己的写作搭子。
