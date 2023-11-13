Documentation generation
========================

```
sphinx-apidoc -o source/apidoc ../PROJECT_NAME_LOWER
```

For HTML documentation generation:
```
make html
```

Once HTML documentation is generated, you can open `build/html/index.html` in your web browser to see it.

To clean generated documentation :
```
make clean
```