---
agent: agent
description: 'Describe projects configuration'
---
# Step: Title
Add a subtitle "Project Configuration" to the output file.

# Step: Check application startup configuration
Call #file:./pqa_check_feature.prompt.md with parameter Configure application startup.
If the hosting model is SaaS, also call #file:./pqa_check_feature.prompt.md with parameter SaaS application startup configuration and include those findings in this check.
Based on the results, add one bullet point to the output file stating whether application startup is present and configured correctly.

# Step: Check middleware order
Call #file:./pqa_check_feature.prompt.md with parameter middleware have the recommended order.
Based on the result, add one bullet point to the output file stating whether the middleware order is correct.

# Step: Check Kentico route registration order
Examine the project's route registration and determine whether Kentico routes are registered before non-Kentico routes.
Based on the result, add one bullet point to the output file stating whether Kentico routes are correctly placed before non-Kentico routes.

# Step: Check NuGet package versions
Verify that the Kentico NuGet packages installed in the project are on the same version as the Kentico database version.
Based on the result, add one bullet point to the output file stating whether the NuGet package versions match the database version.

