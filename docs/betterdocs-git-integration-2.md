<h1>BetterDocs Git Integration</h1>

<!-- wp:paragraph -->
<p>Use when working with BetterDocs Git Integration — GitHub sync via OAuth proxy, GitLab sync via access token, GitIntegration class, GitHubSync class, GitHubOAuth class, GitIntegrationTest class, betterdocs-auth proxy, git_sync_document AJAX, git_pull_document AJAX, enable_git_integration setting, git_repository_url, git_branch, git_docs_directory, git_provider, _betterdocs_git_sync_enabled meta, _betterdocs_git_file_path, _betterdocs_git_commit_hash, markdown conversion, webhook handler, GitHubRepoSettings React component, betterdocs_git_webhook, gitlab_connect, gitlab_branches, gitlab_contents."</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Everything looks right. Here's a summary of what changed:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>includes/Core/GitIntegration.php (ajax_import_md)<br>- Removed the get_posts() lookup + wp_update_post() branch<br>- Now always calls wp_insert_post() — WordPress's wp_unique_post_slug() internally appends -2, -3, etc. when the slug already exists<br>- Imported doc is redirected to the new post's edit screen</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>react-src/admin/git-sync-modal/components/ImportPanel.js<br>- Removed the needsConfirm / "Overwrite existing docs?" SweetAlert flow entirely (no more async, no await, no confirmation)<br>- Clicking "Import Selected" now always fires immediately<br>- On success: shows a green "Imported!" toast, then navigates to the new post's editor after 1.2 s</p>
<!-- /wp:paragraph -->
