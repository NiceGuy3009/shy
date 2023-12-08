import requests 
import streamlit as st
from streamlit_lottie import st_lottie

# Find more imojis here: https://www.webfx.com/tools/emoji-cheat-sheet/ 
st.set_page_config(page_title="Mine Only", page_icon=":tada:", layout="wide")

def load_lottieurl(url):
   r = requests.get(url)
   if r.status_code != 200:\
        return None
   return r.json()
# ---- LOAD ASSETS ----
lottie_coding =  load_lottieurl("https://lottie.host/b3c4efbf-3c67-42b2-ba03-e6e5da2afac5/jXNg2IN9E7.json")
lottie_coding2 = load_lottieurl("https://lottie.host/bc0f39f3-1b10-4569-994f-f867a93306b6/CtcvNKuyXj.json")

# ----HEADER SECTION----
with st.container():  
    st.subheader("Hi, I am Algen Marc a BSCPE student :wave:")
    st.title("SIARGAO")
    st.write("I am here to show you the beauty of SIARGAO.")

# ---- WHAT TO KNOW ----
with st.container():
   st.write("---")
   left_column, right_column = st.columns(2)
   with left_column:
      st.header("What To Know")
      st.write("##")
      st.write(
         """ 
         ABOUT;\n
         -CULTURE & FOOD\n
         -TOP EVENTS & FESTIVALS\n
        THINGS YOU CAN DO IN SIARGAO;\n
         -SURFING\n
         -SUNRISE AND SUNSETS\n
         -ISLAND HOPPING\n
         -SUGBA LAGOON\n
         -CLIFF JUMPING
         -TAYANGBAN CAVE POOLS\n
         -TAKTAK WATERFALL\n
         -BUCAS GRANDE’S LAGOON\n
         -PACIFICO BEACH\n
         -LOCAL COMMUNITY MARKET 
         """
      )
   with right_column:
      st_lottie(lottie_coding, height=300, key="coding")
      st_lottie(lottie_coding2, height=500, key="coding2")




# ---- ABOUT ----
with st.container():
   st.write("---")
   st.header("ABOUT")
   st.write("Culture & Food")
   st.write("Attracting adventurous travellers from around the world – many on a tight budget – Siargao has an eclectic dining scene embracing international cooking, vegan and other healthy cuisine, and local recipes with or without a modern twist. Filipino favourites not to miss include the seafood boodle fight at Daku Island and the unique surfboard-shaped bread, Pan de Surf.  Siargao has a lively nightlife scene focused on different bars on different nights of the week, so chatting to locals is the best way to find out where to head. Regular venues include Bravo, RumBar, Viento and the Jungle Shack.Another way to get to know locals is through their love of karaoke, both in their own homes and in dedicated bars.")
   st.write("Top Events & Festivals")
   st.write("Siargao International Game Fishing Tournament – April\n" 
            "Siargao International Marathon – July\n"
            "Siargao International Surfing Cup – September\n"
            "Part of General Luna’s yearly fiesta – the island’s biggest, with two weeks of parades, parties, live bands and discos.\n" 
            "Other fiestas include Dapa in January, San Benito in March, San Isidro in May, Socorro in June, Del Carmen and Burgus in July, Santa Monica in August, Pilar in October")

      
