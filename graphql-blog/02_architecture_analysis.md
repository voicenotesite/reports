# GraphQL Blog — Architecture Analysis

**Project:** GraphQL Blog  
**Technology:** Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL  
**Location:** `/home/dominic/Documents/graphql-blog`  
**Report #:** 2/20  


## Architecture Type
GraphQL API with PostgreSQL, Docker Compose orchestration

## Layers
GraphQL Schema (Strawberry) → Resolvers → SQLAlchemy ORM → PostgreSQL

## Design Patterns
Resolver pattern via Strawberry GraphQL

## Scalability
PostgreSQL-backed, horizontally scalable via replicas
