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

github "boxen", "3.7.0"

# Support for default hiera data in modules

github "module_data", "0.0.3", :repo => "ripienaar/puppet-module-data"

# Core modules for a basic development environment. You can replace
# some/most of these if you want, but it's not recommended.

github "dnsmasq",     "2.0.1"
github "foreman",     "1.2.0"
github "gcc",         "2.2.0"
github "git",         "2.7.1"
github "go",          "2.1.0"
github "homebrew",    "1.9.8"
github "hub",         "1.3.0"
github "inifile",     "1.2.0", :repo => "puppetlabs/puppetlabs-inifile"
github "nginx",       "1.4.4"
github "nodejs",      "4.0.0"
github "openssl",     "1.0.0"
github "phantomjs",   "2.3.0"
github "pkgconfig",   "1.0.0"
github "repository",  "2.3.0"
github "ruby",        "8.1.7"
github "stdlib",      "4.2.1", :repo => "puppetlabs/puppetlabs-stdlib"
github "sudo",        "1.0.0"
github "xquartz",     "1.2.1"

# Optional/custom modules. There are tons available at
# https://github.com/boxen.

github "appcleaner",     "1.0.0"
github "alfred",         "1.3.1"
github "atom",           "1.1.0"
github "autoconf",       "1.0.0"
github "bash",           "1.2.0"
github "brewcask",       "0.0.5", :repo => "phinze/puppet-brewcask"
github "caffeine",       "1.0.0"
github "chrome",         "1.2.0"
github "codekit",         "1.0.3"
github "cyberduck",      "1.0.0"
github "dropbox",        "1.4.1"
github "docker",         "0.8.0", :repo => "jamieconnolly/puppet-docker"
github "elixir",         "0.0.1"
github "evernote",       "2.0.6"
github "iterm2",         "1.0.0"
github "fig",            "1.0.0"
github "java",        	 "1.8.0"
github "firefox",        "1.2.3"
github "github_for_mac", "1.4.0", :repo => "dieterdemeyer/puppet-github_for_mac"
github "gitx",           "1.2.0"
github "gpgtools",       "1.0.3"
github "googledrive",    "1.0.2", :repo => "gblair/puppet-googledrive"
github "heroku",         "2.1.1"
github "iterm2",         "1.2.2"
github "launchbar",      "1.2.0", :repo => "dieterdemeyer/puppet-launchbar"
github "macvim",         "1.0.0"
github "mou",            "1.1.3"
github "ohmyzsh",        "1.0.0", :repo => "samjsharpe/puppet-ohmyzsh"
github "onepassword",    "1.1.5"
github "osx",            "2.8.0"
github "osxfuse",        "1.3.0"
github "packer",         "1.3.0"
github “postgresql”,	 “3.0.1”
github "perl",           "1.1.0", :repo => "boxelly/puppet-perl"
github "quicksilver",    "1.3.0"
github "python",         "2.0.0"
github "qt",             "1.3.1"
github "screen",         "1.0.0"
github "skype",          "1.0.9"
github "sourcecodepro",  "1.0.0", :repo => "thisishugo/puppet-sourcecodepro"
github "sourcetree",     "1.0.0"
github "sparrow",        "1.0.0"
github "sublime_text_3", "1.0.3", :repo => "jozefizso/puppet-sublime_text_3"
github "sysctl",         "1.0.1"
github "tmux",           "1.0.0"
github "vlc",            "1.1.0"
github "unarchiver",     "1.5.0", :repo => "dieterdemeyer/puppet-unarchiver"
github "vagrant",        "3.2.1"
github "vagrant-manager","0.0.1"
github "vim",            "1.0.5"
github "virtualbox",     "1.0.10"
github "vmware_fusion",  "1.2.0"
github "wget",           "1.0.1"
github "zsh",            "1.0.0"
