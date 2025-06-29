Changelog
=========

.. towncrier release notes start

django-redis 6.0.0 (2025-06-17)
===============================

Features
--------

- Support HashMaps (`#598 <https://github.com/jazzband/django-redis/issues/598>`_)
- Support gzip compression (`#688 <https://github.com/jazzband/django-redis/issues/688>`_)
- Support for sets and support basic operations, sadd, scard, sdiff, sdiffstore, sinter, sinterstore, smismember, sismember, smembers, smove, spop, srandmember, srem, sscan, sscan_iter, sunion, sunionstore (`#730 <https://github.com/jazzband/django-redis/issues/730>`_)


Bug Fixes
---------

- Hotfix for timeout=DEFAULT_TIMEOUT in expire and pexpire (`#724 <https://github.com/jazzband/django-redis/issues/724>`_)
- Fix is_master parsing error for write separation in sentinel mode (`#749 <https://github.com/jazzband/django-redis/issues/749>`_)
- Added blocking parameter for `cache.lock` (`#752 <https://github.com/jazzband/django-redis/issues/752>`_)


Miscellaneous
-------------

- Added support for Python 3.12 (`#689 <https://github.com/jazzband/django-redis/issues/689>`_)
- Pin pytest to <7.0 until compatibility issues are resolved (`#690 <https://github.com/jazzband/django-redis/issues/690>`_)
- Replace isort and flake8 with ruff (`#692 <https://github.com/jazzband/django-redis/issues/692>`_)
- Drop django 4.0 (`#693 <https://github.com/jazzband/django-redis/issues/693>`_)
- Upgrade black to 23.10.1 (`#695 <https://github.com/jazzband/django-redis/issues/695>`_)
- Typed DefaultClient (`#696 <https://github.com/jazzband/django-redis/issues/696>`_)
- Support pytest>=7 (`#697 <https://github.com/jazzband/django-redis/issues/697>`_)
- Drop support for django 3.2, python 3.6 and python 3.7 (`#699 <https://github.com/jazzband/django-redis/issues/699>`_)
- Support tox 4 (`#701 <https://github.com/jazzband/django-redis/issues/701>`_)
- Configured dependabot for github actions (`#702 <https://github.com/jazzband/django-redis/issues/702>`_)
- Use ubuntu-latest for CI (`#703 <https://github.com/jazzband/django-redis/issues/703>`_)
- Dropped support for django 4.1 and added support for django 5.0 (`#729 <https://github.com/jazzband/django-redis/issues/729>`_)
- Added support for django 5.1 (`#754 <https://github.com/jazzband/django-redis/issues/754>`_)
- Update minimum supported versions in README.md: Python to 3.8, Django to 4.2, redis-py to 4.0.2 (`#755 <https://github.com/jazzband/django-redis/issues/755>`_)
- Added support for Python 3.13 (`#756 <https://github.com/jazzband/django-redis/issues/756>`_)
- Speed up tests by using `pytest-xdist` and separating settings on different redis databases.
  Dropped `pytest-django`
  Using `docker-compose` for setting up redis containers for testing
  Use `tox-uv` (`#757 <https://github.com/jazzband/django-redis/issues/757>`_)
- Confirm support for Django 5.2.
  Fix shadowing builtin Python exceptions. (`#824 <https://github.com/jazzband/django-redis/issues/824>`_)


Deprecations and Removals
-------------------------

- Drop support for Python 3.8 (`#852 <https://github.com/jazzband/django-redis/issues/852>`_)


django-redis 5.4.0 (2023-10-01)
===============================

Features
--------

- Connection factory goes to cache options (`#680 <https://github.com/jazzband/django-redis/issues/680>`_)


Documentation
-------------

- Added note in docs for correctly configuring hiredis parser when using redis-py version 5. (`#677 <https://github.com/jazzband/django-redis/issues/677>`_)


django-redis 5.3.0 (2023-06-16)
===============================

Features
--------

- Add support for django 4 (`#627 <https://github.com/jazzband/django-redis/issues/627>`_)


Bug Fixes
---------

- Access `django_redis.cache.DJANGO_REDIS_SCAN_ITERSIZE` and `django_redis.client.herd.CACHE_HERD_TIMEOUT` in runtime to not read Django settings in import time. (`#638 <https://github.com/jazzband/django-redis/issues/638>`_)
- Skipping pickle serializer test for django >= 4.2 (`#646 <https://github.com/jazzband/django-redis/issues/646>`_)


Miscellaneous
-------------

- Speed up deleting multiple keys by a pattern with pipelines and larger itersize (`#609 <https://github.com/jazzband/django-redis/issues/609>`_)
- Print full exception traceback when logging ignored exceptions (`#611 <https://github.com/jazzband/django-redis/issues/611>`_)
- Fix mypy linting (`#626 <https://github.com/jazzband/django-redis/issues/626>`_)
- Added support for python 3.11 (`#633 <https://github.com/jazzband/django-redis/issues/633>`_)
- Fix CI, running tox<4 to still support Python 3.6. (`#645 <https://github.com/jazzband/django-redis/issues/645>`_)
- Dropped support for django 2.2 and 3.1 (`#649 <https://github.com/jazzband/django-redis/issues/649>`_)
- Run actions & tox against Django 4..2 (`#668 <https://github.com/jazzband/django-redis/issues/668>`_)


django-redis 5.2.0 (2021-12-22)
===============================

Bug Fixes
---------

- Block use with broken redis-py 4.0.0 and 4.0.1 (`#542 <https://github.com/jazzband/django-redis/issues/542>`_)


Miscellaneous
-------------

- Unblock redis-py >=4.0.2 (`#576 <https://github.com/jazzband/django-redis/issues/576>`_)
- Add support for django 4 (`#579 <https://github.com/jazzband/django-redis/issues/579>`_)


Django_Redis 5.1.0 (2021-11-29)
===============================

Features
--------

- Add Python 3.10 to CI (`#536 <https://github.com/jazzband/django-redis/issues/536>`_)
- Configured ``towncrier`` to generate the changelog. (`#548 <https://github.com/jazzband/django-redis/issues/548>`_)
- Added ``django_redis.compressors.zstd.ZStdCompressor`` to provide ``pyzstd`` cache value compression. (`#551 <https://github.com/jazzband/django-redis/issues/551>`_)
- Change pickle default version to Python default instead of highest version. (`#555 <https://github.com/jazzband/django-redis/issues/555>`_)
- Add ``hiredis`` extra dependency to request ``redis[hiredis]``. (`#556 <https://github.com/jazzband/django-redis/issues/556>`_)
- Add pexpireat to allow setting 'expire at' with millisecond precision. (`#564 <https://github.com/jazzband/django-redis/issues/564>`_)


Bug Fixes
---------

- Make expire, pexpire, expireat and persist return the redis client value (`#564 <https://github.com/jazzband/django-redis/issues/564>`_)


Miscellaneous
-------------

- Convert most unittest class tests to pytest tests. (`#553 <https://github.com/jazzband/django-redis/issues/553>`_)
- Update type comments to type annotations. (`#568 <https://github.com/jazzband/django-redis/issues/568>`_)
- Pin redis-py to 3.x until 4.x breaking changes can be addressed. (`#570 <https://github.com/jazzband/django-redis/issues/570>`_)


Documentation
-------------

- Clarify redis primary name in sentinel documentation. (`#529 <https://github.com/jazzband/django-redis/issues/529>`_)
- Add documentation on configuring self signed SSL certificates. (`#559 <https://github.com/jazzband/django-redis/issues/559>`_)


django-redis 5.0.0 (2021-05-30)
===============================

- supporting django 3.1 and django 3.2
- dropped support for python 3.5
- added support for python 3.9
- started type hinting the codebase
- ensure connections are closed
- fixed ``ShardClient`` ``.clear()`` method
- ``.delete()`` now returns boolean from django 3.1 onwards
- disconnect connection pools on ``.close()``
- added support for redis sentinel
- added ``.expire_at()`` method
- fixed ``.incr()`` when ttl is ``None`` or when the number is larger than 64 bit
- fixed ``.incr_version()`` when ttl is ``None``
- added ``.pttl()`` method to the clients to support milli-second precision for
  ttl of a key
- added ``.pexpire()`` method to the clients to support milli-second precision
  for setting expiry of a key


django-redis 4.12.1 (2020-05-27)
================================

- No code changes.
- Fixed a typo in setup.cfg metadata preventing a successful release.


django-redis 4.12.0 (2020-05-27)
================================

- The project has moved to `Jazzband <https://jazzband.co/>`_. This is the
  first release under the new organization. The new repository URL is
  `<https://github.com/jazzband/django-redis>`_.
- Removed support for end-of-life Django < 2.2.
- Removed support for unmaintained redis-py 2.X.
- Changed uses of deprecated ``smart_text()`` to ``smart_str()``.
- Fixed deprecation warning with the msgpack serializer.
- The ``.touch()`` method now uses the default timeout, to cache forever pass
  ``None``.
- Subclasses of ``JSONSerializer`` can now override the ``encoder_class``
  attribute to change the JSON encoder. It defaults to ``DjangoJSONEncoder``.
- Fixed ``DefaultClient.set()`` to work with empty ``Pipeline``.
- The ``thread_local`` parameter is now forwarded to the Redis client.


django-redis 4.11.0 (2019-12-13)
================================

- Removed support for Python 2.7 and 3.4.
- Removed support for Django 2.0 and 2.1.
- Added support for Python 3.8.
- Added support for Django 2.2 and 3.0.
- Changed msgpack-python soft dependency to msgpack.
- Fixed ``.touch()`` method for sharded client.
- Fixed prefix escaping for the sharded client.
- Fixed ``.add()`` method to return a bool.


django-redis 4.10.0 (2018-10-19)
================================

- Add support and testing for Django 2.1 and Python 3.7. No actual code changes
  were required.
- Add support for redis-py 3.0.
- Add touch command.


django-redis 4.9.1 (2018-10-19)
===============================

- Pin redis version to 2.10.6


django-redis 4.9.0 (2018-03-01)
===============================

- Add testing and support for Django 2.0. No actual code changes were required.
- Escape ``KEY_PREFIX`` and ``VERSION`` when used in glob expressions.
- Improve handling timeouts less than 1ms.
- Remove fakeredis support.
- Add datetime, date, time, and timedelta serialization support to the JSON
  serializer.
- The deprecated feature of passing ``True`` as a timeout value is no longer
  supported.
- Fix ``add()`` with a negative timeout to not store key (it is immediately
  invalid).
- Remove support for Django < 1.11.
- Add support for atomic incr if key is not set.


django-redis 4.8.0 (2017-04-25)
===============================

- Drop deprecated exception with typo ConnectionInterrumped. Use
  ConnectionInterrupted instead.
- Remove many workarounds related to old and not supported versions
  of django and redis-py.
- Code cleaning and flake8 compliance fixes.
- Add better impl for ``close`` method.
- Fix compatibility warnings with python 3.6


django-redis 4.7.0 (2017-01-02)
===============================

- Add the ability to enable write to replica servers when the primary server is
  not available.
- Add ``itersize`` parameter to ``delete_pattern``.


django-redis 4.6.0 (2016-11-02)
===============================

- Fix incorrect behavior of ``clear()`` method.


django-redis 4.5.0 (2016-09-21)
===============================

- Now only support Django 1.8 and above. Support for older versions has been dropped.
- Remove undocumented and deprecated support for old connection string format.
- Add support for ``PASSWORD`` option (useful when the password contains url unsafe
  characters).
- Make the package compatible with fake redis.
- Fix compatibility issues with latest django version (1.10).


django-redis 4.4.4 (2016-07-25)
===============================

- Fix possible race condition on incr implementation using
  lua script (thanks to @prokaktus).


django-redis 4.4.3 (2016-05-17)
===============================

- Fix minor ttl inconsistencies.


django-redis 4.4.2 (2016-04-21)
===============================

- Fix timeout bug (thanks to @skorokithakis)


django-redis 4.4.1 (2016-04-13)
===============================

- Add additional check for avoid wrong exception on ``get_redis_connection``.


django-redis 4.4.0 (2016-04-12)
===============================

- Make redis client pluggable (thanks to @arnuschky)
- Add version number inside python module (thanks to @BertrandBordage)
- Fix clear method (thanks to @ostcar)
- Add the ability to specify key prefix on delete and delete_pattern.
- BREAKING CHANGE: improved compression support (make it more plugable).


django-redis 4.3.0 (2015-10-31)
===============================

- Improved exception handling in herd client (thanks to @brandoshmando)
- Fix bug that not allows use generators on delete_many (thanks to @ostcar).
- Remove obsolete code that makes hard dependency to mspack.


django-redis 4.2.0 (2015-07-03)
===============================

- Add ``persist`` and ``expire`` methods.
- Remove old and broken dummy client.
- Expose a redis lock method.


django-redis 4.1.0 (2015-06-15)
===============================

- Add plugable serializers architecture (thanks to @jdufresne)
- Add json serializer (thanks to @jdufresne)
- Add msgpack serializer (thanks to @uditagarwal)
- Implement delete_pattern using iter_scan for better performance (thanks to @lenzenmi)


django-redis 4.0.0
==================

- Remove usage of deprecated ``get_cache`` method.
- Added connection option SOCKET_CONNECT_TIMEOUT. [Jorge C. Leitão].
- Replace ``setex`` and friends with set, because it now supports all need for atomic.
  updates (thanks to @23doors) (re revert changes from 3.8.x branch).
- Fix django 1.8 compatibilities.
- Fix django 1.9 compatibilities.
- BREAKING CHANGE: Now timeout=0 works as django specified (expires immediately)
- Now requires redis server >= 2.8
- BREAKING CHANGE: ``redis_cache`` is no longer a valid package name


django-redis 3.8.4
==================

- Backport django 1.8 fixes from master.


django-redis 3.8.3
==================

- Minor fix on regular expression for old url notation.


django-redis 3.8.2
==================

- Revert some changes from 3.8.1 that are incompatible with redis server < 2.6.12


django-redis 3.8.1
==================

- Fix documentation related to new url format.
- Fix documentation parts that uses now removed functions.
- Fix invalid url transformation from old format (password was not set properly)
- Replace setex and friends with set, because it now supports all need for atomic
  updates (thanks to @23doors).


django-redis 3.8.0
==================

- Add compression support. (Thanks to @alanjds)
- Change package name from redis_cache to django_redis.
- Add backward compatibility layer for redis_cache package name.
- BACKWARD INCOMPATIBLE CHANGE: use StrictRedis instead of Redis class of redis-py
- Add redis dummy backend for development purposes. (Thanks to @papaloizouc)
- Now use redis native url notation for connection string (the own connection string
  notation is also supported but is marked as deprecated).
- Now requires redis-py >= 2.10.0
- Remove deprecated ``raw_cache`` property from backend.


django-redis 3.7.2
==================

- Add missing forward of version parameter from ``add()`` to ``set()`` function. (by @fellowshipofone)


django-redis 3.7.1
==================

- Improve docs (by @dkingman).
- Fix missing imports on sentinel client (by @opapy).
- Connection closing improvements on sentinel client (by @opapy).


django-redis 3.7.0
==================

- Add support for django's ``KEY_FUNCTION`` and ``REVERSE_KEY_FUNCTION`` (by @teferi)
- Accept float value for socket timeout.
- Fix wrong behavior of ``DJANGO_REDIS_IGNORE_EXCEPTIONS`` with socket timeouts.
- Backward incompatible change: now raises original exceptions instead of self defined.


django-redis 3.6.2
==================

- Add ttl method purposed to be included in django core.
- Add iter_keys method that uses redis scan methods for memory efficient keys retrieval.
- Add version keyword parameter to keys.
- Deprecate django 1.3.x support.


django-redis 3.6.1
==================

- Fix wrong import on sentinel client.


django-redis 3.6.0
==================

- Add pluggable connection factory.
- Negative timeouts now works as expected.
- Delete operation now returns a number of deleted items instead of None.


django-redis 3.5.1
==================

- Fixed redis-py < 2.9.0 incompatibilities
- Fixed runtests error with django 1.7


django-redis 3.5.0
==================

- Removed: stats module (should be replaced with an other in future)
- New: experimental client for add support to redis-sentinel.
- Now uses a django ``DEFAULT_TIMEOUT`` constant instead of ``True``.
  Deprecation warning added for code that now uses ``True`` (unlikely).
- Fix wrong forward of timeout on shard client.
- Fix incr_version wrong behavior when using shard client (wrong client used for set new key).


django-redis 3.4.0
==================

- Fix exception name from ConnectionInterrumped to
  ConnectionInterrupted maintaining an old exception class
  for backward compatibility (thanks Łukasz Langa (@ambv))

- Fix wrong behavior for "default" parameter on get method
  when DJANGO_REDIS_IGNORE_EXCEPTIONS is True
  (also thanks to Łukasz Langa (@ambv)).

- Now added support for replication setups to default client (it still
  experimental because is not tested in production environments).

- Merged SimpleFailoverClient experimental client (only for
  experiment with it, not ready for use in production)

- Django 1.6 cache changes compatibility. Explicitly passing in
  timeout=None no longer results in using the default timeout.

- Major code cleaning. (Thanks to Bertrand Bordage @BertrandBordage)

- Bugfixes related to some index error on hashring module.


django-redis 3.3.0
==================

- Add SOCKET_TIMEOUT attribute to OPTIONS (thanks to @eclipticplane)


django-redis 3.2.0
==================

- Changed default behavior of connection error exceptions: now by default
    raises exception on connection error is occurred.

Thanks to Mümin Öztürk:

- cache.add now uses setnx redis command (atomic operation)
- cache.incr and cache.decr now uses redis incrby command (atomic operation)


django-redis 3.1.7
==================

- Fix python3 compatibility on utils module.

django-redis 3.1.6
==================

- Add nx argument on set method for both clients (thanks to Kirill Zaitsev)


django-redis 3.1.5
==================

- Bug fixes on sharded client.


django-redis 3.1.4
==================

- Now reuse connection pool on massive use of ``get_cache`` method.


django-redis 3.1.3
==================

- Fixed python 2.6 compatibility.


django-redis 3.1.2
==================

- Now on call close() not disconnect all connection pool.


django-redis 3.1.1
==================

- Fixed incorrect exception message on LOCATION has wrong format.
    (Thanks to Yoav Weiss)


django-redis 3.1
================

- Helpers for access to raw redis connection.


django-redis 3.0
================

- Python 3.2+ support.
- Code cleaning and refactor.
- Ignore exceptions (same behavior as memcached backend)
- Pluggable clients.
- Unified connection string.


django-redis 2.2.2
==================

- Bug fixes on ``keys`` and ``delete_pattern`` methods.


django-redis 2.2.1
==================

- Remove duplicate check if key exists on ``incr`` method.
- Fix incorrect behavior of ``delete_pattern`` with sharded client.


django-redis 2.2
================

- New ``delete_pattern`` method. Useful for delete keys using wildcard syntax.


django-redis 2.1
================

- Many bug fixes.
- Client side sharding.
