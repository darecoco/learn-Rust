## Rust Grammer #1 - Comments

```
// 한 줄 주석

/*
여러줄 주석
*/
```

Rust는 C/C++과 같은 주석입니다.  

***

## [문서화 주석 docs (한국어 번역)](https://doc.rust-kr.org/ch14-02-publishing-to-crates-io.html#%EC%9C%A0%EC%9A%A9%ED%95%9C-%EB%AC%B8%EC%84%9C%ED%99%94-%EC%A3%BC%EC%84%9D-%EB%A7%8C%EB%93%A4%EA%B8%B0)

```
/// 문서화 주석 : 마크다운을 지원합니다. 주석 뒤에 오는 아이템을 문서화 합니다.

//! 문서화 주석 : 위 문서화 주석과는 다르게 주석을 담고 있는 아이템을 문서화 합니다.
```
 
 또한 Rust는 **문서화 주석(documentation comment)**이 있습니다.

```
// docs의 문서화 주석(///) 예제

/// Adds one to the number given. 
/// 
/// # Examples 
/// 
/// ``` 
/// let arg = 5; 
/// let answer = my_crate::add_one(arg); 
/// 
/// assert_eq!(6, answer); 
/// ``` pub fn add_one(x: i32) -> i32 { x + 1 }
```

```
// docs의 문서화 주석(//!) 예제

//! # My Crate <- add_one()을 담고있음
//!
//! `my_crate` is a collection of utilities to make performing certain
//! calculations more convenient.

/// Adds one to the number given. <- add_one() 설명
// --생략--
```
**주석을 포함하고 있는 아이템에 대한 문서화**는 도저히 무슨 설명인지 몰라서 원문도 찾아보고 구글링도 한 결과 다음과 같은 결론을 냈다.

| 설명    | `///`                   | `//!`                  |
| ----- | ----------------------- | ---------------------- |
| 용도    | 아이템(함수, 구조체, 모듈 등)을 문서화 | 모듈 전체를 문서화 or 크레이트 문서화 |
| 작성 위치 | 아이템 바로 위에 작성            | 파일 맨 위 or 모듈 바로 위에 작성  |
| 사용 예  | 함수, 구조체, 열거형 등의 설명 작성   | 모듈이나 크레이트 전체에 대한 설명 작성 |
***
### 공부한 강의
- ##### [Easy Rust Korean #2](https://youtu.be/x7GlQjh2aSw?si=hp53uxyg-Zn1NwJ6)