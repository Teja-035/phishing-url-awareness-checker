# Phishing URL Awareness Checker – Test Results

## 1. Introduction

This document records the testing performed on the Phishing URL Awareness Checker Python application.

The application analyses URL text and identifies common warning indicators without visiting websites or making network requests.

## 2. Test Cases

| Test No. | Sample URL                              | Expected Result                   | Actual Result                 | Status |
| -------- | --------------------------------------- | --------------------------------- | ----------------------------- | ------ |
| 1        | https://www.example.com/login           | No listed warning signs           | No listed warning signs found | PASS   |
| 2        | http://192.0.2.10/account               | Detect IP address and HTTP        | Both warnings detected        | PASS   |
| 3        | http://example.com@sample.invalid/login | Detect @ symbol and HTTP          | Both warnings detected        | PASS   |
| 4        | https://a.b.c.d.e.example.invalid/path  | Detect multiple hostname segments | Warning detected              | PASS   |
| 5        | https://xn--example.invalid/            | Detect Punycode-style hostname    | Warning detected              | PASS   |

## 3. Testing Summary

* Total test cases: 5
* Passed test cases: 5
* Failed test cases: 0
* Overall result: All five sample tests produced the expected results.

## 4. Conclusion

The Phishing URL Awareness Checker successfully completed all five sample tests. The application identified the specified URL warning indicators.

The application performs text-based checks only. It does not visit URLs and cannot guarantee that a URL is safe.
