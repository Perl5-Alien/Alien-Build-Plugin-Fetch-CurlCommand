# Alien::Build::Plugin::Fetch::CurlCommand [![Build Status](https://secure.travis-ci.org/plicease/Alien-Build-Plugin-Fetch-CurlCommand.png)](http://travis-ci.org/plicease/Alien-Build-Plugin-Fetch-CurlCommand)

Curl command line plugin for fetching files

# SYNOPSIS

    use alienfile;
    
    share {
      meta->prop->{start_url} = 'https://www.openssl.org/source/';
      plugin 'Fetch::CurlCommand';
    
    };

# DESCRIPTION

This plugin provides a fetch based on the `curl` command.  It works with other fetch
plugins (ie. the first one which succeeds will be used).  Most of the time the best plugin
to use will be [Alien::Build::Plugin::Download::Negotiate](https://metacpan.org/pod/Alien::Build::Plugin::Download::Negotiate), but for some SSL bootstraping
it may be desirable to try `curl` first.

This plugin is not currently part of the [Alien::Build](https://metacpan.org/pod/Alien::Build) core, but the hope is that it
will be declared stable enough in the near future to be included.

# PROPERTIES

## curl\_command

The full path to the `curl` command.  The default is usually correct.

## ssl

Ignored by this plugin.  Provided for compatbility with some other fetch plugins.

# SEE ALSO

- [alienfile](https://metacpan.org/pod/alienfile)
- [Alien::Build](https://metacpan.org/pod/Alien::Build)

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2017 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
