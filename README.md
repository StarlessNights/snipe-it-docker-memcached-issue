# snipe-it-docker-memcached-issue
This repository simply reproduces an issue related to snipe-it and memcached.

You will encounter this error when running this docker-compose project.

```
Error
snipeit                                      |
snipeit                                      |   Class 'Memcached' not found
snipeit                                      |
snipeit                                      |   at vendor/laravel/framework/src/Illuminate/Cache/MemcachedConnector.php:69
snipeit                                      |      65▕      * @return \Memcached
snipeit                                      |      66▕      */
snipeit                                      |      67▕     protected function createMemcachedInstance($connectionId)
snipeit                                      |      68▕     {
snipeit                                      |   ➜  69▕         return empty($connectionId) ? new Memcached : new Memcached($connectionId);
snipeit                                      |      70▕     }
snipeit                                      |      71▕
snipeit                                      |      72▕     /**
snipeit                                      |      73▕      * Set the SASL credentials on the Memcached connection.
snipeit                                      |
snipeit                                      |   • A class import is missing: You have a missing class import. Try importing this class: `League\Flysystem\Cached\Storage\Memcached`.
```
