# Python Portfolio — Project Overview

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 1/20  


## Overview
Unified FastAPI API combining URL shortener, blog, chat, queue, and RAG modules.

## Purpose
Unifies 5 portfolio project APIs (shortener, blog, chat, queue, RAG) under one FastAPI app.

## Status
Active development. See report 16 (Known Issues) and report 19 (Improvements).

## Key Features
• 5 integrated modules: shortener, blog, chat, queue, RAG
• Unified auth (JWT)
• Shared database schema
• CORS enabled
• Optional frontend serving

## Entry Points
`uvicorn app.main:app`
