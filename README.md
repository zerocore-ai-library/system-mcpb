# System MCP Server

An MCP server providing system utilities for AI agents including sleep, datetime, and random number generation.

## Setup

### Using tool CLI

Install the CLI from https://github.com/zerocore-ai/tool-cli

```bash
# Install from tool.store
tool install library/system
```

```bash
# View available tools
tool info library/system
```

```bash
# Get current time
tool call library/system -m get_datetime
```

```bash
# Generate a random number
tool call library/system -m get_random_integer -p min=1 -p max=100
```

```bash
# Sleep for 1 second
tool call library/system -m sleep -p duration_ms=1000
```

## Tools

### `sleep`

Pause execution for a specified duration.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `duration_ms` | integer | Yes | Duration to sleep in milliseconds (0 to 300000) |

**Output:**
| Field | Type | Description |
|-------|------|-------------|
| `slept_ms` | integer | Actual duration slept in milliseconds |

### `get_datetime`

Get the current UTC date and time.

**Input:** None

**Output:**
| Field | Type | Description |
|-------|------|-------------|
| `iso8601` | string | UTC timestamp in ISO 8601 format |
| `unix_ms` | integer | Unix timestamp in milliseconds |

### `get_random_integer`

Generate a random integer within an inclusive range.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `min` | integer | Yes | Minimum value (inclusive) |
| `max` | integer | Yes | Maximum value (inclusive) |

**Output:**
| Field | Type | Description |
|-------|------|-------------|
| `value` | integer | Random integer in range [min, max] |

## License

MIT
