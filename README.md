# Droid Module: ssh-known-hosts

Add SSH public keys to known_hosts. For more information on Droid, please see
[droidphp.com](http://droidphp.com).

The steps involved are:-

1. Create `~/.ssh/known_hosts` if it does not exist.
2. Add a list of public keys to `known_hosts`.
3. Hash any unhashed entries in `known_hosts`.
4. Remove the `known_hosts.old` generated in the previous step.


## Assumptions

1. The platform is Debian-based.


## Limitations

None.


## Information required by the module

1. A list of one or more entries for the `known_hosts` file:

        variables:
          third_party_public_ssh_keys:
            - [<string>, <string>]
            - ...
   The first string in an entry should be the host name and IP address of the
   SSH host and the second string should be its public key, for example:-

        ["github.com,192.30.253.112", "ssh-rsa AAAA..."]

## Optional information

None.
