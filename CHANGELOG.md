# Changelog
All notable changes to this project will be documented in this file.

## [2.0.1] - 2021-08-04
### Added

### Changed
* #63 Removing redundant code and excluding code fragments from SONAR warnings about commented out code
* #64 Adding support for dealing with static imports of methods named solely $, as with JUnit's JunitParamsRunner.$
* #66 Getting simple names for types now aligned with the JLS spec
* #67 When finding method invocations, method candidates that are not found are now also included in the list of results

### Fixed
* #57 Added compatibility for fully qualified names in Javadoc in TypeReferenceRefactor (fixes #3)
* #65 Incrementing version of javadoc plugin with fix affecting later versions (9+) of java


## [2.0.0] - 2021-07-12
### Added
* #55 Added unit test for matching methods by return type with MethodMatcher
* #58 Added function to get name for anonymous class declaration

### Changed
* #58 Compile with Java 11 
* #56 Don't remove import when changing a static method by name only, as we may not be changing all invocations of this method. Instead, leave the import and let the UnusedImportRefactor clean it up if necessary.

### Fixed


## [1.4.0] - 2021-06-30
### Added

### Changed
* #54 Cached sources and classpath so that they are only retrieved once, and shared between validation and use

### Fixed
* #54 Method parameter type name standardisation


## [1.3.9] - 2021-06-30
### Added

### Changed
* #53 Standardising name of parameter types for methods, between when a MethodMatcher is constructed and evaluated

### Fixed


## [1.3.8] - 2021-06-29
### Added

### Changed
* #51 Extra null safety when checking method names, and static on-demand imports are checked when finding declaring methods

### Fixed
* #49 Allow multiple files in --cp


## [1.3.7] - 2021-06-23
### Added

### Changed
* Tweak to static method type resolution attempting to find single applicable type name from imports, if possible, before falling back to resolving

### Fixed


## [1.3.6] - 2021-06-16
### Added

### Changed

### Fixed
* Fixes for static imports, particularly better detection of when imports are really unused.
* MethodMatcher now works better when matching parameters that are arrays and type variables.


## [1.3.3] - 2021-06-09
### Added

### Changed

### Fixed
* Fixed case where adding a static import would remove an existing static import of the same name, even if this was valid.


## [1.3.1] - 2021-06-04
### Added
* Added a new ASTOperation the JavaPatternASTOperation, [read more in the wiki](https://github.com/alfasoftware/astra/wiki/Java-Pattern-Refactor).

### Changed
* ClassVisitor visits additional ASTNodes

### Fixed


## [1.2.1] - 2021-05-19
### Added

### Changed
* Type matcher now matches on parameterized supertypes
* Method matcher now allows custom predicates to be used for matching any AST node types handled by MethodMatcher

### Fixed
* Fix unused imports refactor so it doesn't lose inner types.
* Log the total number of files after filtering with the predicate


## [1.0.0] - 2021-03-06
### Added
* Initial commit! Please see our [README](https://github.com/alfasoftware/astra/blob/main/README.md) and [Wiki](https://github.com/alfasoftware/astra/wiki) for details on how to get started.

### Changed

### Fixed
