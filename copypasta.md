Layout HTML

```jade
div
  nav.top-nav.top-nav-light.cf(role='navigation')
    input#menu-toggle.menu-toggle(type='checkbox')
    label(htmlfor='menu-toggle') Menu
    ul.list-unstyled.list-inline.cf
      li Labelr
      li
        a(href='/repos') Repos
      li.pull-right
        a(href='/logout') Logout
  .container
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
<div class='container'>
  <header role='banner'>
    <h1>Labelr</h1>
  </header>
  <div>
    <p>We label stuff for you, because, we can&trade;</p>
    <a href='/login' class='button button-large'>
      <span class='mega-octicon octicon-mark-github'></span> Login with GitHub
    </a>
  </div>
</div>
```

```
.container
  header(role='banner')
    h1 Labelr
  div
    p We label stuff for you, because, we can&trade;
    a.button.button-large(href='/login')
      span.mega-octicon.octicon-mark-github Login with GitHub
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


Repo Detail

```
.container
  h1
  p
  ul
```

Labels

```
<form class='label'>
  <span class='label-color avatar avatar-small avatar-rounded'>&nbsp;</span>
  <input name='name'/>
  <input name='color'/>
  <button type='submit' class='button button-small'>Save</button>
  <button type='button' class='button button-small button-unstyled'>cancel</button>
</form>
```

```
form.label
  span.label-color.avatar.avatar-small.avatar-rounded &nbsp;
  input(name='name')
  input(name='color')
  button.button.button-small(type='submit') Save
  button.button.button-small.button-unstyled(type='button') cancel
```

```
.label
  span.label-color &nbsp;
  span
  span.octicon.octicon-pencil
  span.octicon.octicon-x
```

For instructor

```
"commit": "git add --all && git commit -am \"$(date)\" && npm version minor && git push origin master --tags",
```
