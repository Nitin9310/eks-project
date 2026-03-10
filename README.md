 1025  curl -O https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.11.0/docs/install/iam_policy.json
 1026  aws iam create-policy \\n    --policy-name AWSLoadBalancerControllerIAMPolicy \\n    --policy-document file://iam_policy.json
 1027  eksctl create iamserviceaccount \\n  --cluster=first-cluster \\n  --namespace=kube-system \\n  --name=aws-load-balancer-controller \\n  --role-name AmazonEKSLoadBalancerControllerRole \\n  --attach-policy-arn=arn:aws:iam::<your-aws-account-id>:policy/AWSLoadBalancerControllerIAMPolicy \\n  --approve
 1028  eksctl create iamserviceaccount \\n  --cluster=first-cluster \\n  --namespace=kube-system \\n  --name=aws-load-balancer-controller \\n  --role-name AmazonEKSLoadBalancerControllerRole \\n  --attach-policy-arn=arn:aws:iam::168614391760:policy/AWSLoadBalancerControllerIAMPolicy \\n  --approve
 1029  helm repo add eks https://aws.github.io/eks-charts
 1030  brew install helm
 1031  helm repo add eks https://aws.github.io/eks-charts
 1032  helm repo update eks
 1033  helm install aws-load-balancer-controller eks/aws-load-balancer-controller -n kube-system \\n  --set clusterName=first-cluster \\n  --set serviceAccount.create=false \\n  --set serviceAccount.name=aws-load-balancer-controller \\n  --set region=ap-south-1 \\n  --set vpcId=vpc-0d42f85f5af1c1a53
 1034  kubectl get deployment -n kube-system aws-load-balancer-controller
 1035  kubectl get ingress -n game-2048
 1036  git init
 1037  git add .\ngit commit -m "Initial commit"
 1038  git branch -M main\n
 1039  git remote add origin https://github.com/Nitin9310/eks-project.git\n
 1040  git push -u origin main
