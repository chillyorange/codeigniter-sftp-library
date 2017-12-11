codeigniter-sftp-library
========================

## Overview

SFTP library for CodeIgniter 3+

This is a Library for CodeIgniter 3+ that uses sFTP. Usage keept as simple as CodeIgniter's default FTP library.


## Requirements

1.  PHP 5.4+
2.  CodeIgniter 3+
3.  PECL SSH2 Extension

## Installation

Drop this file into the ./application/libraries/ folder in your CodeIgniter installation.

## Usage

This lib has the same methods as the CodeIgniter FTP Class.

## Example (username/password)

```
$this->load->library('sftp');

$config['hostname'] = 'ssh.example.com';
$config['username'] = 'your-username';
$config['password'] = 'your-password';

$this->sftp->connect($config);

$this->sftp->upload('/local/path/to/myfile.html', '/public_html/myfile.html', 'ascii', 0644);

$this->sftp->close();
```