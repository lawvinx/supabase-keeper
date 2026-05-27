# Supabase Keeper 🔋

自动保活 Supabase 免费项目，防止 7 天无活动被暂停。

## 已配置

- ✅ 每 6 天自动执行一次（GitHub Actions）
- ✅ 支持手动触发（Actions → Supabase Keep Alive → Run workflow）

## 下一步：配置 Secrets

进入仓库 → Settings → Secrets and variables → Actions → New repository secret

添加两个 Secret：

| Name | 说明 | 在哪找 |
|---|---|---|
| `SUPABASE_URL` | 项目 URL | Supabase Dashboard → Settings → API → URL |
| `SUPABASE_ANON_KEY` | Anon/Public Key | 同上 → `anon` `public` |

## 获取 Supabase 信息

1. 登录 https://supabase.com/dashboard
2. 进入你的项目
3. Project Settings → API
4. 复制 `URL` 和 `anon` `public` key

⚠️ 不要用 `service_role` key（以 `sbp_` 开头）

## 手动测试

配置完 Secrets 后：
1. 进入仓库 → Actions → Supabase Keep Alive
2. 点 "Run workflow"
3. 查看运行日志确认成功
