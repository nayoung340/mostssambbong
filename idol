import streamlit as st
import pandas as pd

# 샘플 데이터프레임 생성
data = {
    '아이돌': ['BTS', 'BLACKPINK', 'SEVENTEEN', 'TWICE', 'IVE'],
    '앨범': ['Map of the Soul: 7', 'THE ALBUM', 'Face the Sun', 'Eyes Wide Open', 'ELEVEN'],
    '판매량': [5000000, 1200000, 1300000, 800000, 500000]
}
df = pd.DataFrame(data)

# Streamlit 애플리케이션 제목
st.title("아이돌 앨범 판매량 조회")

# 사용자 입력 받기
idol_name = st.text_input("아이돌 이름을 입력하세요:")

# 입력된 아이돌 이름에 해당하는 데이터 필터링
if idol_name:
    result = df[df['아이돌'].str.contains(idol_name, case=False)]
    if not result.empty:
        st.write(f"**{idol_name}**의 앨범 판매량:")
        st.table(result)
    else:
        st.write(f"아이돌 이름 '{idol_name}'에 해당하는 데이터를 찾을 수 없습니다.")
