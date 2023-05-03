# Demo to reproduce 'pnpm` bug [#6497](https://github.com/pnpm/pnpm/issues/6497)

See https://github.com/pnpm/pnpm/issues/6497

# Reproduction steps

```
git clone https://github.com/e1himself/pnpm-hoisted-installation-peer-deps-bug-demo
cd pnpm-hoisted-installation-peer-deps-bug-demo
pnpm install
find node_modules -name react
```

# Expected result

- `react`, `react-dom`, and `react-with-direction` packages are installed

# Actual result

- `react`, `react-dom`, and `react-with-direction` packages are NOT installed
