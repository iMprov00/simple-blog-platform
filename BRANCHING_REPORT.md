# Branching Report

## Merge Statistics
- Total number of merges: 4
- Fast-forward merges: 1 (feature/posts)
- 3-way merges: 3 (feature/comments, feature/design, documentation)
- Merges with conflicts: 1 (feature/header-update)

## Branch History
git log --graph --oneline --all

*   fa8ad3a (HEAD -> master, origin/master) Merge branch 'documentation'
|\
| * 7c54907 (documentation) Update documentation
|/
*   e6fb158 Merge feature/header-update with conflict resolution
|\
| * f00b595 Update header to v2.0
* | 0501fd5 Customize blog title
|/
*   09088a6 Merge branch 'feature/design'
|\
| * 8865955 Improve design and add navigation
* | 584200e Add comments section
|/
* 4cc00b5 Add posts page and functionality
* 45dc575 Initial project setup

## Lessons Learned
Я узнал что существует 2 вида слияния: быстрая перемотка (fast-forward), когда ветка, грубо говоря, просто переходит обратно в основную, тогда по логам даже не будет видно что было слияние веток (если при слиянии не укажут флаг --no-ff), а так же узнал про трехсторонее слияние (3-way merge), когда 2 и более веток развивались отдельно. В таком случае обе и более веток имеют уникальные коммиты. При объеднинении ветки сравнивают начальный коммти (с которого началось ветвление), и в случае конфлика сообщают об этом пользователю.

Также узнал про решение конфликтов. При возникновении конфлика git помети сам конфликт в файле в формате <<<HEAD ==== >>>, где HEAD - это то что содержит основная ветка, а поле === то что содержит сливаемая ветка. В таких случая проблему можно разрешить разными способами: принять измненеия только одной из веток (ours - текущая ветка или theirs - сливаемая), либо вручную внести измненения и закоммитить.

Спасибо за курс! За уже пройденных 4 главы узнал про Git больше чем за пол года самостоятельной работы с ним, параллельно с обучением языков!
