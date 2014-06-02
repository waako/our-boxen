# This file manages Puppet module dependencies.
#
# It works a lot like Bundler. We provide some core modules by
# default. This ensures at least the ability to construct a basic
# environment.

# Shortcut for a module from GitHub's boxen organization
def github(name, *args)
  options ||= if args.last.is_a? Hash
    args.last
  else
    {}
  end

  if path = options.delete(:path)
    mod name, :path => path
  else
    version = args.first
    options[:repo] ||= "boxen/puppet-#{name}"
    mod name, version, :github_tarball => options[:repo]
  end
end

# Shortcut for a module under development
def dev(name, *args)
  mod name, :path => "#{ENV['HOME']}/src/boxen/puppet-#{name}"
end

# Includes many of our custom types and providers, as well as global
# config. Required.

github "boxen", "3.4.2"

# Support for default hiera data in modules

github "module-data", "0.0.3", :repo => "ripienaar/puppet-module-data"

# Core modules for a basic development environment. You can replace
# some/most of these if you want, but it's not recommended.

github "dnsmasq",     "1.0.1"
github "foreman",     "1.2.0"
github "gcc",         "2.0.100"
github "git",         "2.3.1"
github "go",          "1.1.0"
github "homebrew",    "1.9.2"
github "hub",         "1.3.0"
github "inifile",     "1.0.3", :repo => "puppetlabs/puppetlabs-inifile"
github "nginx",       "1.4.3"
github "nodejs",      "3.7.0"
github "openssl",     "1.0.0"
github "phantomjs",   "2.3.0"
github "pkgconfig",   "1.0.0"
github "repository",  "2.3.0"
github "ruby",        "7.3.0"
github "stdlib",      "4.1.0", :repo => "puppetlabs/puppetlabs-stdlib"
github "sudo",        "1.0.0"
github "xquartz",     "1.1.1"

# Optional/custom modules. There are tons available at
# https://github.com/boxen.

# github "vagrant",     "1.6.2"
# github "sublime_text","1.0.0"
# github "iterm2",      "1.1.0"
# github "osx",         "2.5.0"
# github "opera",       "0.3.3"
# github "dockutil",    "0.2.1"
# github "linkinus",    "1.0.3"
# github "evernote",    "2.0.6"
# github "firefox",     "1.2.1"
# github "gh",          "2.0.0"
# github "git",         "2.3.1"
# github "skype",       "1.0.8"
# github "wget",        "1.0.1"
# github "php",         "1.2.2"
# github "homebrew",    "1.9.2"
# github "gpgtools",    "0.1.1"
# github "alfred",      "1.1.8"
# github "vlc",         "1.1.0"
# github "copy",        "1.0.1"
# github "virtualbox",  "1.0.9"
# github "flux",        "1.0.1"
# github "fluid",       "1.0.1"
# github "keyremap4macbook",  "1.2.2"
# github "mysql",       "1.99.9"
# github "memcached",   "2.0.0"
# github "repository",  "2.3.0"
# github "hub",         "1.3.0"
# github "onepassword", "1.1.0"
# github "dropbox",     "1.2.0"
# github "dash",        "1.0.0"
# github "daisy_disk",  "1.0.1"
# github "sequel_pro",  "1.0.1"
# github "zsh",         "1.0.0"
# github "xscope",      "1.0.0"
