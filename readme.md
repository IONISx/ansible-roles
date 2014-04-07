# ansible-roles

> A few ansible roles that we use here, at @IONISx.

## Roles

Here’s a small documentation about the roles you can find here.


### Base role : `base`

All roles should depend on the `base` role.  
It installs a few dependencies required by some ansible tasks, it also installs git and ntp.

If you define a `mirror_apt_url`, apt will be configured to point to that URL. So install `apt_cacher_ng`, then define that variable somewhere in your playbooks.


### Base role : `base_nodejs`

*Dependencies*: `base`

All nodejs applications should depend on the `base_nodejs` role.  
It builds a recent version of nodejs.

If you define a `mirror_npm_url`, npm will be (globally) configured to point to that URL. So install `sinopia`, then define that variable somewhere in your playbooks.


### `apt_cacher_ng`

*Dependencies*: `base`

Installs apt-cacher-ng.


### `sinopia`

*Dependencies*: `base_nodejs`

Installs sinopia.


## License
[MIT License](http://en.wikipedia.org/wiki/MIT_License)
