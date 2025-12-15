# n8n Code Examples Specification

## ADDED Requirements

### Requirement: Data Manipulation Code Examples
The system SHALL provide simple, reusable code examples for transforming and processing data within n8n workflows.

#### Scenario: Transform item data with new fields
**Given** a workflow receives items with `firstName` and `lastName` fields  
**When** the Code Node processes the items  
**Then** each item should have a new `fullName` field combining first and last names  
**And** the original fields should be preserved

#### Scenario: Filter and map array data
**Given** a workflow receives an array of items  
**When** the Code Node filters items based on a condition  
**Then** only matching items should be returned  
**And** each item should be transformed to the desired format

### Requirement: API Integration Code Examples
The system SHALL provide examples for making HTTP requests and handling API responses in n8n workflows.

#### Scenario: Make GET request to external API
**Given** a workflow needs data from an external API  
**When** the Code Node makes an HTTP GET request  
**Then** the response data should be parsed and returned  
**And** errors should be handled gracefully

#### Scenario: POST data to webhook
**Given** a workflow needs to send data to an external service  
**When** the Code Node makes an HTTP POST request with JSON payload  
**Then** the request should include proper headers  
**And** the response should be captured and returned

### Requirement: Conditional Logic Code Examples
The system SHALL provide examples for implementing decision-making logic in workflows.

#### Scenario: Route items based on conditions
**Given** a workflow receives items with different properties  
**When** the Code Node evaluates conditions  
**Then** items should be categorized or filtered accordingly  
**And** the logic should be clearly documented

### Requirement: Data Formatting Code Examples
The system SHALL provide examples for converting between different data formats.

#### Scenario: Convert JSON to CSV format
**Given** a workflow has JSON data  
**When** the Code Node converts to CSV  
**Then** the output should be properly formatted CSV string  
**And** headers should be included

#### Scenario: Format dates and timestamps
**Given** a workflow has date/time data  
**When** the Code Node formats the dates  
**Then** dates should be in the specified format  
**And** timezone handling should be correct

### Requirement: Error Handling Code Examples
The system SHALL provide examples for handling errors gracefully in workflows.

#### Scenario: Catch and log errors
**Given** a Code Node operation might fail  
**When** an error occurs  
**Then** the error should be caught with try/catch  
**And** error details should be logged  
**And** the workflow should continue or fail gracefully
