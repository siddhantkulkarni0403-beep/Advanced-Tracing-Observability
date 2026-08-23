Project name = Advanced-Tracing-Observability
Team Member name= Leader Saish Bhadange
                  Member2= Siddhant Kulkarni
                  Member3= Siddhi Jagtap
                  Member4 Samiksha Kadam
                  Member5= Aditi Narode





Task 7 — Advanced Tracing & Observability
Overview

This project implements Advanced Tracing & Observability for an autonomous Research & Competitor Tracking AI Agent.

The system tracks:

Agent execution
Planning decisions
Tool calls
Latency
Token usage
Errors
Failure recovery
Fallback tools
Final results
Before/after performance

The implementation uses OpenTelemetry for tracing and metrics.

Architecture
User Query
    ↓
Agent Planner
    ↓
Research Tool ───────┐
                     ├──→ Synthesis Agent
News Tool ───────────┘
    ↓
Controlled Failure
    ↓
Failure Diagnosis
    ↓
Fallback Tool
    ↓
Recovery
    ↓
Final Result
    ↓
Trace + Metrics
Task 7 Requirements Covered
1. End-to-End Tracing

The system creates traces for:

Agent execution
Planning
Research tool
News tool
Failure diagnosis
Recovery
Fallback tool
Synthesis
2. Tool Observability

Every tool call records:

Tool name
Query
Result count
Execution time
Errors
Recovery status
3. Failure Detection

A controlled tool failure can be triggered during the live demo.

Example:

{
  "query": "AI semiconductor competitor trends",
  "fail_tool": true
}
4. Automatic Diagnosis

When a tool fails, the agent records:

Failure detected
      ↓
Root cause identified
      ↓
Primary tool unavailable
      ↓
Fallback activated
