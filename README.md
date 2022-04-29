# label-test
Repository to test use of GitHub labels

## Label with period

The example label https://github.com/MikeMcC399/label-test/labels/to%2Edo includes a `.` in its name. If the URL for this label is copied using browser right-click and `Copy link address` and the label is then pasted into a GitHub Markdown document, the label will not be rendered. Instead the URL is shown.

To workaround this issue, the copied URL `https://github.com/MikeMcC399/label-test/labels/to.do` needs to be manually edited and the `.`character replaced by its escaped form `%2E`, so the URL becomes `https://github.com/MikeMcC399/label-test/labels/to%2Edo` which is then correctly rendered as https://github.com/MikeMcC399/label-test/labels/to%2Edo.

## Problematic HTML code

The label view https://github.com/MikeMcC399/label-test/labels displays the label using the following HTML code

```
<a id="label-c39a93" href="/MikeMcC399/label-test/labels/to.do" data-name="to.do" style="--label-r:14;--label-g:138;--label-b:22;--label-h:123;--label-s:81;--label-l:29;" data-view-component="true" class="IssueLabel hx_IssueLabel IssueLabel--big lh-condensed js-label-link d-inline-block v-align-top">
        <span>to.do</span>
</a>
```

Since the `.` character is not escaped in `href="/MikeMcC399/label-test/labels/to.do"` it will be copied exactly in this form by a browser `Copy link address` action.

## Feedback

This issue has been entered as feedback on https://github.com/github/feedback/discussions/15742
