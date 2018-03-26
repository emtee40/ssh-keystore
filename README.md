# coltondrg?'s ssh keystore

This is a place where I store the id_rsa.pub files for all of my computers. An `authorized_keys` file can easily be generated and installed via the `./install` script.

The canonical version of this repo is at [drg git](https://git.drg.li/ColtonDRG/ssh-keystore), however, a mirror is available at [GitHub](https://github.com/ColtonDRG/ssh-keystore) for convenience.

An http-accessible copy of these, including a pre-generated `authorized_keys` file is available at https://security.coltondrg.com/ssh/

## Quick installation

### Using git

##### From drg git
```sh
git clone https://git.drg.li/coltondrg/ssh-keystore.git
cd ssh-keystore
./install
```

##### From GitHub
```sh
git clone https://github.com/coltondrg/ssh-keystore.git
cd ssh-keystore
./install
```

##### Updating
```sh
cd ssh-keystore
git pull
./install
```

The install script also supports cron. By running it with `--cron`, it will automatically fetch the latest commit and install without confirmation.

### Using curl/wget

##### From security.coltondrg.com via curl
```sh
curl -O https://security.coltondrg.com/ssh/authorized_keys
cp authorized_keys ~/.ssh/authorized_keys
```

##### From security.coltondrg.com via wget
```sh
wget https://security.coltondrg.com/ssh/authroized_keys
cp authorized_keys ~/.ssh/authorized_keys
```

For updates, simply repeat the process.

### Other notes

In the extras directory you'll find keys that are not included in the authorized_keys file generated by the installer script, but are kept here for dexterity anyway. You can also find an example of a postinstall script you can use to extend the functionality of the installer script, including to add some of these extra keys to the generated authorized_keys file.
