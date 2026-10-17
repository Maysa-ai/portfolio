# CSS structure

- `assets/css/tokens.css` documents the shared brand palette as reusable design tokens.
- `assets/css/blog-post.css` is shared by all four article pages; their CSS was identical, so it is stored once.
- Other page stylesheets are external files extracted in original rule order from the finalized HTML. This avoids changing the cascade during the first safe refactor.

## Why page-specific styles remain
The case studies and homepage have accumulated intentional, page-specific overrides from visual review. Removing or merging those rules without screenshot-based regression testing could change the approved design. The first pass therefore removes inline CSS and eliminates duplicated article CSS while preserving rule order. Further consolidation can follow after visual comparison at desktop and mobile widths.
