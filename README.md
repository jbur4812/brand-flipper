# 🚀 Brandable Domain Name Generator & Checker - Streamlit App Version


OPENAI_API_KEY = 'your-openai-api-key-here'
NAMECHEAP_API_USER = 'your-namecheap-api-username'
NAMECHEAP_API_KEY = 'your-namecheap-api-key'
NAMECHEAP_API_IP = 'your-whitelisted-ip-address'

# --- LIBRARIES ---
import openai
import requests
import streamlit as st

openai.api_key = OPENAI_API_KEY

# --- PROMPT LIBRARY ---
PROMPT_LIBRARY = {
    'tech': "Generate 10 brandable, short domain names (3-5 letters), pronounceable, for the tech startup industry. Separate each name by a new line.",
    'finance': "Generate 10 unique, catchy, short domain names (3-5 letters), for fintech companies. Must be easy to pronounce.",
    'health': "List 10 short, brandable domain names (3-5 letters), ideal for a health and wellness brand. Each on a new line.",
    'luxury': "Create 10 luxurious-sounding, short domain names (3-5 letters) that would appeal to high-end fashion or jewelry brands.",
    'crypto': "Generate 10 futuristic, edgy, brandable domain names (3-5 letters), perfect for a cryptocurrency startup.",
    'AI': "Generate 10 sleek, AI-inspired domain names, each 3-5 letters, for artificial intelligence products.",
    'gaming': "List 10 punchy, playful domain names (3-5 letters), for gaming or esports brands.",
    'eco': "Suggest 10 eco-friendly sounding, short domain names (3-5 letters), suitable for sustainability-focused companies.",
    'fashion': "Provide 10 chic, fashion-forward domain names (3-5 letters), suitable for an online clothing boutique or fashion app.",
    'education': "Generate 10 engaging, short domain names (3-5 letters), perfect for edtech startups or online learning platforms.",
    'travel': "Give me 10 catchy, wanderlust-inducing domain names (3-5 letters), ideal for a travel brand or booking platform.",
    'music': "Generate 10 rhythmic, cool, and brandable domain names (3-5 letters) perfect for music platforms or record labels.",
    'sports': "List 10 energetic, competitive-sounding domain names (3-5 letters), great for sports teams, gear, or streaming apps.",
    'food': "Create 10 appetizing, fun, and brandable domain names (3-5 letters) for a food delivery service or gourmet brand."
}

# --- FUNCTIONS ---
#

