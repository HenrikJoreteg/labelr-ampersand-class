Layout HTML

```jade
body
  nav.top-nav.top-nav-light.cf(data-hook='navbar', role='navigation')
    input#menu-toggle.menu-toggle(type='checkbox')
    label(for='menu-toggle') Menu
    ul.list-unstyled.list-inline.cf
      li Labelr
      li
        a(href='/repos') Repos
      li.pull-right
        span(data-hook='username')
        |
        a(href='/logout') Logout
  .container(data-hook='page-container')

```

GitHub auth

```
'https://github.com/login/oauth/authorize?' + x
```

```
{
  scope: 'user,repo',
  redirect_uri: {something} + '/auth/callback',
  client_id: 'f8dd69187841cdd22a26'
}
```

```
http://labelr-dev.herokuapp.com/authenticate/CODE'
```

Login page:


```
section.page
  header(role='banner')
    h1 Labelr
  div
    p We label stuff for you, because, we can&trade;
    a.button.button-large(href='/login')
      span.mega-octicon.octicon-mark-github
      |  Login with GitHub

```

Styles

```
header
  padding-top: 50px

.label
  height: 40px

  .label-color
    width: 24px
    height: 24px
    border: 1px solid grey
    border-radius: 20px
    display: inline-block

  > span
    margin-left: 10px
    margin-right: 10px

```

Repos Page

```
section.page
  h1 Repos

  div(data-hook='repo-container')

```

Repo Detail Page

```
section.page
  h1(data-hook='title')
  p
    button.button(data-hook='add-label') Add New

  ul(data-hook='label-container')

```

Repo Item

```
div
  span.octicon.octicon-repo
    a(data-hook='link')

```

Labels


```
div
  form.label(data-hook='editing')
    span.label-color(data-hook='color-dot') &nbsp;
    input(name='name')
    input(name='color')
    button.button.button-small(type='submit') Save
    button.button.button-small.button-unstyled(type='button', data-hook='cancel') cancel

  .label(data-hook='viewing')
    span.label-color(data-hook='color-dot') &nbsp;
    span(data-hook='name')
    span.octicon.octicon-pencil(data-hook='edit')
    span.octicon.octicon-x(data-hook='delete')
```

For instructor

```
"commit": "git add --all && git commit -am \"$(date)\" && npm version minor && git push origin master --tags",
```
