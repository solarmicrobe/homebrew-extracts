# Solarmicrobe Extracts

## How do I install these formulae?

`brew install solarmicrobe/extracts/<formula>`

Or `brew tap solarmicrobe/extracts` and then `brew install <formula>`.

## Documentation

`brew help`, `man brew` or check [Homebrew's documentation](https://docs.brew.sh).

### RPM
Due to [RPM Upstream](https://github.com/rpm-software-management/rpm/issues/2222#issuecomment-1693170271) the rpm tools are no longer supported on MacOS. Version 4.18.1
of the formulae is the last supported.

You may need the edit before install will work
```
brew tap solarmicrobe/extracts
brew edit
## And add the line below to the beginning of the install method:
ENV.append_to_cflags "-Wno-implicit-function-declaration" if DevelopmentTools.clang_build_version >= 1403
## Save and continue
brew install solarmicrobe/extracts/rpm@4.18.1
```

