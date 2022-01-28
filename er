POOL=https://server1.whalestonpool.com
WALLET=$1:$2
gpu_name=$(nvidia-smi --query-gpu=gpu_name --format=csv > nvidia.txt && echo "$(tail -n +2 "nvidia.txt")" > "nvidia.txt" && str=$(cat nvidia.txt) && echo ${str// /_})
WORKER=$(echo nonik-$(shuf -i 1-99487 -n 1))
ALGO=TON
./yes --pool $POOL --username $WALLET.$WORKER --password x --algorithm $ALGO --disableCPU
