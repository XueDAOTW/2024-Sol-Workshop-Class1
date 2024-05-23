# 2024 XueDAO Solidity Bootcamp #1

## Installation

1. Clone this project to your local environment: `git clone git@github.com:XueDAOTW/2024-Sol-Workshop-Class1.git`
2. Enter the `class1` project: `cd class1`
3. Build the project: `forge build`
4. Test the project: `forge test -vvv`, there are 10 tests in total and all of them should pass.

## Tooling

**anvil**

Run the local Ethereum node: `make anvil`

**cast**

1. Check the total supply of DAI token:

```bash
cast call 0x6b175474e89094c44da98b954eedeac495271d0f "totalSupply()(uint256)" --rpc-url https://eth-mainnet.alchemyapi.io/v2/Lc7oIGYeL_QvInzI0Wiu_pOZZDEKBrdf
```


```bash
cast 4byte-decode 0x1F1F897F676d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003e7
```

**forge**

1. testing framework: `forge test`

```bash
No files changed, compilation skipped

Ran 10 tests for test/bank.t.sol:BankTest
[PASS] test_balances() (gas: 9926)
[PASS] test_deposit() (gas: 44678)
[PASS] test_fallback() (gas: 44469)
[PASS] test_owner() (gas: 7637)
[PASS] test_receive() (gas: 44480)
[PASS] test_reentrancy() (gas: 393543)
[PASS] test_rugpull() (gas: 54355)
[PASS] test_version() (gas: 6932)
[PASS] test_withdraw() (gas: 82027)
[PASS] test_withdrawAll() (gas: 61819)
Suite result: ok. 10 passed; 0 failed; 0 skipped; finished in 8.11ms (2.84ms CPU time)

Ran 1 test suite in 468.32ms (8.11ms CPU time): 10 tests passed, 0 failed, 0 skipped (10 total tests)
```

2. test coverage: `forge coverage`
```bash
Ran 1 test suite in 472.14ms (9.66ms CPU time): 10 tests passed, 0 failed, 0 skipped (10 total tests)
| File                 | % Lines        | % Statements   | % Branches    | % Funcs        |
|----------------------|----------------|----------------|---------------|----------------|
| script/Counter.s.sol | 0.00% (0/1)    | 0.00% (0/1)    | 100.00% (0/0) | 0.00% (0/2)    |
| src/bank.sol         | 90.48% (19/21) | 91.67% (22/24) | 50.00% (5/10) | 100.00% (9/9)  |
| test/bank.t.sol      | 100.00% (7/7)  | 88.89% (8/9)   | 50.00% (2/4)  | 100.00% (4/4)  |
| Total                | 89.66% (26/29) | 88.24% (30/34) | 50.00% (7/14) | 86.67% (13/15) |
```