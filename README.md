# 관성 도르래 애트우드 가속도 계산기

두 개의 매달린 추와 회전 관성이 있는 도르래로 이루어진 애트우드 장치의 가속도를 계산합니다.

- ID: E126
- App: https://nanalab.kr/eng-inertial-atwood/
- Repository: https://github.com/NaNaCompany/eng-inertial-atwood
- Formula: a = (m₂ − m₁)g / (m₁ + m₂ + I/r²)

## Model and data

로프는 질량이 없고 늘어나지 않으며 도르래에서 미끄러지지 않습니다. 축 마찰·공기저항을 무시하고 두 추는 자유롭게 움직입니다. 출력의 양수는 둘째 추의 하강, 음수는 첫 추의 하강입니다. I=0은 이상적인 무관성 도르래의 극한입니다.

Inputs normalize to SI. Repeated-input models support adding/removing actual input rows. Calculations, finite-number checks and physical-domain checks run locally; no external property database or solver API is used.

## Validation

Run node --test tests/*.test.mjs and python scripts/build-locales.py --check. tests/reference.json contains independently computed high-precision default and boundary references. The source notices distinguish original MIT work from citation-only external references.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
