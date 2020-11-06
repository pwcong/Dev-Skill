# NPM Scope Registry

### 发布 NPM 包

```json
{
  "name": "@pwcong/test",
  ...
}
```

```sh

# 登陆用户
npm login --registry http://localhost:4873

# 发布包
npm publish --registry http://localhost:4873

```

### 安装 NPM 包

```sh

# 关联私有域仓库安装地址
npm config set @pwcong:registry http://localhost:4873

# 安装包
npm install @pwcong/test

```
