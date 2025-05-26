// Jenkinsfile
pipeline {
    agent any  // 使用任意可用代理（Jenkins节点）
    stages {
        // 阶段 1: 克隆仓库（自动触发，无需显式命令）
        stage('Clone Repository') {
            steps {
                script {
                    // Jenkins 会自动从GitHub克隆代码，此步骤仅为占位符
                    echo "Cloning repository from GitHub..."
                }
            }
        }
        // 阶段 2: 安装依赖
        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'  // Windows命令
            }
        }
        // 阶段 3: 运行测试
        stage('Run Tests') {
            steps {
                bat 'pytest test_main.py -v'  // -v 表示详细输出
            }
        }
    }
}
