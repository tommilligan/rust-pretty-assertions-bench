# Benchmarks for `pretty_assertions`

To avoid pulling in many, many additional development dependencies, the benchmarks for `pretty_assertions` are in a separate repo.

## Usage

To run the benchmarks, clone this repo as a sister of [rust-pretty-assertions](https://github.com/colin-kiegel/rust-pretty-assertions), then run `cargo bench`. A HTML report will be generated.

```bash
# Clone both repos
git clone https://github.com/colin-kiegel/rust-pretty-assertions
git clone https://github.com/tommilligan/rust-pretty-assertions-bench

# Run benchmarks
cd rust-pretty-assertions-bench
cargo bench

# View report
xdg-open target/criterion/report/index.html
```

### Comparing two builds

Running the benchmarks again with update the report, showing the difference between the most recent two sets of results.

```bash
# To compare to a different build, checkout an rerun the benchmarks
cd ../rust-pretty-assertions
git checkout "$MY_BRANCH_NAME"
cd ../rust-pretty-assertions-bench
cargo bench
xdg-open target/criterion/report/index.html
```