# browserify administration handbook

This document is for members of the browserify org.

The sections below document administrative procedures for adding packages,
adding new users, and some tips on handling issues and pull requests.

# principles

* avoid human bottlenecks
* trust people to do the right thing (until proven otherwise)

In order to minimize human bottlenecks, all members should be fully empowered to
do everything that might be necessary to handle administration of the project.

For some actions, it might be good to discuss with other members and the
community about the best course of action. For other decisions, it might be
better to take individual initiative.

# adding new members

New members should be added liberally! If you identify someone who is interested
in contributing to core or any of the browserify satellite projects, seems
trustworthy, and agrees to the [code of conduct][], you can follow the steps
below. You should feel individually empowered to make a decision.

New members should be added as owners on github and npm.

For github:

Visit https://github.com/orgs/browserify/people and click the green "invite
member" button. Type in the github username and add the new member as an owner.

For npm:

Visit https://www.npmjs.com/org/browserify/members and type in the npm user
name. Set the radio button to "owner" then click the red "add member" button.

[code of conduct]: https://raw.githubusercontent.com/browserify/browserify/master/code-of-conduct.md

# adding a package to the browserify org

To add a package to the browserify org, you will need to transfer ownership on
github as well as add the package to the browserify org on npm.

For github:

Visit the project page settings for a github user `$USER` and a project name
`$PROJECT` at:

https://github.com/$USER/$PROJECT/settings

At the bottom in the "danger zone" box, click "transfer ownership".

Type the name of the repository to confirm and below that box, type "browserify"
in the field labeled "new owner's github username or organization name".

For npm, run this command, replacing `$PKGNAME` with the name of the package on
npm:

```
npm access grant read-write browserify:developers $PKGNAME
```

