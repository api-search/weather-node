---
name: Broadcast
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/broadcast.png
url: https://example.com/apis/broadcast.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Broadcast
apis:
  - name: GitLab REST API
    description: >+
      The REST APIs have been around for a longer time compared to GraphQL APIs,
      which may make them more familiar to some developers. It is often a good
      choice for developers who are more comfortable with traditional API
      architecture.

    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.gitlab.com/ee/api/rest/index.html
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.gitlab.com/ee/api/rest/index.html
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: GitLab API
            license:
              name: CC BY-SA 4.0
              url: https://gitlab.com/gitlab-org/gitlab/-/blob/master/LICENSE
          tags:
            - name: badges
              description: Operations about badges
            - name: branches
              description: Operations about branches
            - name: alert_management
              description: Operations about alert_managements
            - name: batched_background_migrations
              description: Operations about batched_background_migrations
            - name: admin
              description: Operations about admins
            - name: migrations
              description: Operations about migrations
            - name: applications
              description: Operations about applications
            - name: avatar
              description: Operations about avatars
            - name: broadcast_messages
              description: Operations about broadcast_messages
            - name: bulk_imports
              description: Operations about bulk_imports
            - name: application
              description: Operations about applications
            - name: access_requests
              description: Operations related to access requests
            - name: ci_lint
              description: Operations related to linting a CI config file
            - name: ci_resource_groups
              description: Operations to manage job concurrency with resource groups
            - name: ci_variables
              description: Operations related to CI/CD variables
            - name: cluster_agents
              description: Operations related to the GitLab agent for Kubernetes
            - name: clusters
              description: Operations related to clusters
            - name: composer_packages
              description: Operations related to Composer packages
            - name: conan_packages
              description: Operations related to Conan packages
            - name: container_registry
              description: Operations related to container registry
            - name: container_registry_event
              description: Operations related to container registry events
            - name: dashboard_annotations
              description: Operations related to dashboard annotations
            - name: debian_distribution
              description: Operations related to Debian Linux distributions
            - name: debian_packages
              description: Operations related to Debian Linux packages
            - name: dependency_proxy
              description: Operations to manage dependency proxy for a groups
            - name: deploy_keys
              description: Operations related to deploy keys
            - name: deploy_tokens
              description: Operations related to deploy tokens
            - name: deployments
              description: Operations related to deployments
            - name: dora_metrics
              description: >-
                Operations related to DevOps Research and Assessment (DORA) key
                metrics
            - name: environments
              description: Operations related to environments
            - name: error_tracking_client_keys
              description: Operations related to error tracking client keys
            - name: error_tracking_project_settings
              description: Operations related to error tracking project settings
            - name: feature_flags_user_lists
              description: Operations related to accessing GitLab feature flag user lists
            - name: feature_flags
              description: Operations related to feature flags
            - name: features
              description: Operations related to managing Flipper-based feature flags
            - name: freeze_periods
              description: Operations related to deploy freeze periods
            - name: generic_packages
              description: Operations related to Generic packages
            - name: geo
              description: Operations related to Geo
            - name: geo_nodes
              description: Operations related Geo Nodes
            - name: go_proxy
              description: Operations related to Go Proxy
            - name: group_export
              description: Operations related to exporting groups
            - name: group_import
              description: Operations related to importing groups
            - name: group_packages
              description: Operations related to group packages
            - name: helm_packages
              description: Operations related to Helm packages
            - name: integrations
              description: Operations related to integrations
            - name: issue_links
              description: Operations related to issue links
            - name: jira_connect_subscriptions
              description: Operations related to JiraConnect subscriptions
            - name: jobs
              description: Operations related to CI Jobs
            - name: maven_packages
              description: Operations related to Maven packages
            - name: merge_requests
              description: Operations related to merge requests
            - name: metadata
              description: Operations related to metadata of the GitLab instance
            - name: metrics_user_starred_dashboards
              description: Operations related to User-starred metrics dashboards
            - name: ml_model_registry
              description: Operations related to Model registry
            - name: npm_packages
              description: Operations related to NPM packages
            - name: nuget_packages
              description: Operations related to Nuget packages
            - name: package_files
              description: Operations about package files
            - name: plan_limits
              description: Operations related to plan limits
            - name: project_export
              description: Operations related to exporting projects
            - name: project_hooks
              description: Operations related to project hooks
            - name: project_import
              description: Operations related to importing projects
            - name: project_import_bitbucket
              description: Operations related to importing BitBucket projects
            - name: project_import_github
              description: Operations related to importing GitHub projects
            - name: project_packages
              description: Operations related to project packages
            - name: projects
              description: Operations related to projects
            - name: protected environments
              description: Operations related to protected environments
            - name: pypi_packages
              description: Operations related to PyPI packages
            - name: release_links
              description: Operations related to release assets (links)
            - name: releases
              description: Operations related to releases
            - name: resource_milestone_events
              description: Operations about resource milestone events
            - name: rpm_packages
              description: Operations related to RPM packages
            - name: rubygem_packages
              description: Operations related to RubyGems
            - name: suggestions
              description: Operations related to suggestions
            - name: system_hooks
              description: Operations related to system hooks
            - name: terraform_state
              description: Operations related to Terraform state files
            - name: terraform_registry
              description: Operations related to the Terraform module registry
            - name: unleash_api
              description: Operations related to Unleash API
          paths:
            /api/v4/groups/{id}/badges/{badge_id}:
              get:
                tags:
                  - Gets
                  - Badge
                  - Of
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: Gets a badge of a group.
                description: This feature was introduced in GitLab 10.6.
              put:
                tags:
                  - Updates
                  - Badge
                  - Of
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: Updates a badge of a group.
                description: This feature was introduced in GitLab 10.6.
              delete:
                tags:
                  - Removes
                  - Badge
                  - From
                  - The
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: Removes a badge from the group.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/groups/{id}/badges:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Group
                  - Badges
                  - Viewable
                  - By
                  - The
                  - Authenticated
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: >-
                  Gets a list of group badges viewable by the authenticated
                  user.
                description: This feature was introduced in GitLab 10.6.
              post:
                tags:
                  - Adds
                  - Badge
                  - To
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                summary: Adds a badge to a group.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/groups/{id}/badges/render:
              get:
                tags:
                  - Preview
                  - Badge
                  - From
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                summary: Preview a badge from a group.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/groups/{id}/access_requests/{user_id}:
              delete:
                tags:
                  - Denies
                  - An
                  - Access
                  - Request
                  - For
                  - The
                  - Given
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                summary: Denies an access request for the given user.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/groups/{id}/access_requests/{user_id}/approve:
              put:
                tags:
                  - Approves
                  - An
                  - Access
                  - Request
                  - For
                  - The
                  - Given
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                summary: Approves an access request for the given user.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/groups/{id}/access_requests:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Access
                  - Requests
                  - For
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                summary: Gets a list of access requests for a group.
                description: This feature was introduced in GitLab 8.11.
              post:
                tags:
                  - Requests
                  - Access
                  - For
                  - The
                  - Authenticated
                  - User
                  - To
                  - Group.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                summary: Requests access for the authenticated user to a group.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/projects/{id}/repository/merged_branches:
              delete:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                description: Delete all merged branches
            /api/v4/projects/{id}/repository/branches/{branch}:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Get a single repository branch
              delete:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Delete a branch
              head:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Check if a branch exists
            /api/v4/projects/{id}/repository/branches:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Get a project repository branches
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                description: Create branch
            /api/v4/projects/{id}/repository/branches/{branch}/unprotect:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                description: Unprotect a single branch
            /api/v4/projects/{id}/repository/branches/{branch}/protect:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                description: Protect a single branch
            /api/v4/projects/{id}/badges/{badge_id}:
              get:
                tags:
                  - Gets
                  - Badge
                  - Of
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Gets a badge of a project.
                description: This feature was introduced in GitLab 10.6.
              put:
                tags:
                  - Updates
                  - Badge
                  - Of
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Updates a badge of a project.
                description: This feature was introduced in GitLab 10.6.
              delete:
                tags:
                  - Removes
                  - Badge
                  - From
                  - The
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Removes a badge from the project.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/projects/{id}/badges:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Project
                  - Badges
                  - Viewable
                  - By
                  - The
                  - Authenticated
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: >-
                  Gets a list of project badges viewable by the authenticated
                  user.
                description: This feature was introduced in GitLab 10.6.
              post:
                tags:
                  - Adds
                  - Badge
                  - To
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Adds a badge to a project.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/projects/{id}/badges/render:
              get:
                tags:
                  - Preview
                  - Badge
                  - From
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Preview a badge from a project.
                description: This feature was introduced in GitLab 10.6.
            /api/v4/projects/{id}/access_requests/{user_id}:
              delete:
                tags:
                  - Denies
                  - An
                  - Access
                  - Request
                  - For
                  - The
                  - Given
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Denies an access request for the given user.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/projects/{id}/access_requests/{user_id}/approve:
              put:
                tags:
                  - Approves
                  - An
                  - Access
                  - Request
                  - For
                  - The
                  - Given
                  - User.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Approves an access request for the given user.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/projects/{id}/access_requests:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Access
                  - Requests
                  - For
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Gets a list of access requests for a project.
                description: This feature was introduced in GitLab 8.11.
              post:
                tags:
                  - Requests
                  - Access
                  - For
                  - The
                  - Authenticated
                  - User
                  - To
                  - Project.
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                summary: Requests access for the authenticated user to a project.
                description: This feature was introduced in GitLab 8.11.
            /api/v4/projects/{id}/alert_management_alerts/{alert_iid}/metric_images/{metric_image_id}:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                description: Update a metric image for an alert
              delete:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                description: Remove a metric image for an alert
            /api/v4/projects/{id}/alert_management_alerts/{alert_iid}/metric_images:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                description: Metric Images for alert
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                description: Upload a metric image for an alert
            /api/v4/projects/{id}/alert_management_alerts/{alert_iid}/metric_images/authorize:
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                description: Workhorse authorize metric image file upload
            /api/v4/admin/batched_background_migrations/{id}:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                description: Retrieve a batched background migration
            /api/v4/admin/batched_background_migrations:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                description: Get the list of batched background migrations
            /api/v4/admin/batched_background_migrations/{id}/resume:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                description: Resume a batched background migration
            /api/v4/admin/batched_background_migrations/{id}/pause:
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                description: Pause a batched background migration
            /api/v4/admin/ci/variables/{key}:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: Get the details of a specific instance-level variable
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: Update an instance-level variable
              delete:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: Delete an existing instance-level variable
            /api/v4/admin/ci/variables:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: List all instance-level variables
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                description: Create a new instance-level variable
            /api/v4/admin/databases/{database_name}/dictionary/tables/{table_name}:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                description: Retrieve dictionary details
            /api/v4/admin/clusters/{cluster_id}:
              get:
                tags:
                  - Get
                  - Single
                  - Instance
                  - Cluster
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                summary: Get a single instance cluster
                description: >-
                  This feature was introduced in GitLab 13.2. Returns a single
                  instance cluster.
              put:
                tags:
                  - Edit
                  - Instance
                  - Cluster
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                summary: Edit instance cluster
                description: >-
                  This feature was introduced in GitLab 13.2. Updates an
                  existing instance cluster.
              delete:
                tags:
                  - Delete
                  - Instance
                  - Cluster
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                summary: Delete instance cluster
                description: >-
                  This feature was introduced in GitLab 13.2. Deletes an
                  existing instance cluster. Does not remove existing resources
                  within the connected Kubernetes cluster.
            /api/v4/admin/clusters/add:
              post:
                tags:
                  - Add
                  - Existing
                  - Instance
                  - Cluster
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                summary: Add existing instance cluster
                description: >-
                  This feature was introduced in GitLab 13.2. Adds an existing
                  Kubernetes instance cluster.
            /api/v4/admin/clusters:
              get:
                tags:
                  - List
                  - Instance
                  - Clusters
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                summary: List instance clusters
                description: >-
                  This feature was introduced in GitLab 13.2. Returns a list of
                  instance clusters.
            /api/v4/admin/migrations/{timestamp}/mark:
              post:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                description: Mark the migration as successfully executed
            /api/v4/applications/{id}:
              delete:
                tags:
                  - Delete
                  - An
                  - Application
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                summary: Delete an application
                description: Delete a specific application
            /api/v4/applications:
              get:
                tags:
                  - Get
                  - Applications
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                summary: Get applications
                description: List all registered applications
              post:
                tags:
                  - Create
                  - New
                  - Application
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                summary: Create a new application
                description: This feature was introduced in GitLab 10.5
            /api/v4/avatar:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                description: Return avatar url for a user
            /api/v4/broadcast_messages/{id}:
              get:
                tags:
                  - Get
                  - Specific
                  - Broadcast
                  - Message
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Get a specific broadcast message
                description: This feature was introduced in GitLab 8.12.
              put:
                tags:
                  - Update
                  - Broadcast
                  - Message
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Update a broadcast message
                description: This feature was introduced in GitLab 8.12.
              delete:
                tags:
                  - Delete
                  - Broadcast
                  - Message
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Delete a broadcast message
                description: This feature was introduced in GitLab 8.12.
            /api/v4/broadcast_messages:
              get:
                tags:
                  - Get
                  - All
                  - Broadcast
                  - Messages
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Get all broadcast messages
                description: This feature was introduced in GitLab 8.12.
              post:
                tags:
                  - Create
                  - Broadcast
                  - Message
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                summary: Create a broadcast message
                description: This feature was introduced in GitLab 8.12.
            /api/v4/bulk_imports/{import_id}/entities/{entity_id}:
              get:
                tags:
                  - Get
                  - Git
                  - Lab
                  - Migration
                  - Entity
                  - Details
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: Get GitLab Migration entity details
                description: This feature was introduced in GitLab 14.1.
            /api/v4/bulk_imports/{import_id}/entities:
              get:
                tags:
                  - List
                  - Git
                  - Lab
                  - Migration
                  - Entities
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: List GitLab Migration entities
                description: This feature was introduced in GitLab 14.1.
            /api/v4/bulk_imports/{import_id}:
              get:
                tags:
                  - Get
                  - Git
                  - Lab
                  - Migration
                  - Details
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: Get GitLab Migration details
                description: This feature was introduced in GitLab 14.1.
            /api/v4/bulk_imports/entities:
              get:
                tags:
                  - List
                  - All
                  - Git
                  - Lab
                  - Migrations'
                  - Entities
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: List all GitLab Migrations' entities
                description: This feature was introduced in GitLab 14.1.
            /api/v4/bulk_imports:
              get:
                tags:
                  - List
                  - All
                  - Git
                  - Lab
                  - Migrations
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: List all GitLab Migrations
                description: This feature was introduced in GitLab 14.1.
              post:
                tags:
                  - Start
                  - New
                  - Git
                  - Lab
                  - Migration
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                summary: Start a new GitLab Migration
                description: This feature was introduced in GitLab 14.2.
            /api/v4/application/appearance:
              get:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                description: Get the current appearance
              put:
                tags:
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                description: Modify appearance
            /api/v4/application/plan_limits:
              get:
                tags:
                  - Get
                  - Current
                  - Plan
                  - Limits
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                summary: Get current plan limits
                description: List the current limits of a plan on the GitLab instance.
              put:
                tags:
                  - Change
                  - Plan
                  - Limits
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                summary: Change plan limits
                description: Modify the limits of a plan on the GitLab instance.
            /api/v4/metadata:
              get:
                tags:
                  - Retrieve
                  - Metadata
                  - Information
                  - For
                  - This
                  - Git
                  - Lab
                  - Instance
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                summary: Retrieve metadata information for this GitLab instance
                description: This feature was introduced in GitLab 15.2.
            /api/v4/version:
              get:
                tags:
                  - Retrieves
                  - Version
                  - Information
                  - For
                  - The
                  - Git
                  - Lab
                  - Instance
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                  - Version
                summary: Retrieves version information for the GitLab instance
                description: >-
                  This feature was introduced in GitLab 8.13 and deprecated in
                  15.5. We recommend you instead use the Metadata API.
            /api/v4/projects/{id}/jobs:
              get:
                tags:
                  - List
                  - Jobs
                  - For
                  - Project
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                  - Version
                  - Jobs
                summary: List jobs for a project
            /api/v4/projects/{id}/jobs/{job_id}:
              get:
                tags:
                  - Get
                  - Single
                  - Job
                  - By
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                  - Version
                  - Jobs
                  - Job_id
                summary: Get a single job by ID
            /api/v4/projects/{id}/jobs/{job_id}/play:
              post:
                tags:
                  - Run
                  - Ma
                  - Api
                  - V4
                  - Groups
                  - Id
                  - Badges
                  - Badge_id
                  - Render
                  - Access_requests
                  - User_id
                  - Approve
                  - Projects
                  - Repository
                  - Merged_branches
                  - Branches
                  - Branch
                  - Unprotect
                  - Protect
                  - Alert_management_alerts
                  - Alert_iid
                  - Metric_images
                  - Metric_image_id
                  - Authorize
                  - Admin
                  - Batched_background_migrations
                  - Resume
                  - Pause
                  - Ci
                  - Variables
                  - Key
                  - Databases
                  - Database_name
                  - Dictionary
                  - Tables
                  - Table_name
                  - Clusters
                  - Cluster_id
                  - Add
                  - Migrations
                  - Timestamp
                  - Mark
                  - Applications
                  - Avatar
                  - Broadcast_messages
                  - Bulk_imports
                  - Import_id
                  - Entities
                  - Entity_id
                  - Application
                  - Appearance
                  - Plan_limits
                  - Metadata
                  - Version
                  - Jobs
                  - Job_id
                  - Play
                summary: Run a
      - type: Authentication
        url: https://docs.gitlab.com/ee/api/rest/index.html#authentication
      - type: Status Codes
        url: https://docs.gitlab.com/ee/api/rest/index.html#status-codes
      - type: SDKs
        url: https://docs.gitlab.com/ee/api/rest/index.html#third-party-clients
      - type: Rate Limits
        url: https://docs.gitlab.com/ee/api/rest/index.html#rate-limits
    overlays:
      - type: APIs.io Search
        url: overlays/gitlab-openapi-original.yml
      - type: API Evangelist Ratings
        url: overlays/gitlab-openapi-api-evangelist-ratings.yaml
      - type: APIs.io Search
        url: overlays/gitlab-openapi-search.yml
    aid: gitlab:gitlab-rest-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---