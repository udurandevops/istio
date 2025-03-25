# istio

curl -L https://istio.io/downloadIstio | sh -
cd istio-*
export PATH=$PWD/bin:$PATH

istioctl version #version check yap

istioctl install --set profile=default -y

kubectl get pods -n istio-system #pod'ların durumunu kontrol et

İstio mesh’e pod'ları dahil edebilmek için namespace’e otomatik sidecar injection’ı açılıyor;
- kubectl label namespace default istio-injection=enabled
