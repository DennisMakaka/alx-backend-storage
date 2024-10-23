# 0x02. Redis Basic

## Project Overview

This project introduces basic usage of Redis with Python, focusing on using Redis for caching, storing data, and creating a simple tracking system for web pages. The project explores key concepts such as working with Redis data types, caching with decorators, and managing cache expiration.

## Learning Objectives

- Use Redis as a basic data store.
- Implement Redis as a simple cache.
- Apply Python decorators to track function calls and store history.
- Cache web pages and manage cache expiration times.

## Requirements

- All files should be interpreted/compiled on Ubuntu 18.04 LTS using Python 3 (version 3.7).
- Code must follow `pycodestyle` standards (version 2.5).
- Functions must have type annotations.
- Each module, class, and method must contain docstrings.
- Redis should be installed and running locally or in a container for testing.

### Redis Installation

To install Redis on Ubuntu 18.04:

1. Install Redis server and Redis Python package.
2. Update Redis configuration to bind it to `127.0.0.1`.
3. Start the Redis server.


## Tasks

### 0. Writing Strings to Redis

Create a `Cache` class that stores data in Redis with randomly generated keys. The `store` method should accept data in various types (string, bytes, integer, or float) and store them in Redis.

### 1. Reading From Redis and Recovering Original Type

Implement a `get` method to retrieve data from Redis and return it in its original format. The method should accept an optional parameter to convert the data back to its original form. Additional methods (`get_str` and `get_int`) are used for automatic type conversion.

### 2. Incrementing Values

Create a `count_calls` decorator to track the number of times the `store` method is called. This decorator uses Redis' `INCR` command to increment the count each time the method is invoked.

### 3. Storing Lists

Define a `call_history` decorator to store the input and output history of a function in Redis lists. For each call, the decorator appends the input to one list and the output to another.

### 4. Retrieving Lists

Implement a `replay` function that retrieves and displays the history of calls made to a function. The function should use Redis to fetch the stored inputs and outputs for a decorated method.

### 5. Expiring Web Cache and Tracker

Implement a `get_page` function that fetches the HTML content of a URL and caches the response for 10 seconds. Additionally, the function should track the number of times a URL was accessed using Redis.

## Usage

You can test the functionality by creating a `main.py` script and running examples as provided in the task descriptions.

```bash
$ python3 main.py
```
