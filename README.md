import streamlit as st
import pandas as pd
from datetime import datetime

st.set_page_config(page_title="Kirstie Cornett - AI Learning", layout="wide")

st.title("🚀 Kirstie Cornett's AI Learning Journey")
st.subheader("Phase 0 Foundations - Completed ✅")

st.sidebar.metric("Total Hours", "13.25+")
st.sidebar.metric("Projects Done", "6/6")
st.sidebar.metric("Phase", "0 / Complete")

col1, col2 = st.columns(2)

with col1:
    st.subheader("My Progress")
    data = {
        "Project": ["Project 1", "Project 2", "Project 3", "Project 4", "Project 5", "Project 6"],
        "Hours": [0.5, 0.75, 1.0, 1.0, 1.25, 0.5],
        "Status": ["✅ Completed"] * 6
    }
    df = pd.DataFrame(data)
    st.dataframe(df, use_container_width=True)

    total_hours = df["Hours"].sum()
    st.metric("Total Hours Invested", f"{total_hours:.2f} hours")

with col2:
    st.subheader("Next Steps")
    st.success("✅ Phase 0 Complete!\nNow entering Prompt Engineering + Machine Learning")
    st.info("Current Focus: Clean Code & Prompt Writing Practice")

st.balloons()
