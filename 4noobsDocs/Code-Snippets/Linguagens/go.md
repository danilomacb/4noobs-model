[Roadmap](../../../README.md)

```go
package funding

import "testing"

func BenchmarkFund(b *testing.B) {
    // Add as many dollars as we have iterations this run
    fund := NewFund(b.N)

    // Burn through them one at a time until they are all gone
    for i := 0; i < b.N; i++ {
        fund.Withdraw(1)
    }

    if fund.Balance() != 0 {
        b.Error("Balance wasn't zero:", fund.Balance())
    }
}
```
