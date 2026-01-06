import streamlit as st
import os
from PIL import Image

# 제목
st.title("2025년 추억 모음집")
st.write("이곳은 2025년의 추억을 모으는 공간입니다. 사진과 텍스트를 업로드하고, 소중한 추억을 기록하세요!")

# 이미지 업로드 기능
st.subheader("추억의 사진 업로드")
uploaded_image = st.file_uploader("이미지를 업로드하세요", type=["png", "jpg", "jpeg"])

if uploaded_image is not None:
    # 이미지 표시
    image = Image.open(uploaded_image)
    st.image(image, caption="업로드된 이미지", use_column_width=True)
    st.write("이 사진에 대한 설명을 작성해주세요:")
    description = st.text_area("추억의 설명")
    if st.button("추억 추가하기"):
        st.write(f"추억이 추가되었습니다! 설명: {description}")
        # 여기에 데이터베이스나 파일 저장 기능 추가 가능
else:
    st.write("사진을 업로드하여 추억을 추가하세요!")

# 텍스트 기록 기능 (추억의 글쓰기)
st.subheader("2025년의 추억을 글로 남기기")
text = st.text_area("이곳에 2025년의 추억을 남겨주세요!")
if st.button("추억 저장"):
    if text:
        st.write(f"추억이 저장되었습니다: {text}")
    else:
        st.write("내용을 입력해주세요.")

# 데이터베이스 기능 (기본적으로 파일로 저장할 수 있음)
# 추억을 로컬 파일에 저장하거나 더 나아가 클라우드 저장소를 활용할 수도 있습니다.
