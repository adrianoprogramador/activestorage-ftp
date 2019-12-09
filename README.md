# ActiveStorage FTP Service

FTP Active Storage service.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'activestorage-ftp'
```

And then execute:

```bash
$ bundle install
```

## Usage

config/storage.yml

```yml
production:
  service: Ftp
  ftp_host: <%= ENV["FTP_HOST"] %>
  ftp_port: <%= ENV["FTP_PORT"] %>
  ftp_user: <%= ENV["FTP_USER"] %>
  ftp_passwd: <%= ENV["FTP_PASSWD"] %>
  ftp_folder: <%= ENV["FTP_FOLDER"] %>
  ftp_url: <%= ENV["FTP_URL"] %>
  # optional
  ftp_passive: true
  ftp_chmod: 0600
```

## Remote md5.php

rails-storage/md5.php

```php
<?php
  if(isset($_GET['file'])) {
    echo( md5_file($_GET['file']) );
  }
?>
```

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
