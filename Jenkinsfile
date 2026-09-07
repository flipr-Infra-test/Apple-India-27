@Library('ms-jenkins-global-lib') _

multipleFolderBuild(
    config: [
        domainWith: "subdomain",
        apiPath: "api",
        volumes: [uploads: []]
    ],
    apps: [
        [nextJs: [path: "web", node_version: "24"]],
        [nodeJs: [path: "api", node_version: "24", volumes: ["uploads:/app/uploads"]]],
        [reactJs: [path: "admin", node_version: "24"]]
    ]
)
