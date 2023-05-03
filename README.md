# Demo to reproduce 'pnpm` bug [#6497](https://github.com/pnpm/pnpm/issues/6497)

See https://github.com/pnpm/pnpm/issues/6497

# Reproduction steps

With the prepared code:

```
git clone https://github.com/e1himself/pnpm-hoisted-installation-peer-deps-bug-demo
cd pnpm-hoisted-installation-peer-deps-bug-demo
pnpm install
find node_modules -name react
```

Manually:

```
pnpm init
echo 'auto-install-peers=true' > .npmrc
echo 'node-linker-hoisted' > .npmrc
pnpm add react-dates
find node_modules -name react
```


# Expected result

- `react`, `react-dom`, and `react-with-direction` packages are installed

# Actual result

- `react`, `react-dom`, and `react-with-direction` packages are NOT installed
