# Bug Notes

| Bug | Evidence / Failed Test | Cause | Fix |
|---|---|---|---|
| Average calculation | `135.0` returned instead of `90.0`; one mark caused division by zero | The code divided by `len(marks) - 1` | Divide by `len(marks)` |
| Pass boundary | `is_passing(40)` returned `False` | The code used `>` instead of `>=` | Use `>= PASS_MARK` |
| Distinction grade | `get_grade(95)` returned `First` | The `>= 60` condition appeared before `>= 90` | Check `>= 90` first |
