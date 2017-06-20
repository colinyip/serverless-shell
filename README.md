# Serverless Shell

[![Greenkeeper badge](https://badges.greenkeeper.io/UnitedIncome/serverless-shell.svg)](https://greenkeeper.io/)

[![serverless](http://public.serverless.com/badges/v3.svg)](http://www.serverless.com)
[![npm](https://nodei.co/npm/serverless-shell.png?mini=true)](https://www.npmjs.com/package/serverless-shell)

A Serverless v1.0 plugin to drop to a local shell with your environment
variables from `serverless.yml`.


## Install

```
npm install --save serverless-shell
```

Add the plugin to your `serverless.yml`:

```yaml
plugins:
  - serverless-shell
```

## Usage
Example in a python project
```
$ serverless shell
Serverless: Spawning python3.6...
Python 3.6.1 (default, Mar 22 2017, 06:17:05) 
[GCC 6.3.0 20170321] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```
and in a NodeJS project:
```
$ serverless shell
Serverless: Dropping to repl...
>  
```

### Per function & stage specific env vars
Since the main reason for building this was to test code with the configs for
various stages, it supports properly building the environment. For example:
```
$ serverless -s staging shell -f status
```
