# 競技プロ典型90問

- [競プロ 典型90問](https://github.com/E869120/kyopro_educational_90)

- [競プロ典型90問をRustで解く](https://dev.thanaism.com/tags/rust/)

---

- 入出力ライブラリ
  - Cargo.toml
    ```
    [dependencies]
    proconio = "0.4.1"
    ```
  
  - main.rs
  
    ```rust
    use proconio::input;
    ```
  
  - 入出力用マクロ
  
    ```rust
    use std::io::*;
    use std::str::FromStr;
    
    fn read<T: FromStr>() -> T {
      let stdin = stdin();
      let stdin = stdin.lock();
      let token: String = stdin
          .bytes()
          .map(|c| c.expect("failed to read char") as char) 
          .skip_while(|c| c.is_whitespace())
          .take_while(|c| !c.is_whitespace())
          .collect();
      token.parse().ok().expect("failed to parse token")
    }
    ```
  
    