# Security

Please report vulnerabilities privately, through GitHub's **Report a vulnerability**
button on the repository's Security tab. Don't open a public issue for them.

The tools where this matters most:

- **chatlens** runs a local web server holding conversation data. Anything that lets
  another web page, another site or another origin read from or write to it is in scope.
- **skill-preflight** is a pre-install check. A skill that makes it read files outside the
  skill directory, or hides a capability or a change from `diff`, is in scope. A skill
  that simply evades its pattern rules isn't a vulnerability, since the README says the
  rules can be evaded, but a report is still welcome as an ordinary issue.
- **parda** and **chat2faq** handle personal data. A way to make either one write a
  value it detected to its output, logs or disk is in scope. A value it fails to detect is
  a detection miss: report it as an issue, with the identifier replaced by a fake one
  of the same shape.
- **turncheck** runs the command you give it. That is its job, so running your own agent
  isn't a vulnerability; a scenario file that makes it run something else would be.

Only the latest release of each tool gets fixes. One person maintains these, so there is
no fixed response time, but security reports are read first.
