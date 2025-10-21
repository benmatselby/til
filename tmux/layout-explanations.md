# Layout explanations

When defining layouts for tmux/tmuxinator there are a few named layouts you can use. Here are explanations of what each layout does:

- main-vertical
- main-horizontal
- even-vertical
- even-horizontal

## main-vertical

It will look like this:

```text
|------------------------------|
|              |               |
|              |               |
|              |---------------|
|              |               |
|              |               |
|------------------------------|
```

## main-horizontal

It will look like this:

```text
|------------------------------|
|                              |
|                              |
|--------------|---------------|
|              |               |
|              |               |
|------------------------------|
```

## even-vertical

It will look like this:

```text
|------------------------------|
|                              |
|------------------------------|
|                              |
|------------------------------|
|                              |
|------------------------------|
```

## even-horizontal

It will look like this

```text
|------------------------------|
|        |           |         |
|        |           |         |
|        |           |         |
|        |           |         |
|        |           |         |
|------------------------------|
```

## Example tmuxinator configuration

```yml
name: project
root: ~/git/

windows:
  - coding:
      layout: main-vertical
      panes:
        -
        -
        -
```
