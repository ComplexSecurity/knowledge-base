# @Html.Partial()

The `@Html.Partial()` function is used in [ASP.NET](../frameworks/aspnet.md) MVC ([Model-View-Controller (MVC)](../misc/mvc.md)) framework, which is a part of ASP.NET for building web applications. It's a method defined in the `HtmlHelper` class and is used to render a specified partial view within a view. This method helps in modularizing and reusing views by allowing the inclusion of reusable components (partial views) within other views.

It helps in breaking down complex views into smaller, reusable components (partial views) and enables the reuse of views across different parts of the application. It also improves the maintainability of the code by keeping views organized and avoiding repetition.

The syntax is:

```cs
@Html.Partial(string partialViewName)
@Html.Partial(string partialViewName, object model)
```

- `partialViewName`: The name of the partial view to render.
- `model` (Optional): The model that should be passed to the partial view.

Some usage examples include rendering a partial view without a passing model:

```cs
@Html.Partial("PartialViewName")
```

And with passing a model:

```cs
@Html.Partial("PartialViewName", Model)
```

As an example, assume you have a partial view named `_UserInfo.cshtml` that renders user information. In your main view, you can render this partial view as follows:

```cs
@Html.Partial("_UserInfo", Model.UserInfo)
```

The partial view is rendered inline and its output is included in the parent view's output. The `@Html.Partial()` method can be called with just the name of the partial view or with both the name and the model to be passed to the partial view.

Partial views are generally stored in the `Views/Shared` folder if they are to be shared across multiple views or in the same folder as the calling view if they are specific to that view. ASP.NET MVC also offers other similar methods like `@Html.RenderPartial()`, which has slight differences in usage and performance characteristics. 

`RenderPartial` writes directly to the response stream, offering better performance for larger content, whereas `Html.Partial` returns a string that can be stored, manipulated, or displayed in different ways.