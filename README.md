# LabsByHoodie-Website-Project
A practical website project for learning .NET backend development, Azure infrastructure, PowerShell automation, GitHub Actions, monitoring, security, and search engine optimization.

Repository status: Private during development. Secrets, passwords, API keys, connection strings, and employer information must never be committed—even to a private repository.

Project Goal

Build and operate a professional technical portfolio and learning website without becoming a frontend developer. The site will publish hands-on Windows, Azure, PowerShell, cybersecurity, and infrastructure notes while providing experience with real backend and cloud operations.

The goal is not only to create a résumé website. The project should demonstrate that I can:

Build and maintain a backend application

Deploy an application to Azure

Configure DNS and HTTPS

Store and retrieve data

Protect application secrets

Automate deployments with PowerShell and GitHub Actions

Monitor availability, performance, and errors

Apply practical SEO techniques

Document problems, fixes, and lessons learned

Repository Information

Suggested repository name:

labsbyhoodie-dotnet-website

Suggested repository description:

A hands-on ASP.NET Core website project for learning Azure infrastructure, PowerShell automation, CI/CD, monitoring, security, and technical SEO.

Technology Stack

Component

Technology

Purpose

Application

ASP.NET Core Razor Pages

Backend and server-rendered pages

Language

C# and .NET

Application logic

Design

Bootstrap theme

Responsive layout without advanced CSS

Development database

SQLite

Simple local data storage

Production database

Azure Database for PostgreSQL

Managed production database experience

Hosting

Azure App Service

Application hosting

Secrets

Azure Key Vault

Secure storage for connection strings and secrets

Identity

Microsoft Entra ID

Authentication for the administration area

Automation

PowerShell

Deployment, validation, maintenance, and reporting

CI/CD

GitHub Actions

Automated build, test, and deployment

Monitoring

Application Insights and Azure Monitor

Logs, errors, availability, and performance

DNS and security

Cloudflare

DNS, HTTPS, caching, and security controls

SEO

Google Search Console

Indexing and search-performance analysis

Analytics

Privacy-conscious web analytics

Visitor and content-performance measurements

Important Learning Decision

I do not need to become a frontend developer. However, I should understand enough HTML and CSS to work with:

Page titles

Headings such as H1 and H2

Paragraphs and lists

Links and images

Forms

Metadata

Responsive layouts

Accessibility labels

Semantic page structure

Advanced JavaScript and custom CSS are not initial project requirements.

Planned Website Pages

Home

About Me

Skills and Certifications

Technical Projects

GitHub Repositories

Windows and PowerShell Guides

Azure and Sentinel Notes

Blog or Knowledge Base

Downloadable Résumé

Contact Page

Private Administration Area

Proposed Architecture

Visitor
  |
Cloudflare DNS and HTTPS
  |
Azure App Service
  |
ASP.NET Core Razor Pages
  |
PostgreSQL Database

Supporting services:
- Azure Key Vault for secrets
- Entra ID for administrator authentication
- Application Insights for telemetry
- GitHub Actions for deployment
- PowerShell for validation and maintenance

Project Phases

Phase 1: Create the Local Application

Objectives

Install the current supported .NET SDK

Install Git and Visual Studio Code or Visual Studio

Create the ASP.NET Core Razor Pages application

Run the application locally

Understand the project folders

Create the initial Git commit

Initial commands

dotnet --version
dotnet new webapp -n LabsByHoodie.Web
Set-Location LabsByHoodie.Web
dotnet restore
dotnet run

Topics to understand

Program.cs

appsettings.json

Pages folder

wwwroot folder

Razor .cshtml files

Page model .cshtml.cs files

Development versus production configuration

Completion checklist

The application runs locally

I can explain the main project folders

I can modify page text

I created the first Git commit

No secrets are stored in the repository

Phase 2: Build the Public Website

Objectives

Select and customize a Bootstrap theme

Create the main navigation

Build the public pages

Add projects and certifications

Add a résumé download

Test mobile responsiveness

Completion checklist

Home page completed

About page completed

Skills and certifications page completed

Projects page completed

Blog landing page completed

Contact page completed

Navigation works on desktop and mobile

Images include useful alternative text

Phase 3: Add Backend Functionality

Objectives

Create models for projects and articles

Configure Entity Framework Core

Use SQLite during development

Add database migrations

Display database content on the website

Create an administration area

Possible data models

Project

ID

Title

Summary

Technology list

GitHub URL

Article URL

Image path

Published status

Created date

Article

ID

Title

URL slug

Summary

Content

Category

Meta description

Published status

Published date

Updated date

Completion checklist

SQLite database created

First migration completed

Projects load from the database

Articles load from the database

Unpublished content is hidden from visitors

Administration pages require authentication

Phase 4: Deploy to Azure

Objectives

Create an Azure resource group

Create an Azure App Service plan

Create an Azure Web App

Deploy the application

Configure environment-specific settings

Connect the custom domain

Enforce HTTPS

Suggested resource naming

Resource group: rg-labsbyhoodie-prod
App Service plan: asp-labsbyhoodie-prod
Web App: app-labsbyhoodie-prod
Key Vault: kv-labsbyhoodie-prod
Application Insights: appi-labsbyhoodie-prod

Actual Azure resource names must be globally unique where required.

Completion checklist

Application deployed successfully

Production settings are separate from development settings

Custom domain configured

HTTPS enforced

HTTP redirects to HTTPS

Application restarts successfully

Rollback procedure documented

Phase 5: Secure the Application

Objectives

Store secrets outside the repository

Configure Azure Key Vault

Use managed identity where supported

Protect the administration area with Entra ID

Apply least-privilege access

Enable secure headers and production error handling

Never commit

Passwords

API keys

Access tokens

Database connection strings containing credentials

Private certificates or private keys

.env files containing secrets

Production configuration values

Employer or customer information

Completion checklist

Secrets stored in Key Vault or protected environment settings

Managed identity enabled where practical

Administration area protected

Authorization tested with allowed and unauthorized accounts

Detailed errors disabled in production

Access permissions documented

Phase 6: Automate with GitHub Actions

Objectives

Build the application automatically

Run automated tests

Deploy only after successful validation

Keep production secrets out of workflow files

Document rollback procedures

Proposed workflow

Push or approved merge to main
  -> Restore dependencies
  -> Build application
  -> Run tests
  -> Publish application
  -> Deploy to Azure App Service
  -> Run health check

Completion checklist

Workflow file created

Build runs automatically

Tests run automatically

Failed builds prevent deployment

Successful builds deploy to Azure

Deployment result is visible in GitHub

Post-deployment health check added

Phase 7: Automate Operations with PowerShell

Proposed scripts

scripts/
├── Test-Prerequisites.ps1
├── Deploy-Infrastructure.ps1
├── Test-WebsiteHealth.ps1
├── Test-BrokenLinks.ps1
├── Export-AppServiceConfiguration.ps1
├── Backup-WebsiteData.ps1
└── Get-WebsiteStatusReport.ps1

PowerShell learning goals

Parameters

Variables

Conditional logic

Loops

Functions

Error handling

Logging

REST API requests

JSON processing

Azure PowerShell commands

Secure credential handling

Completion checklist

Prerequisite-checking script completed

Website health-check script completed

Broken-link checker completed

Scripts use parameters instead of hard-coded values

Scripts include error handling

Scripts produce useful logs or reports

Phase 8: Add Monitoring

Objectives

Configure Application Insights

Review application requests and failures

Track response time

Configure availability tests

Create alerts for failures and degraded performance

Document common troubleshooting queries

Conditions to monitor

Website availability

HTTP 5xx errors

Slow response times

Failed dependencies

Application exceptions

Deployment failures

Database connectivity

Expiring certificates or domain problems

Completion checklist

Application Insights connected

Logs visible

Availability test configured

Failure alert configured

Performance alert configured

Test incident generated and investigated

Monitoring screenshots sanitized and documented

Phase 9: Implement Technical SEO

On-page SEO

Unique page title for every page

Useful meta description for every important page

One clear H1 heading per page

Logical H2 and H3 structure

Descriptive internal links

Descriptive image alternative text

Clean and readable URLs

Original, useful content

Technical SEO

XML sitemap

robots.txt

Canonical URLs

HTTPS

Mobile-friendly design

Fast page loading

Compressed images

Structured data where appropriate

Useful 404 page

Correct redirects

No broken internal links

Search measurement

Connect Google Search Console

Submit the XML sitemap

Monitor indexed pages

Review search queries and impressions

Track click-through rate

Identify pages with indexing problems

Improve articles based on actual search data

Completion checklist

Titles and meta descriptions completed

Heading structure reviewed

Sitemap available

robots.txt available

Canonical URLs configured

Search Console connected

Sitemap submitted

Mobile performance tested

Broken-link report completed

Phase 10: Add Python Automation Later

Python is not required for the initial website. It can be added when the site is operating and there is a real automation need.

Possible Python projects

Crawl the website for broken links

Audit missing titles and meta descriptions

Analyze exported Search Console data

Generate SEO reports

Check sitemap contents

Process analytics data

Identify duplicate page titles

Create content-performance reports

Suggested Repository Structure

labsbyhoodie-dotnet-website/
├── README.md
├── src/
│   └── LabsByHoodie.Web/
├── tests/
│   └── LabsByHoodie.Web.Tests/
├── scripts/
│   ├── Test-Prerequisites.ps1
│   ├── Test-WebsiteHealth.ps1
│   └── Test-BrokenLinks.ps1
├── docs/
│   ├── architecture.md
│   ├── deployment.md
│   ├── monitoring.md
│   ├── security.md
│   ├── seo-checklist.md
│   └── troubleshooting-journal.md
├── .github/
│   └── workflows/
│       └── deploy.yml
├── .gitignore
└── LICENSE

Documentation Requirements

For each major change, document:

What I wanted to accomplish

Why I selected the approach

Commands or configuration used

What failed

How I investigated the failure

How I fixed it

How I validated the result

What I would improve next time

Troubleshooting Journal Template

## Problem

Describe the symptom and expected behavior.

## Environment

List the relevant application, operating-system, Azure, and network details without exposing sensitive information.

## Investigation

List the logs, commands, tests, and evidence reviewed.

## Root Cause

Explain the actual cause of the problem.

## Resolution

Document the change that corrected the problem.

## Validation

Explain how the fix was tested.

## Lesson Learned

Record what should be remembered or improved.

Git Workflow

git pull origin main
git switch -c feature/descriptive-name
git status
git add <specific-files>
git diff --staged
git commit -m "Describe the completed change"
git push -u origin feature/descriptive-name

Initial Milestone

The first milestone is complete when:

The ASP.NET Core application runs locally

The website has a Home, About, Projects, and Blog page

The project is tracked in Git

The private GitHub repository is organized

No secrets are committed

The application is deployed to Azure App Service

The custom domain uses HTTPS

Application Insights collects telemetry

A PowerShell script verifies website availability

GitHub Actions builds and deploys the application

The sitemap and robots.txt file are working

Final Success Criteria

This project is successful when I can explain and demonstrate:

How the application handles a web request

How the application retrieves data

How the production environment is configured

How secrets are protected

How code moves from GitHub to Azure

How deployment failures are detected

How application errors are investigated

How DNS and HTTPS are configured

How search engines discover and index the website

How PowerShell reduces repetitive operational work

Current Status

Current phase: Planning

Next action: Create the private GitHub repository and initialize the ASP.NET Core Razor Pages application

Frontend priority: Basic HTML and Bootstrap only

Primary learning focus: .NET, Azure, PowerShell, backend infrastructure, automation, monitoring, and SEO

License

Keep this repository private during early development. Select a license only when the project is ready to be shared publicly.
