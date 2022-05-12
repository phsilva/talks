---
marp: true
paginate: true
theme: uncover
author: Paulo Henrique Silva
math: katex
size: 16:9
---

# Rust :crab:

maio de 2022

@phsilva

---

# Rust

![Rust](https://www.rust-lang.org/static/images/rust-logo-blk.svg)
> A language empowering everyone
to build reliable and efficient software.

https://www.rust-lang.org/

---

# Olá!

```rust

fn main() {
    let pessoa = "Cássio";
    println!("Olá {pessoa}!");
}

```

---

# Prós

- expressividade
- controle sobre recursos
- ferramentas modernas
- tipagem

---

# Contras

- curva de aprendizado
- tipagem

---

# Tools

![bg left](./tools.jpg)

* `cargo` build
* `cargo` test
* `cargo` fmt
* `cargo` clippy
* crates.io

---

# crates.io

![w:850px](./modules.png)

---

# Embarcados

![bg left](./embedded.jpg)

- Arduino
- Raspberry Pi
- Relógios
- Foguetes
- ...


---

# Embarcados

> Qualquer sistema onde haja restrições de recursos computacionais, de memória ou ambos.

---

# Rust Embedded WG

- SVD
- PAC
- HAL
- embedded-hal
- knurling
    - defmt
- probe-rs

---

# Ecossistema

![h:350px](https://cdn.hashnode.com/res/hashnode/image/upload/v1650963194624/LJHBDqlVQ.png?auto=compress,format&format=webp)

https://craigjb.com/2019/12/31/stm32l0-rust/

---

# Ecossistema

![](https://craigjb.com/public/images/rust/embedded_rust_eco.png)

https://craigjb.com/2019/12/31/stm32l0-rust/

---

# blink

https://github.com/rp-rs/rp2040-project-template

```md
## cargo-generate

cargo generate --git https://github.com/rp-rs/rp2040-project-template \
   --branch main --name blink

## toolchain

rustup target install thumbv6m-none-eabi
cargo install flip-link
cargo install elf2uf2-rs --locked

cd blink && cargo run
```

---

# FIM
<!-- _color: white -->

![bg](./fim.jpg)

---

# Links

```md
- https://doc.rust-lang.org/book/
- https://github.com/rust-embedded/wg
- https://github.com/rust-embedded/awesome-embedded-rust
- https://rtic.rs
- https://embassy.dev/
```

---

# Arduino

```cpp
void setup() {
    pinMode(LED_BUILTIN, OUTPUT);
}

void loop() {
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000);
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000);
}
```

