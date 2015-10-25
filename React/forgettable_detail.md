# Forgettable Detail

- IN **JSX**. component variable name begin with **UPPER CASE**

```
var SelfBox = React.createClass({
  render: function() {
    return (
      <div >
        Hello, world! I am a CommentBox.
      </div>
    );
  }
});
React.render(
  <SelfBox />,
  document.getElementById('example')
);

```
- Each `React.render` or `React.createClass` can only put single `＜div></div>`. Rationale should be checked.