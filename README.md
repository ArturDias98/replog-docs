# RepLog Documentation Repository

This repository contains technical documentation for the **RepLog** project — an offline-first workout tracking application. The documentation is structured to facilitate AI agent comprehension and provide comprehensive context for development assistance.

## Purpose

This repository serves as a centralized knowledge base for AI agents working on the RepLog project. By maintaining separate, focused documentation files, AI agents can quickly access relevant technical specifications without parsing the main codebase.

## Documentation Structure

### [backend-api.md](backend-api.md)

Complete backend API specification for the RepLog sync system, including:

- Data model (DynamoDB schema)
- API endpoints and request/response formats
- Entity processing logic
- Conflict resolution strategies
- Authentication and security considerations

### [sync-strategy.md](sync-strategy.md)

Comprehensive offline-first synchronization strategy, covering:

- System architecture and data flow
- Change log (sync queue) implementation
- Frontend sync service design
- Backend API contract
- Conflict resolution mechanisms
- Edge case handling
- Migration planning

## About RepLog

RepLog is an offline-first workout tracking application that allows users to:

- Create, edit, and delete workouts entirely offline
- Sync data across multiple devices when online
- Track exercises, muscle groups, and workout logs

The app uses a **change log with last-write-wins** strategy, where every mutation is recorded as a change event in a local queue and synced with the backend when connectivity is available.

### Tech Stack

- **Frontend**: Angular with IndexedDB for local storage
- **Backend**: DynamoDB for document storage
- **Sync**: Event-based change log with idempotent operations

### Related Repositories

- **Frontend**: [https://github.com/ArturDias98/replog](https://github.com/ArturDias98/replog)
- **Backend**: [https://github.com/ArturDias98/replog-api](https://github.com/ArturDias98/replog-api)

## Usage for AI Agents

When working on the RepLog project:

1. Reference these documents to understand system architecture and design decisions
2. Use the specifications to maintain consistency across implementations
3. Refer to conflict resolution and edge case documentation when handling sync logic
4. Follow the established patterns for API endpoints and data models

## Updates

This documentation should be updated whenever significant architectural changes or new features are implemented in the RepLog project.

---

**Repository Type**: Technical Documentation  
**Target Audience**: AI Development Agents  
**Last Updated**: March 2026
