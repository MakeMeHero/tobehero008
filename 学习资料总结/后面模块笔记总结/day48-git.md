# 第五章：使用git管理文件版本（本地仓库）

## 概念

**版本库**：“.git”目录就是版本库，将来文件都需要保存到版本库中。

**工作目录（工作区）**：包含“.git”目录的目录，也就是.git目录的上一级目录就是工作目录==。只有工作目录中的文件或者是文件夹才能保存到版本库中==。

##我们把文件往Git版本库里添加的时候，是分两步执行的：

==第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；==

==第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支（默认是master）。==

# 第七章：分支管理

## 分支相关

1.一开始的时候，master分支是一条线，Git用master指向最新的提交，再用HEAD指向master，就能确定当前分支，以及当前分支的提交点

2.每次提交，master分支都会向前移动一步，这样，随着你不断提交，master分支的线也越来越长。

3.当我们创建新的分支，例如dev时，Git新建了一个指针叫dev，指向master相同的提交，再把HEAD指向dev，就表示当前分支在dev上

4.直接把master指向dev的当前提交，就完成了==合并==

5.合并完分支后，甚至可以删除dev分支。删除dev分支就是把dev指针给删掉，删掉后，我们就剩下了一条master