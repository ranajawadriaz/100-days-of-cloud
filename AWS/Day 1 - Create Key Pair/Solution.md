<pre>
~ on ☁️  (us-east-1) ➜  ^C
~ 
~ on ☁️  (us-east-1) ✖ ^C
  (u
~ on ☁️  (us-east-1) ✖ ^C
➜ 
~ on ☁️  (us-east-1) ✖ aws sts get-caller-identity
{
    "UserId": "AIDAVJDPLDLUCNKJLD25L",
    "Account": "363158248168",
    "Arn": "arn:aws:iam::363158248168:user/kk_labs_user_633098"
}

~ on ☁️  (us-east-1) ➜  aws ec2 create-key-pair \
>   --key-name nautilus-kp \
>   --key-type rsa \
>   --query 'KeyMaterial' \
>   --output text > nautilus-kp.pem

~ on ☁️  (us-east-1) ➜  chmod 400 nautilus-kp.pem

~ on ☁️  (us-east-1) ➜  aws ec2 describe-key-pairs --key-names nautilus-kp
{
    "KeyPairs": [
        {
            "KeyPairId": "key-02c75c332d17adf7a",
            "KeyType": "rsa",
            "Tags": [],
            "CreateTime": "2026-01-08T15:27:02.704Z",
            "KeyName": "nautilus-kp",
            "KeyFingerprint": "db:52:6d:18:49:c6:18:7f:ee:c4:82:45:d9:ab:76:03:fc:e1:42:22"
        }
    ]
}

~ on ☁️  (us-east-1) ➜  
</pre>