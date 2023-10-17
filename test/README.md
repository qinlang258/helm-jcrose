# Rest Service

标准的后端rest服务，部署后通过指定的域名对外提供服务。

## Parameters

| Parameter                                   | Description                                         | Default                                                           |
|---------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------|
| `replicaCount`                              | 实例数                                               | `1`                                                               |
| `image.repository`                          | 镜像名                                               | `nil`                                                             |
| `image.tag`                                 | 镜像tag                                              | `latest`                                                          |
| `image.pullPolicy`                          | image pull policy                                   | `IfNotPresent`                                                    |
| `nameOverride`                              | String to partially override fullname template with a string (will prepend the release name) | `nil`                    |
| `fullnameOverride`                          | String to fully override fullname template with a string                                     | `nil`                    |
| `service.type`                              | 内部服务发现类型                                       | `ClusterIP`                                                       |
| `service.port`                              | 服务端口                                              | `8080`                                                            |
| `hostName`                                  | 配置域名                                              | `nil`                                                             |
| `ingress.enabled`                           | 是否启用ingress对外提供http服务                         | `true`                                                            |
| `configs.enabled`                           | 是否启用配置文件                                       | `true`                                                            |
| `configs.type`                              | 配置文件加载方式, `env`为环境变量方式，`file`为文件形式     | `env`                                                             |
| `configs.path`                              | `configs`.`type`为`file`时生效，配置以文件形式加载的路径   | `/configs`                                                       |
| `configs.data`                              | 配置文件内容，kv格式                                    | `nil`                                                            |
