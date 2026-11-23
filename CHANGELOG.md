# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-config`, published as `gizmocraft/zendframework1-config`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-config` to `gizmocraft/zendframework1-config`. It now requires `gizmocraft/zendframework1-exception` and `gizmocraft/zendframework1-json`, each `^2.0.0`. The optional XML dependency is now `gizmocraft/zendframework1-xml`.

### Other changes

- `Zend_Config_Xml::__construct()` now always restores the previous error handler, also when loading the file throws. Before, a failed load left the handler installed.
- `Zend_Config_Writer_Ini` uses `is_int()` instead of `is_integer()`, which is deprecated in PHP 8.6.
- Removed an always-true `false` check after `DOMDocument::createTextNode()` in `Zend_Config_Xml`.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes and declared properties. CI runs PHP 8.5 and 8.6.
- No public signature changes.
