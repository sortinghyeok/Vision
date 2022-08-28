# 픽셀 직접 접근 비전 알고리즘 적용 프로그램 개발

## 대용량 bmp 파일에 대한 로딩 로직 구현, 전체 이미지 세이브 로직 구현 완료 / 2022.08.23
파일을 바이트 Stream으로 변경하고, 해당 Stream을 메모리 직접 접근을 통한 로우 레벨 수준의 분할 Reading하여 메모리가 처리 가능한 수준으로 바꾸어 로딩 성공

## Morphology Dilation 연산 적용 완료, 확대, 축소 기능 적용 개발 완료 / 2022.08.24

완료
- 픽셀 패딩 밀리는 현상 수정 완료,
- 모폴로지 연산 중 팽창 구현 완료

이슈
- 확대, 축소 시 저장 기능에 문제 있음
- 모폴로지 침식 연산 구현 요망

## Morphology Erosion 연산 적용 완료 / 2022.08.25

완료
- 모폴로지 연산 중 침식(축소) 구현 완료

이슈
- 오리지널 비트맵의 저장시 저장 안되는 이슈 발견

## Histogram Equalization, Otsu Binarization 연산 적용 완료 / 2022.08.26

완료
- 히스토그램 평활화와 오츠 이진화 기능 구현 완료

이슈
- Gaussian Filter 기능 로직 완료했으나 Blur의 느낌이 아님. 색이 단순히 어두워지는 느낌. 추후 로직을 살펴봐야할 필요 있음
- 연산 미처리한 원데이터 저장 불가 이슈 잔존, 연산 추가 개발 후 추후 수정하도록 함

## Morphology Erosion 이슈 발견 / 2022.08.29

이슈
- 모폴로지 침식 중 픽셀의 우측만이 수그러드는 현상 발견, 코드 구현 중 커널의 중심이 정가운데가 아닌 좌측에 있는 것을 확인하고 이에 대한 수정 요망
