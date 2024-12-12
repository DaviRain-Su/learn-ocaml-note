# A tour of Ocaml

本教程介绍了 OCaml 的基本功能：值、表达式、列表、函数、模式匹配等等。

不需要 OCaml 或任何函数式编程知识;但是，本文假设读者具备一些基本的软件开发知识。请确保您已经安装了 OCaml 并设置了环境，如安装 OCaml 页面上所述。

我们建议你执行我们提供的示例，并尝试使用它们，以感受 OCaml 中的编码。为此，您可以使用 UTop （Universal Toplevel）。

UTop 允许用户通过读取和评估 OCaml 短语（如表达式或值定义）来与 OCaml 交互，并将结果打印在屏幕上。使用 utop 命令运行 UTop。按 Ctrl+D 退出它。要了解更多信息，你可以阅读 OCaml Toplevel 简介。

此导览中的一些示例包括注释。OCaml 中的注释以 （* 开头，以 * 结尾） 并且可以嵌套。
由于它们被 OCaml 忽略，因此它们可以在任何允许空格的地方使用。
在 UTop 中输入以下代码时，可以省略注释。以下是一些示例：

```ocaml
(* Here is a comment *)
(* Outside of the nested comment is still a comment. (* Here is a nested comment *) Outside of the nested comment again. *)
# 50 + (* A comment in between parts of an expression *) 50;;
- : int = 100
```

## 表达式和定义

让我们从一个简单的表达式开始：

```ocaml
# 50 + 50;;
- : int = 100
```

在 OCaml 中，一切都有一个值，每个值都有一个类型。
上面的示例说，“50 * 50 是一个类型为 int （整数） 的表达式，计算结果为 2500。
由于它是一个匿名表达式，因此将显示字符 - 而不是名称。
