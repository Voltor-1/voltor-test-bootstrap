## Deploy: {product} to production

**Type:** deploy
**Agent:** deploy
**Priority:** P1

### Product
{product-slug}

### Environment
production

### Pre-flight options
- Run migrations: yes
- Run smoke tests: yes

### Context
Production deployment of {product} triggered by Founder approval.

### Acceptance Criteria
1. All pre-flight checks pass
2. Migrations applied successfully
3. Worker deployed and health check returns 200
4. Frontend built and deployed to Pages
5. Smoke test passes — POST /sessions returns 201 with shareToken
6. Deploy result posted to #executive with live URLs

### Definition of done
- [ ] deploy_product.sh exits 0
- [ ] Worker URL responding
- [ ] Pages URL responding
- [ ] Smoke test passed
- [ ] Deploy result posted to Slack #executive
