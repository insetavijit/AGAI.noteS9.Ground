> [!quote] Yajur Veda 19.30 **"विद्याम् चाविद्याम् च यस्तद्वेदोभयं सह।"** _"True wisdom is gained by uniting knowledge with action."_ Learning Loop: **Explore → Learn → Do → Comprehend → Improve → Repeat**

# 1. FOUNDATIONS (ALL – PYTHON CONTEXT)

## 1.1 Definitions – core Python terms

- Script, interpreter, bytecode
- Statements, expressions, variables
- Data types (int, float, str, bool, None)
- Collections (list, tuple, dict, set)
- Functions, methods, classes, modules, packages
- Decorators, generators, context managers
- Virtual environments, pip, package management

## 1.2 Core Principles – how Python "thinks"

- "Everything is an object" philosophy
- Duck typing & dynamic typing
- Indentation-based syntax (whitespace matters)
- LEGB scope rule (Local, Enclosing, Global, Built-in)
- GIL (Global Interpreter Lock) implications
- Pythonic code: "There should be one obvious way to do it"
- PEP 8 style guide & PEP standards
- Explicit is better than implicit (Zen of Python)

## 1.3 Mental Models – intuition builders

- "Python as glue language" → connecting different systems
- "Batteries included" → rich standard library
- "Readable code over clever code" → maintainability focus
- "List comprehensions as functional loops" → concise iteration
- "Everything returns something" → functions always have return values (None if not specified)
- "Mutable vs immutable" → understanding reference behavior
- "Iterator protocol" → lazy evaluation pattern

## 1.4 Architecture Overview – typical Python application stack

### 1.4.1 High-Level Diagram

- User/Client → Web Server (Gunicorn/uWSGI) → WSGI/ASGI App (Flask/Django/FastAPI) → Business Logic → DB/Cache/Services

### 1.4.2 Components & Responsibilities

- Entry point (`main.py`, `__main__.py`, `app.py`)
- Router/URL patterns → view/endpoint functions
- Views/Controllers → request handling
- Models → data structures & ORM entities
- Templates → HTML rendering (Jinja2, Django templates)
- Services/Managers → business logic layer
- Settings/Config → `settings.py`, `.env`, config files
- Middleware → request/response processing pipeline

### 1.4.3 Data Flow

- Input: Query params, JSON, form data, files
- Processing: Validation (Pydantic, marshmallow), sanitization
- Persistence: PostgreSQL/MySQL via SQLAlchemy/Django ORM, Redis, MongoDB
- Output: HTML, JSON APIs, CSV/Excel, binary files

## 1.5 Internals & Mechanics

- CPython interpreter: compilation to bytecode (.pyc files)
- Memory management: reference counting + garbage collection
- GIL and its impact on multi-threading
- `__dict__` and attribute storage
- Method Resolution Order (MRO) for inheritance
- Import system: modules, packages, `__init__.py`
- Context managers & the `with` statement protocol
- Descriptor protocol (`__get__`, `__set__`, `__delete__`)

## 1.6 Limitations & Trade-offs

- Performance vs C/Rust/Go for CPU-intensive tasks
- GIL limiting true parallel threading (use multiprocessing/async)
- Memory consumption (higher than compiled languages)
- Packaging and dependency management complexity
- Python 2 vs 3 legacy issues (mostly resolved)
- Dynamic typing can hide bugs (mitigated by type hints + mypy)

---

# 2. APPLIED PRACTICE (4 Sheets – PYTHON FOCUSED)

## 2.1 Code Examples – growing difficulty

### 2.1.1 Basic Examples

- Variables, types, operators
- Control flow (`if`, `elif`, `else`, `for`, `while`)
- Lists, tuples, dictionaries, sets
- Functions, default arguments, `*args`, `**kwargs`
- String formatting (f-strings, `.format()`)
- File I/O (reading/writing text and binary files)
- List comprehensions, dict comprehensions

### 2.1.2 Intermediate Examples

- Classes and OOP (inheritance, composition, properties)
- Exception handling (`try`/`except`/`finally`)
- Decorators (function and class decorators)
- Generators and `yield`
- Context managers (`with` statement)
- Working with JSON, CSV, XML
- Regular expressions (`re` module)
- Virtual environments and pip
- Unit testing with `unittest` or `pytest`

### 2.1.3 Advanced Examples

- Metaclasses and class customization
- Async/await and asyncio
- Descriptors and properties
- Type hints and using mypy for static checking
- Custom iterators and itertools
- Multiprocessing and threading patterns
- Building CLI tools with `argparse` or `click`
- Creating and publishing packages to PyPI
- C extensions and using `ctypes`/`cffi`
- Performance profiling (cProfile, line_profiler)

## 2.2 Hands-on Mini Projects

### 2.2.1 Beginner Project – "Python Basics Lab"

- CLI calculator with operator functions
- Todo list with file persistence (JSON/CSV)
- Simple web scraper with `requests` + `BeautifulSoup`
- Contact book with CRUD operations

### 2.2.2 Intermediate Project – "Data Dashboard"

- Web app with Flask/FastAPI
- Data visualization with matplotlib/plotly
- RESTful API with CRUD endpoints
- SQLite/PostgreSQL integration
- JWT authentication
- Unit and integration tests

### 2.2.3 Production Project – "Full-Stack Application"

- Django/FastAPI backend with ORM
- User authentication & authorization
- Background tasks with Celery
- Frontend integration (REST API or templates)
- Docker containerization
- CI/CD pipeline
- Logging, monitoring, error tracking
- Environment-based configuration

## 2.3 Patterns & Workflows

### 2.3.1 Design Patterns (Python examples)

- Singleton (module-level pattern)
- Factory, Abstract Factory
- Strategy, Observer, Command
- Dependency Injection
- Repository pattern
- Service layer architecture
- MVC/MVT patterns

### 2.3.2 Common Workflows

- Creating a new Django/Flask/FastAPI project
- Adding a new endpoint (route → view → service → model)
- Database migrations (Alembic, Django migrations)
- Writing and running tests (pytest fixtures, mocking)
- Environment management (venv, poetry, conda)
- Deploying to production (WSGI servers, Docker)

### 2.3.3 Anti-patterns (Python flavored)

- Using mutable default arguments
- Bare `except` clauses (catching all exceptions)
- Not using context managers for resources
- Global state and shared mutable data
- Import *
- Premature optimization
- Not following PEP 8
- Mixing tabs and spaces

## 2.4 Tools, Tips & Debugging Notes

- Python REPL and IPython for interactive exploration
- Virtual environments: `venv`, `virtualenv`, `poetry`, `conda`
- Package management: `pip`, `pip-tools`, `poetry`
- Debugging: `pdb`, `ipdb`, IDE debuggers
- Linting: `pylint`, `flake8`, `ruff`
- Formatting: `black`, `autopep8`
- Type checking: `mypy`, `pyright`
- Testing: `pytest`, `unittest`, `doctest`
- Profiling: `cProfile`, `memory_profiler`, `py-spy`
- Documentation: Sphinx, MkDocs, docstrings

## 2.5 Real-World Use Cases

### 2.5.1 Industry Applications

- Web development (Django, Flask, FastAPI)
- Data science & ML (NumPy, pandas, scikit-learn, TensorFlow, PyTorch)
- DevOps & automation (Ansible, Fabric)
- Scientific computing (SciPy, SymPy)
- Game development (Pygame)

### 2.5.2 Business Applications

- Data analysis and reporting
- ETL pipelines
- Business intelligence dashboards
- API integrations and microservices
- Automation scripts

### 2.5.3 System Integrations

- REST/GraphQL APIs
- Database operations (SQL, NoSQL)
- Message queues (RabbitMQ, Redis, Kafka)
- Cloud services (AWS, GCP, Azure SDKs)
- File processing and batch jobs

---

# 3. QUICK REFERENCE (PYTHON)

## 3.1 Cheatsheets

- Syntax & operators
- Built-in functions (sorted, map, filter, zip, enumerate)
- String methods
- List/Dict/Set methods
- Common standard library modules
- OOP keywords (`class`, `@property`, `@staticmethod`, `@classmethod`)
- Virtual environment commands

## 3.2 Snippets

- Database connection with SQLAlchemy
- Basic Flask/FastAPI route
- File upload handler
- JSON API response helper
- Context manager template
- Decorator template
- Async function example

## 3.3 Templates

### 3.3.1 "Prompt" Templates (for you + AI)

- "Refactor this Python function to use type hints and be more testable…"
- "Convert this procedural Python into OOP with proper separation of concerns…"
- "Add async/await to this synchronous code…"

### 3.3.2 Code Templates

- Class skeleton with `__init__`, `__str__`, `__repr__`
- FastAPI/Flask route handler
- pytest test case template
- CLI tool with argparse
- Data class with `dataclasses` or Pydantic

### 3.3.3 Boilerplates

- Minimal Flask REST API structure
- FastAPI project with dependency injection
- Django project structure
- Python package with setup.py/pyproject.toml

## 3.4 Condensed Architecture Diagrams

- One-page app structure for:
    - Flask microservice
    - Django monolith
    - FastAPI + async workers
    - CLI tool architecture

## 3.5 Error & Issue Playbook

### 3.5.1 Common Errors

- `NameError: name 'x' is not defined`
- `IndentationError`
- `KeyError` / `IndexError`
- `AttributeError: 'NoneType' object has no attribute...`
- `ImportError` / `ModuleNotFoundError`
- `TypeError: unsupported operand type(s)`

### 3.5.2 Causes

- Variable not defined or typo
- Inconsistent indentation (tabs vs spaces)
- Key doesn't exist in dict, index out of range
- Operating on None without checking
- Module not installed or wrong import path
- Type mismatch in operations

### 3.5.3 Fixes

- Check variable names and scope
- Use consistent indentation (4 spaces, PEP 8)
- Use `.get()` for dicts, check list length
- Add None checks or use Optional types
- `pip install` package, check PYTHONPATH
- Add type hints and use mypy for early detection

## 3.6 Best Practices

### 3.6.1 Do's & Don'ts

- DO use virtual environments for every project
- DO follow PEP 8 style guide
- DO use type hints in new code
- DO write docstrings for functions/classes
- DON'T use mutable default arguments
- DON'T use bare except clauses
- DON'T modify lists while iterating over them
- DON'T use global variables excessively

### 3.6.2 Performance Guidelines

- Use built-in functions (they're C-optimized)
- Use list comprehensions over loops when appropriate
- Avoid string concatenation in loops (use join)
- Use generators for large datasets
- Profile before optimizing
- Consider numpy for numerical operations
- Use `__slots__` for memory optimization with many instances

### 3.6.3 Security Considerations

- Input validation and sanitization
- SQL injection prevention (use parameterized queries)
- XSS prevention (escape output)
- Secure password hashing (bcrypt, argon2)
- CSRF protection in web apps
- Environment variables for secrets (never hardcode)
- Dependency vulnerability scanning

---

# 4. ACTIVE RECALL (3 Sheets – PYTHON CONTENT)

## 4.1 Flashcards (Q/A) – Python-focused **[🗸]**

- Built-in types and their methods
- Common standard library modules
- OOP concepts (inheritance, polymorphism, encapsulation)
- When to use list vs tuple vs set vs dict
- Mutable vs immutable types
- `*args` vs `**kwargs`
- Decorators, generators, context managers

## 4.2 Quizzes – progressively harder **[🗸]**

### 4.2.1 Beginner Quiz

- Syntax, data types, control flow
- Lists, dicts, functions
- File I/O, string manipulation

### 4.2.2 Intermediate Quiz

- OOP, decorators, generators
- Exception handling patterns
- Virtual environments and packages
- Testing basics

### 4.2.3 Expert Quiz

- Metaclasses, descriptors
- Async programming
- Performance optimization
- GIL implications
- Type system advanced usage

## 4.3 Challenges & Exercises

- "Make this code thread-safe"
- "Convert this synchronous code to async"
- "Refactor this procedural script into OOP with tests"
- "Optimize this slow function" (profiling exercise)
- "Add type hints and pass mypy strict mode"

## 4.4 Memory Anchors – Python-specific **[🗸]**

### 4.4.1 Analogies

- pip = npm/composer
- Virtual environment = isolated workspace
- List comprehension = for loop compressed
- Generator = lazy loaded sequence
- Decorator = function wrapper/modifier

### 4.4.2 Visual Mnemonics

- Request flow diagram with middleware layers
- Scope resolution (LEGB) as nested boxes
- MRO as inheritance tree traversal
- GIL as single-lane bridge

### 4.4.3 Comparison Tables

- List vs Tuple vs Set vs Dict
- `is` vs `==`
- `@staticmethod` vs `@classmethod` vs instance method
- Threading vs Multiprocessing vs Async
- Flask vs Django vs FastAPI

## 4.5 Spaced Repetition Plan

### 4.5.1 Daily Quick Review

- 5-10 flashcards + read one PEP or article
- Write one small function with type hints

### 4.5.2 Weekly Review

- Solve one coding challenge (LeetCode, HackerRank)
- Refactor or extend a previous mini-project
- Read one chapter of Python documentation

### 4.5.3 30-Day Refresh

- Build a small project using a new library/framework
- Contribute to an open-source Python project

### 4.5.4 90-Day Mastery Cycle

- Build a production-ready application
- Write a blog post or tutorial on a Python concept
- Mentor someone or answer questions on Stack Overflow

---

# 5. STAYING CURRENT (PYTHON ECOSYSTEM)

## 5.1 New Features & Updates

- Track Python releases (3.x versions)
- PEP proposals and acceptances
- New standard library modules
- Performance improvements
- Typing system enhancements

## 5.2 Breaking Changes & Deprecations

- Deprecated modules and functions
- Python 2 → 3 migration (historical context)
- Syntax changes and removals
- Standard library reorganizations

## 5.3 Migration Guides

- Python version upgrades (3.x → 3.x+1)
- Framework upgrades (Django, Flask, FastAPI)
- Package management tool transitions (pip → poetry)
- Type hints adoption strategy

## 5.4 Ecosystem Shifts

- Growth of type hints and static typing
- Async/await becoming standard
- New frameworks (FastAPI growth)
- Packaging improvements (pyproject.toml)
- Python in machine learning dominance
- Performance improvements (Python 3.11+)

## 5.5 Market & Industry Trends

- Python in data science and AI/ML
- Python for backend APIs
- DevOps and infrastructure as code
- Python in cloud computing (serverless, containers)
- Scientific computing and research

## 5.6 Monthly Upgrade Ritual

### 5.6.1 Update This Document

- Add new patterns or libraries used
- Document new language features
- Update best practices

### 5.6.2 Refresh Templates

- Update boilerplates with latest syntax
- Add type hints to older examples
- Incorporate new standard library features

### 5.6.3 Evaluate New Tools

- IDE plugins and extensions
- New testing tools
- Static analyzers updates
- New frameworks or libraries

### 5.6.4 Archive Outdated Notes

- Mark Python 2 patterns as historic
- Update deprecated library references
- Remove obsolete workarounds

---

<p align="center">--- [ 🐍 Python Mastery Garden 🐍 ] ---</p>