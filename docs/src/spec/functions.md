# Functions

> **<sup>Syntax</sup>**\
> _Function_ :\
> &nbsp;&nbsp; _FunctionQualifiers_ `def` [IDENTIFIER]\
> &nbsp;&nbsp; &nbsp;&nbsp; `(` _FunctionParameters_<sup>?</sup> `)`\
> &nbsp;&nbsp; &nbsp;&nbsp; _FunctionReturnType_<sup>?</sup>\
> &nbsp;&nbsp; &nbsp;&nbsp; `:` [NEWLINE]\
> &nbsp;&nbsp; &nbsp;&nbsp; [INDENT]\
> &nbsp;&nbsp; &nbsp;&nbsp; _FunctionStatements_<sup>*</sup>\
> &nbsp;&nbsp; &nbsp;&nbsp; [DEDENT]\
>
> _FunctionQualifiers_ :\
> &nbsp;&nbsp; `pub`<sup>?</sup>
>
> _FunctionStatements_ :\
> &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;  [_ReturnStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_VariableDeclarationStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_AssignStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_AugmentedAssignStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_ForStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_WhileStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_IfStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_AssertStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_EmitStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_PassStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_BreakStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_ContinueStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_RevertStatement_]\
> &nbsp;&nbsp; &nbsp;&nbsp; | [_Expression_]\
>
> _FunctionParameters_ :\
> &nbsp;&nbsp; _FunctionParam_ (`,` _FunctionParam_)<sup>\*</sup> `,`<sup>?</sup>
>
> _FunctionParam_ :\
> &nbsp;&nbsp; [IDENTIFIER] `:` [_Type_]
>
> _FunctionReturnType_ :\
> &nbsp;&nbsp; `->` [_Type_]


A _function_ consists of a code block, along with a name and a set of parameters.
Other than a name, all these are optional. Functions are declared with the
keyword `def`. Functions may declare a set of *input* [*variables*][variables]
as parameters, through which the caller passes arguments into the function, and
the *output* [*type*][type] of the value the function will return to its caller
on completion.

When referred to, a _function_ yields a first-class *value* of the
corresponding zero-sized [*function item type*], which
when called evaluates to a direct call to the function.

A function header ends with a colon (`:`) after which the function body begins.

For example, this is a simple function:

```python
def answer_to_life_the_universe_and_everything() -> u256:
    return 42
```

[NEWLINE]: tokens.md#newline
[INDENT]: tokens.md#indent
[DEDENT]: tokens.md#dedent
[IDENTIFIER]: identifiers.md
[_Type_]: types.md
[type]: types.md
[_function_]: function_item_types.md
[*function item type*]: function_item_types.md
[variables]: variables.md

[_ReturnStatement_]: statements.md
[_VariableDeclarationStatement_]: statements.md
[_AssignStatement_]: statements.md
[_AugmentedAssignStatement_]: statements.md
[_ForStatement_]: statements.md
[_WhileStatement_]: statements.md
[_IfStatement_]: statements.md
[_AssertStatement_]: statements.md
[_EmitStatement_]: statements.md
[_PassStatement_]: statements.md
[_BreakStatement_]: statements.md
[_ContinueStatement_]: statements.md
[_RevertStatement_]: statements.md
[_Expression_]: expressions.md