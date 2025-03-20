# Amazon Web Servisleri (AWS) ile Bulut Bilişim Notları

Bu döküman, Amazon Web Servisleri (AWS) ve bulut bilişim konularında alınan eğitim notlarını içermektedir. AWS'nin temel kavramları, hizmetleri, avantajları ve kullanım senaryoları gibi konulara dair özet bilgiler sunmayı amaçlamaktadır.

## İçindekiler

- [Amazon Web Servisleri (AWS) Nedir?](#amazon-web-servisleri-aws-nedir)
    - [AWS'nin Avantajları Nelerdir?](#awsnin-avantajları-nelerdir)
    - [AWS Hizmetlerine Kısa Bir Bakış](#aws-hizmetlerine-kısa-bir-bakış)
- [Amazon EC2 (Elastic Compute Cloud) Nedir?](#amazon-ec2-elastic-compute-cloud-nedir)
    - [EC2'nin Temel Kavramları Nelerdir?](#ec2nin-temel-kavramları-nelerdir)
    - [EC2'nin Avantajları Nelerdir?](#ec2nin-avantajları-nelerdir)
    - [EC2 İçin Kullanım Örnekleri](#ec2-için-kullanım-örnekleri)
- [AWS Auto Scaling (Autoscaler) Nedir ?](#aws-auto-scaling-autoscaler-nedir)
    - [Autoscaler Nasıl Çalışır?](#autoscaler-nasıl-çalışır)
    - [AWS Autoscaler Türleri Nelerdir?](#aws-autoscaler-türleri-nelerdir)
    - [Autoscaler Örneği](#autoscaler-örneği)
    - [AWS Autoscaler Kullanmanın Avantajları Nelerdir?](#aws-autoscaler-kullanmanın-avantajları-nelerdir)
- [AWS Load Balancer Nedir?](#aws-load-balancer-nedir)
    - [AWS Load Balancer Türleri Nelerdir?](#aws-load-balancer-türleri-nelerdir)
    - [Load Balancer Nasıl Çalışır?](#load-balancer-nasıl-çalışır)
    - [AWS Load Balancer Kullanmanın Avantajları Nelerdir?](#aws-load-balancer-kullanmanın-avantajları-nelerdir)
    - [Application Load Balancer (ALB)](#application-load-balancer-alb)
    - [Network Load Balancer (NLB)](#network-load-balancer-nlb)
    - [Sağlık Kontrolü (Health Check) Nedir?](#sağlık-kontrolü-health-check-nedir)
- [AWS Container Lambda Nedir?](#aws-container-lambda-nedir)
    - [Neden Container Lambda Kullanılır?](#neden-container-lambda-kullanılır)
    - [Container Lambda'nın Temel Özellikleri](#container-lambdanın-temel-özellikleri)
    - [AWS Container Lambda Nasıl Çalışır?](#aws-container-lambda-nasıl-çalışır)
    - [Container Lambda Kullanarak Bir Fonksiyon Nasıl Oluşturulur?](#container-lambda-kullanarak-bir-fonksiyon-nasıl-oluşturulur)
    - [Container Lambda'nın Avantajları Nelerdir?](#container-lambdanın-avantajları-nelerdir)
    - [Container Lambda Kullanım Senaryoları Nelerdir?](#container-lambda-kullanım-senaryoları-nelerdir)
- [AWS Depolama (Storage) Hizmetleri Nelerdir?](#aws-depolama-storage-hizmetleri-nelerdir)
    - [1. Amazon S3 (Simple Storage Service)](#1-amazon-s3-simple-storage-service)
    - [2. Amazon EBS (Elastic Block Store)](#2-amazon-ebs-elastic-block-store)
    - [3. Amazon EFS (Elastic File System)](#3-amazon-efs-elastic-file-system)
    - [4. Amazon S3 Glacier](#4-amazon-s3-glacier)
- [AWS Veritabanı Hizmetleri Nelerdir?](#aws-veritabanı-hizmetleri-nelerdir)
    - [1. Amazon RDS (Relational Database Service](#1-amazon-rds-relational-database-service)
    - [2. Amazon Aurora](#2-amazon-aurora)
    - [3. Amazon DynamoDB](#3-amazon-dynamodb)
    - [4. Amazon ElastiCache](#4-amazon-elasticache)
    - [5. Amazon Redshift](#5-amazon-redshift)
- [AWS Ağ (Network) Hizmetleri Nelerdir?](#aws-ağ-network-hizmetleri-nelerdir)
    - [1. Amazon VPC (Virtual Private Cloud)](#1-amazon-vpc-virtual-private-cloud)
    - [2. Subnet (Alt Ağ)](#2-subnet-alt-ağ)
    - [3. Internet Gateway (IGW)](#3-internet-gateway-igw)
    - [4. Route Tables (Yönlendirme Tabloları)](#4-route-tables-yönlendirme-tabloları)
    - [5. Security Groups ve Network ACLs](#5-security-groups-ve-network-acls)
    - [6. Elastic IP (EIP)](#6-elastic-ip-eip)
    - [7. Amazon Route 53](#7-amazon-route-53)
    - [8. Amazon CloudFront](#8-amazon-cloudfront)
- [AWS Hizmetlerine Erişim Yolları Nelerdir?](#aws-hizmetlerine-erişim-yolları-nelerdir)
    - [1. AWS Management Console (Web Arayüzü)](#1-aws-management-console-web-arayüzü)
    - [2. AWS CLI (Command Line Interface)](#2-aws-cli-command-line-interface)
    - [3. AWS SDK'ları (Software Development Kits)](#3-aws-sdkları-software-development-kits)
    - [4. AWS API (REST API)](#4-aws-api-rest-api)
    - [AWS Hizmetlerine Erişim İçin Güvenlik (IAM)](#aws-hizmetlerine-erişim-için-güvenlik-iam)
- [AWS Güvenlik ve Mevzuat Uyumluluğu](#aws-güvenlik-ve-mevzuat-uyumluluğu)
    - [AWS'de Güvenlik Nasıl Sağlanır?](#awsde-güvenlik-nasıl-sağlanır)
    - [1. Bulutun Güvenliği (AWS Tarafından Sağlanır)](#1-bulutun-güvenliği-aws-tarafından-sağlanır)
    - [2. Buluttaki Güvenlik (Kullanıcı Tarafından Sağlanır)](#2-buluttaki-güvenlik-kullanıcı-tarafından-sağlanır)
    - [3. Mevzuat Uyumluluğu (Compliance)](#3-mevzuat-uyumluluğu-compliance)
    - [AWS Güvenlik için En İyi Uygulamalar](#aws-güvenlik-için-en-iyi-uygulamalar)
- [AWS Kimlik ve Erişim Yönetimi (IAM)](#aws-kimlik-ve-erişim-yönetimi-iam)
    - [IAM Nedir ve Neden Önemlidir?](#iam-nedir-ve-neden-önemlidir)
    - [IAM Temel Kavramları Nelerdir?](#iam-temel-kavramları-nelerdir)
- [AWS Yönetim ve İdare Hizmetleri Nelerdir?](#aws-yönetim-ve-idare-hizmetleri-nelerdir)
    - [1. Amazon CloudWatch](#1-amazon-cloudwatch)
    - [2. AWS CloudTrail](#2-aws-cloudtrail)
    - [3. AWS Config](#3-aws-config)
    - [4. AWS CloudFormation](#4-aws-cloudformation)
    - [5. AWS Trusted Advisor](#5-aws-trusted-advisor)
    - [6. AWS Systems Manager](#6-aws-systems-manager)
    - [7. AWS Organizations](#7-aws-organizations)
    - [8. AWS Budgets](#8-aws-budgets)
    - [AWS Yönetimi İçin En İyi Uygulamalar](#aws-yönetimi-için-en-iyi-uygulamalar)
- [Kapanış ve Özet](#kapanış-ve-özet)
- [Eğitim İçeriğinde Neler Öğrendik?](#eğitim-içeriğinde-neler-öğrendik)
---

## Amazon Web Servisleri (Aws) Nedir?

Amazon Web Servisleri (AWS), Amazon tarafından sağlanan, dünyanın en yaygın kullanılan bulut bilişim platformlarından biridir. AWS, bilgi işlem gücü, depolama, veritabanları, makine öğrenimi, güvenlik, ağ yönetimi ve çok daha fazlasını içeren, geniş çaplı hizmetleri içerir. Bu hizmetler, şirketlerin ve bireylerin kendi fiziksel altyapılarını oluşturmadan, ihtiyaçları doğrultusunda kaynakları kiralayarak kullanabilmelerini sağlar.

###  AWS'nin Avantajları Nelerdir?
AWS bulut platformunu kullanmanın birçok avantajı vardır:

- Maliyet Tasarrufu: Sadece kullandığınız kaynaklar için ödeme yaparsınız. Donanım, bakım veya yönetim masraflarını azaltır.

- Ölçeklenebilirlik: İhtiyaçlarınıza göre kaynakları kolayca artırabilir veya azaltabilirsiniz.

- Esneklik ve Güvenilirlik: Çoklu bölge ve kullanılabilirlik alanları sayesinde yüksek düzeyde erişilebilirlik sunar.

- Güvenlik: AWS, güvenlik önlemleri için birçok araç ve sertifikasyon sunar.

- Hızlı Yenilik: Yeni teknolojileri ve araçları hızlıca kullanıma sunarak sürekli güncel kalmanızı sağlar.

### AWS Hizmetlerine Kısa Bir Bakış

**Amazon EC2 (Elastic Compute Cloud)**

- Sanal sunucular oluşturur ve yönetmenizi sağlar.
- İhtiyacınıza uygun işletim sistemi ve konfigürasyon seçebilirsiniz.

**Amazon S3 (Simple Storage Service)**

- Dosya ve nesne depolama hizmetidir.
- Yüksek dayanıklılık ve erişilebilirlik sunar.

**Amazon RDS (Relational Database Service)**

- İlişkisel veritabanlarını bulutta kolayca yönetir.
- MySQL, PostgreSQL, Oracle, SQL Server gibi veritabanları desteği sunar.

**AWS Lambda**

- Sunucusuz (serverless) uygulama geliştirmeye olanak sağlar.
- Kodunuzu tetikleyici (trigger) bir olay olduğunda otomatik çalıştırır.

---

## Amazon EC2 (Elastic Compute Cloud) Nedir?

Amazon EC2 (Elastic Compute Cloud), AWS tarafından sunulan, sanal sunucular oluşturmak ve yönetmek için kullanılan bulut tabanlı bir hizmettir. EC2 sayesinde fiziksel donanım yatırımı yapmak yerine, ihtiyaçlarınıza göre yapılandırılmış sanal makineleri (sunucuları) hızlıca oluşturabilir, çalıştırabilir ve yönetebilirsiniz.

### EC2'nin Temel Kavramları Nelerdir?

EC2'yi anlamak için bilmeniz gereken birkaç temel kavram vardır:

1. **Instance (Sunucu Örneği)**
- AWS üzerindeki sanal sunuculara Instance denir.
- İşlemci, RAM, disk gibi kaynakları yapılandırarak ihtiyaç duyduğunuz kadar instance oluşturabilirsiniz.

2. **AMI (Amazon Machine Image)**
- AMI, bir EC2 instance'ının başlatılmasını sağlayan şablonlardır.
- İşletim sistemi, uygulamalar ve yapılandırmaları içerebilir.
- AWS Marketplace üzerinde birçok hazır AMI bulunur ya da kendi AMI'nizi oluşturabilirsiniz.

3. **Instance Types (Örnek Türleri)**
- Kullanacağınız EC2 instance'larının kaynak kapasitesini belirleyen tiplerdir.
- CPU, RAM ve ağ performansı gibi farklı kaynak kapasitelerine sahip instance türleri vardır.
- Örneğin:
    - **t2.micro**: Küçük web uygulamaları veya test ortamları için ideal (AWS Free Tier kapsamında ücretsiz).
    - **m5.large**: Orta ölçekli uygulamalar için ideal, dengeli performans sağlar.
    - **c5.xlarge**: İşlem gücü yoğun görevler için uygundur.

### EC2'nin Avantajları Nelerdir?

- **Kolay Ölçeklenebilirlik**: İş yükünüz arttığında veya azaldığında kaynakları hızlıca ölçeklendirebilirsiniz.
- **Hızlı Başlangıç**: Dakikalar içinde yeni sunucu başlatabilirsiniz.
- **Çeşitli İşletim Sistemi Seçenekleri**: Linux, Windows gibi farklı işletim sistemlerini destekler.
- **Esnek ve Özelleştirilebilir Yapılandırma**: İşlemci, bellek, depolama ve ağ yapılandırmasını istediğiniz gibi seçebilirsiniz.
- **Maliyet Avantajı**: Kullanımınıza göre saatlik veya saniyelik ödeme yapılır.

### EC2 İçin Kullanım Örnekleri

EC2 farklı kullanım senaryolarına uygundur:

- **Web Uygulamaları**: Web siteleri ve uygulamalarınızı çalıştırmak için idealdir.
- **Test Ortamları**: Yazılım geliştirme ve test ortamlarını hızlıca kurup yönetebilirsiniz.
- **Veri Analizi**: Veri işleme ve analitik uygulamaları çalıştırabilirsiniz.
- **Makine Öğrenimi**: GPU ve CPU yoğun uygulamalar için kullanılabilir.

---

## AWS Auto Scaling (Autoscaler) Nedir?

AWS Auto Scaling, uygulamanızın değişen iş yüküne göre kaynakları otomatik olarak ölçeklendiren bir AWS servisidir. Trafik artışı sırasında sunucu kapasitenizi otomatik olarak artırırken, trafik azaldığında ise kaynakları azaltarak maliyetleri optimize eder. Böylece hem uygulamanızın erişilebilirliği ve performansı korunur, hem de gereksiz harcamalar önlenir.

### Autoscaler Nasıl Çalışır?

Auto Scaling, belirlediğiniz kurallar ve kriterlere göre sunucu sayısını otomatik olarak ayarlar. Bunu şu adımlarla gerçekleştirir:

- **CloudWatch ile İzleme**: CPU kullanımı, bellek, ağ trafiği gibi metrikleri izler.
- **Kuralların Kontrol Edilmesi**: Belirlediğiniz eşik değerler aşılırsa (örneğin CPU kullanımı %70'i geçerse) yeni sunucular eklenir veya azaltılır.
- **Scaling (Ölçekleme)**: Tanımladığınız min ve max değerlere göre kaynaklar eklenir ya da çıkarılır.

### AWS Autoscaler Türleri Nelerdir?

AWS'te iki temel autoscaler türü vardır:

1. **EC2 Auto Scaling**

- EC2 instance’larınızı otomatik olarak ölçeklendirmeye yarar.
- Önceden belirlediğiniz koşullara göre instance sayısını artırır veya azaltır.
2. **Application Auto Scaling**

- EC2 dışında başka AWS servislerini ölçeklendirir.
- Örneğin: DynamoDB tabloları, ECS görevleri, Aurora veritabanları vs.

### Autoscaler Örneği

Örnek bir senaryo üzerinden inceleyelim:

**Senaryo**: Bir web uygulamanız var ve trafiğe göre ölçeklendirmek istiyorsunuz.

- Minimum Instance: 2
- Maksimum Instance: 6
- Ölçeklendirme Politikası:
    - CPU %60 üzerindeyse 1 sunucu ekle
    - CPU %30 altındaysa 1 sunucu çıkar

AWS Auto Scaling, CPU kullanımı sürekli takip ederek kaynakları bu kurallar doğrultusunda otomatik ölçeklendirecektir.

### AWS Autoscaler Kullanmanın Avantajları Nelerdir?

**Yüksek Kullanılabilirlik**: Uygulama kapasitesini talepler doğrultusunda otomatik ayarlar ve erişilebilirliği artırır.

**Maliyet Optimizasyonu**: Gereksiz kapasiteyi azaltarak tasarruf sağlar.

**Otomasyon**: Manuel müdahale ihtiyacını azaltır ve operasyonel yükü hafifletir.

**Esneklik**: Değişken yük durumlarına hızlı tepki vererek performansı sabit tutar.

---

## AWS Load Balancer Nedir?

AWS Load Balancer, gelen trafiği birden fazla sunucuya (EC2 instance’ına) dağıtarak uygulamanızın erişilebilirliğini, ölçeklenebilirliğini ve performansını artıran bir servistir. Trafiği yönetirken, sunucuların yükünü eşit şekilde dağıtır ve böylece sunucuların aşırı yüklenmesini engeller.

### AWS Load Balancer Türleri Nelerdir?

AWS üzerinde temel olarak üç farklı Load Balancer türü bulunur:

- **Application Load Balancer (ALB)**: HTTP/HTTPS trafiğini yönetir, katman 7’de çalışır, gelişmiş routing özelliklerine sahiptir. (Web uygulamaları, REST API'ler, microservice mimarileri)
- **Network Load Balancer (NLB)**: TCP, UDP ve TLS protokollerini yönetir, yüksek performanslıdır, katman 4'te çalışır. (Çok yüksek performans ve düşük gecikme isteyen uygulamalar)
- **Gateway Load Balancer (GLB)**: Üçüncü parti firewall veya güvenlik cihazları için kullanılır. (Güvenlik duvarı veya üçüncü parti servis entegrasyonları)

### Load Balancer Nasıl Çalışır?

- Kullanıcıdan istek alır.
- Belirlenmiş kurallara göre trafiği uygun sunucuya yönlendirir.
- Sunucuların sağlık durumunu (Health Check) kontrol eder.
- Sağlıksız sunucuları devre dışı bırakır, trafik göndermez.
- Yeni sunucular eklendikçe otomatik olarak devreye alır.

### AWS Load Balancer Kullanmanın Avantajları Nelerdir?

**Yüksek Kullanılabilirlik (High Availability)**: Sağlıksız instance’ları devreden çıkararak erişilebilirliği artırır.

**Performans Artışı**: Trafik dengeli dağıldığı için sunucuların yükü hafifler ve performans artar.

**Otomatik Ölçeklenebilirlik**: Yeni sunucular eklendikçe otomatik olarak algılar ve trafik gönderir.

**Esneklik**: Trafiği farklı routing kurallarıyla yönetebilir, HTTP header veya path gibi kriterlerle yönlendirme yapabilirsiniz.

**Güvenlik**: SSL/TLS sertifikalarını yönetebilir, HTTPS trafiğini sonlandırarak ekstra güvenlik sağlar.


### Application Load Balancer (ALB)

Application Load Balancer, HTTP/HTTPS protokollerini kullanan web uygulamaları için idealdir ve OSI modelinin 7. katmanında çalışır.

**ALB Özellikleri**

- URL tabanlı yönlendirme yapılabilir.
- SSL/TLS sonlandırma ve yönetimi yapabilir.
- Gelişmiş HTTP header tabanlı yönlendirme sağlar.
- Websocket ve HTTP/2 desteği vardır.

**ALB Kullanım Senaryoları**

- Mikro servis mimarileri.
- Web tabanlı uygulamalar.

### Network Load Balancer (NLB)

Network Load Balancer, yüksek performans gerektiren durumlarda kullanılır. TCP/UDP gibi protokoller üzerinde çalışır (Layer 4).

**NLB Özellikleri**

- Çok düşük gecikme süreleri sunar.
- Statik IP adresi desteği sağlar.
- Yüksek miktarda eş zamanlı bağlantıyı kaldırabilir.

**NLB Kullanım Senaryoları**

- Oyun sunucuları.
- Video streaming platformları.
- Yüksek performans gerektiren uygulamalar.

### Sağlık Kontrolü (Health Check) Nedir?

Load Balancer, uygulamanızın sürekli erişilebilir olduğundan emin olmak için düzenli olarak "sağlık kontrolü" yapar.

- Sağlıksız sunucular otomatik olarak yük dağılımından çıkarılır.
- Yeniden sağlıklı duruma döndüklerinde otomatik olarak tekrar devreye girerler.

Örneğin, bir HTTP health check aşağıdaki gibi tanımlanabilir:

- Path: `/health`
- Success Codes: `200`
- Interval: `30 saniye`
- Timeout: `5 saniye`
- Healthy Threshold: `2`
- Unhealthy Threshold: `2`

---

## AWS Container Lambda Nedir?

AWS Container Lambda, AWS Lambda fonksiyonlarını Docker konteynerleri içinde çalıştırmanıza olanak tanıyan bir yöntemdir. Standart Lambda fonksiyonlarının boyut (250 MB) veya çalışma ortamı kısıtlamalarına takılmadan, uygulamalarınızı konteyner tabanlı olarak AWS Lambda üzerinde çalıştırabilirsiniz.

### Neden Container Lambda Kullanılır?

Standart AWS Lambda fonksiyonları basit, hafif ve hızlıdır; ancak bazı durumlarda yeterli olmayabilir. Özellikle aşağıdaki durumlarda Container Lambda tercih edilir:

- Lambda paket boyutu limiti (250 MB) aşılırsa,
- Özel runtime veya kütüphaneler gerekliyse,
- Containerize edilmiş mevcut uygulamalar Lambda üzerinde çalıştırılmak isteniyorsa.

### Container Lambda'nın Temel Özellikleri

- 10 GB'a kadar konteyner imajı desteği
- 15 dakikaya kadar çalışma süresi
- Docker imajları ile kolay entegrasyon
- ECR (Elastic Container Registry) üzerinden entegrasyon
- Özel çalışma ortamı (custom runtime) oluşturma imkânı

### AWS Container Lambda Nasıl Çalışır?

- Uygulamanız Docker imajı olarak paketlenir ve ECR üzerine yüklenir.
- Lambda fonksiyonu oluşturulur ve kaynak olarak bu Docker imajı gösterilir.
- Fonksiyon tetiklendiğinde, Lambda servisi otomatik olarak bu konteyner imajını başlatır ve çalıştırır.
- Lambda, gelen isteklere göre konteyner içindeki kodunuzu çalıştırır ve sonuçları döner.

### Container Lambda Kullanarak Bir Fonksiyon Nasıl Oluşturulur?

1. Dockerfile Hazırlama

Öncelikle Lambda uyumlu Dockerfile oluşturmalısınız:

```dockerfile
FROM public.ecr.aws/lambda/dotnet:6

COPY --from=build /app/bin/Release/net6.0/publish/ ${LAMBDA_TASK_ROOT}

CMD ["ContainerLambda::ContainerLambda.Function::FunctionHandler"]
```

2. C# Lambda Fonksiyonu (`Function.cs`)

```csharp
using System.Collections.Generic;
using Amazon.Lambda.Core;
using Amazon.Lambda.APIGatewayEvents;

// Assembly attribute to enable the Lambda function's JSON input to be converted into a .NET class.
[assembly: LambdaSerializer(typeof(Amazon.Lambda.Serialization.SystemTextJson.DefaultLambdaJsonSerializer))]

namespace ContainerLambda.Function;

public class Function
{
    public APIGatewayProxyResponse FunctionHandler(APIGatewayProxyRequest request, ILambdaContext context)
    {
        return new APIGatewayProxyResponse
        {
            StatusCode = 200,
            Body = "Merhaba AWS Container Lambda!",
            Headers = new Dictionary<string, string> { { "Content-Type", "text/plain" } }
        };
    }
}
```

3. Docker İmajını Oluşturup ECR'a Yükleyin

```bash
# Docker imajını build edin
docker build -t container-lambda-demo .

# AWS ECR'ye giriş yapın (region bilgisi ile)
aws ecr get-login-password --region <region> | docker login --username AWS --password-stdin <account_id>.dkr.ecr.<region>.amazonaws.com

# Docker imajını ECR'ye push edin
docker tag container-lambda-demo:latest <account_id>.dkr.ecr.<region>.amazonaws.com/container-lambda-demo:latest
docker push <account_id>.dkr.ecr.<region>.amazonaws.com/container-lambda-demo:latest
```

### Container Lambda'nın Avantajları Nelerdir?

**Esneklik**: Özel çalışma ortamları ve bağımlılıkları Lambda'ya taşır.

**Uygulama Taşınabilirliği**: Docker ile paketlenen mevcut uygulamalarınızı kolayca Lambda'ya aktarabilirsiniz.

**Daha Fazla Kaynak Kullanımı**: Standart Lambda sınırlarını aşan büyük paketleri kullanabilirsiniz.

_Container Lambda'nın Dezavantajları Var mı?_

Konteynerlerin açılması ve çalıştırılması standart Lambda'ya göre biraz daha uzun sürebilir (Cold Start).
Docker imajı boyutu arttıkça soğuk başlatma süreleri artabilir.

### Container Lambda Kullanım Senaryoları Nelerdir?

- Büyük boyutlu kütüphaneler kullanan makine öğrenimi modelleri
- Özel runtime ortamları (örneğin Rust, C++, özel derlenmiş uygulamalar)
- Mevcut konteyner tabanlı uygulamaları serverless mimariye taşımak isteyenler

---

## AWS Depolama (Storage) Hizmetleri Nelerdir?

AWS depolama hizmetleri, uygulamalarınızın verilerini güvenli, esnek ve ölçeklenebilir bir şekilde saklamanızı sağlar. AWS, farklı ihtiyaçlara yönelik çeşitli depolama çözümleri sunmaktadır:

- Nesne Depolama: Amazon S3
- Blok Depolama: Amazon EBS
- Dosya Depolama: Amazon EFS
- Arşivleme: Amazon S3 Glacier

### 1. Amazon S3 (Simple Storage Service)

Amazon S3, internet üzerinde nesne (object) tabanlı bir veri depolama hizmetidir. Görseller, videolar, loglar gibi her türlü dosyayı saklayabilir, web üzerinden kolayca erişebilirsiniz.

**Amazon S3'nin Özellikleri**:

- Yüksek dayanıklılık: %99.999999999 (11 dokuz) dayanıklılık oranı.
- Kolay erişim: HTTP veya HTTPS üzerinden erişim.
- Ölçeklenebilirlik: Kapasitesi neredeyse sınırsızdır.
- Versiyonlama: Dosyaların eski sürümlerini saklayabilir.
- Güvenlik: Bucket Policy, IAM, Encryption gibi çeşitli güvenlik yöntemleri sunar.

**Kullanım Örneği**:

```bash
# Dosya yükleme (AWS CLI)
aws s3 cp dosya.txt s3://mybucket/dosya.txt
```

### 2. Amazon EBS (Elastic Block Store)


Amazon EBS, EC2 instance'ları için blok tabanlı depolama hizmetidir. Bilgisayarınızdaki sabit disk gibi çalışır, ancak bulutta tutulur ve EC2 instance'larına bağlanarak kullanılır.

**Amazon EBS'nin Özellikleri**:

- Hızlı ve tutarlı performans: SSD veya HDD seçenekleri vardır.
- Snapshot ile yedekleme: Veri yedeklerini alıp saklayabilir ve geri yükleyebilirsiniz.
- Esneklik: Boyutu ve performansı sonradan değiştirilebilir.

**Kullanım Senaryoları**:
- İşletim sistemi diskleri
- Veritabanları ve uygulama diskleri

### 3. Amazon EFS (Elastic File System)

Amazon EFS, bulut tabanlı, esnek ve paylaşımlı dosya depolama hizmetidir. Birden fazla EC2 sunucusu arasında ortak kullanılabilir.

**Amazon EFS'nin Özellikleri**:

- Paylaşımlı kullanım: Birden fazla sunucu tarafından aynı anda kullanılabilir.
- Ölçeklenebilir: Otomatik olarak kapasiteyi artırıp azaltır.
- Yüksek kullanılabilirlik: Birden fazla erişilebilirlik bölgesinde otomatik çoğaltılır.

**Kullanım Senaryoları**:

- İçerik yönetim sistemleri (CMS)
- Büyük veri uygulamaları
- Paylaşılan depolama gerektiren uygulamalar

### 4. Amazon S3 Glacier

S3 Glacier, düşük maliyetli ve uzun süreli veri arşivleme çözümüdür. Yıllarca erişim gerektirmeyen verileri düşük maliyetle saklamak için idealdir.

**Amazon S3 Glacier'ın Özellikleri**:

- Düşük maliyet: Çok uygun fiyatlarla uzun vadeli veri saklar.
- Uzun vadeli arşivleme: Veriler uzun süreli saklanır.
- Erişim süreleri: Dakikalar veya saatler içinde verileri geri alabilirsiniz.

**Kullanım Senaryoları**:

- Yasal uyumluluk için veri saklama
- Eski verilerin arşivlenmesi
- Felaket kurtarma ve uzun vadeli yedeklemeler

_Hangi AWS Depolama Hizmeti Seçilmeli?_

- Statik içerik ve web dosyaları: **Amazon S3**
- Veritabanları ve uygulama diskleri: **Amazon EBS**
- Birden fazla sunucunun paylaştığı veriler: **Amazon EFS**
- Uzun süre erişilmeyen verilerin arşivlenmesi: **Amazon Glacier**

---

## AWS Veritabanı Hizmetleri Nelerdir?

AWS, çeşitli uygulama ihtiyaçlarına cevap verebilmek için geniş bir veritabanı hizmetleri yelpazesine sahiptir. İlişkisel (SQL) veya ilişkisel olmayan (NoSQL) veritabanları, yüksek performans, ölçeklenebilirlik ve güvenilirlik için tasarlanmıştır.

AWS'nin temel veritabanı hizmetleri:

- Amazon RDS (Relational Database Service)
- Amazon Aurora
- Amazon DynamoDB
- Amazon ElastiCache
- Amazon Redshift

### 1. Amazon RDS (Relational Database Service)

Amazon RDS, ilişkisel veritabanlarını bulutta kolayca kurup yönetmenizi sağlar. MySQL, PostgreSQL, MariaDB, Oracle ve SQL Server gibi popüler ilişkisel veritabanı motorlarını destekler.

**Amazon RDS Özellikleri**

- Otomatik yedekleme ve geri yükleme
- Yüksek erişilebilirlik için Multi-AZ desteği
- Kolay ölçeklenebilirlik
- Otomatik güvenlik güncellemeleri ve yamalar

**Kullanım Örneği**:

- Kurumsal web uygulamaları
- Mobil uygulama backendleri
- İçerik yönetim sistemleri (CMS)

### 2. Amazon Aurora

Amazon Aurora, AWS tarafından geliştirilen, MySQL ve PostgreSQL uyumlu, yüksek performanslı ilişkisel bir veritabanı hizmetidir. Geleneksel veritabanlarına göre 5 kat daha hızlı performans sağlayabilir.

**Amazon Aurora Özellikleri**

- MySQL ve PostgreSQL ile tam uyumludur.
- Çok yüksek performans ve düşük gecikme sağlar.
- Depolama alanı otomatik olarak ölçeklendirilir (128 TB'a kadar).
- Multi-AZ desteği ve otomatik yedekleme sağlar.

**Kullanım Örneği**:

- Büyük ölçekli web ve mobil uygulamalar
- Yüksek trafikli e-ticaret uygulamaları
- Kurumsal kritik iş uygulamaları

### 3. Amazon DynamoDB

Amazon DynamoDB, tamamen yönetilen, ölçeklenebilir, hızlı, NoSQL bir veritabanı hizmetidir. Yapısal olmayan veriler ve büyük veri uygulamaları için idealdir.

**Amazon DynamoDB Özellikleri**
- Düşük gecikme (milisaniye seviyesinde)
- Otomatik ölçeklenir ve kapasite ayarlarını kendisi yapar.
- Yüksek erişilebilirlik sağlar.
- Anahtar-değer ve belge (JSON) yapısını destekler.

**Kullanım Örneği**:
- Mobil ve IoT uygulamaları
- Gerçek zamanlı oyunlar
- Büyük ölçekli web uygulamaları (ör. sosyal medya)

### 4. Amazon ElastiCache

Amazon ElastiCache, Redis ve Memcached gibi popüler bellek-içi (in-memory) veritabanı sistemlerini yönetir. Sık erişilen verileri önbelleğe alarak uygulamaların performansını artırır.

**Amazon ElastiCache Özellikleri**
- Yüksek performanslı, düşük gecikmeli veri erişimi sağlar.
- Tam yönetimli (bakım ve güncellemeler AWS tarafından yapılır).
- Ölçeklenebilir ve yüksek erişilebilirlik sunar.

**Kullanım Örneği**:
- Oturum yönetimi (session management)
- Önbelleğe alma (caching)
- Gerçek zamanlı analitik uygulamaları

### 5. Amazon Redshift

Amazon Redshift, AWS tarafından sunulan veri ambarı (data warehouse) hizmetidir. Büyük ölçekli veri analizi ve raporlama için kullanılır.

**Amazon Redshift Özellikleri**
- Petabayt ölçeğinde verileri analiz edebilir.
- Yüksek performanslı sorgular için optimize edilmiştir.
- AWS'nin diğer servisleriyle entegre çalışır (ör. S3, QuickSight).

**Kullanım Örneği**:
- İş zekası (BI) uygulamaları
- Büyük veri analizleri
- Veri ambarı çözümleri

_Hangi AWS Veritabanı Hizmeti Seçilmeli?_

- Klasik ilişkisel uygulamalar için: **RDS**
- Yüksek performanslı ve ilişkisel uygulamalar için: **Aurora**
- Mobil ve ölçeklenebilir uygulamalar için: **DynamoDB**
- Önbellekleme ve oturum yönetimi için: **ElastiCache**
- Büyük veri ve analiz işlemleri için: **Redshift**

---

## AWS Ağ (Network) Hizmetleri Nelerdir?

AWS, bulut ortamında güvenli, esnek ve ölçeklenebilir ağ altyapısı kurmanızı sağlayan çeşitli ağ (network) hizmetleri sunar. AWS Network servisleri sayesinde kaynaklarınızı izole edebilir, ağ trafiğinizi yönetebilir, güvenliğinizi artırabilir ve uygulama performansını yükseltebilirsiniz.

**AWS üzerindeki temel ağ servisleri şunlardı**r:

- VPC (Virtual Private Cloud)
- Subnet (Alt Ağ)
- Internet Gateway
- Route Tables
- Security Groups ve Network ACLs
- Elastic IP (EIP)
- Route 53
- CloudFront

### 1. Amazon VPC (Virtual Private Cloud)

Amazon VPC, AWS üzerinde kendi özel ağınızı oluşturmanıza olanak tanır. Bu sayede kendi mantıksal izolasyonunuza sahip, güvenli ve kontrol edilebilir bir ağ altyapısı kurabilirsiniz.

**VPC'nin Temel Özellikleri**:
- Kendi IP adres aralığınızı belirleyebilirsiniz.
- Alt ağlar (Subnet'ler) oluşturabilirsiniz.
- İnternet erişimini yönetebilirsiniz.
- Güvenlik kurallarını (Security Group ve NACL) belirleyebilirsiniz.

### 2. Subnet (Alt Ağ)

Subnet'ler, VPC içerisindeki daha küçük ağ segmentleridir. Kaynaklarınızı mantıksal olarak gruplandırmak için kullanılır. Subnet'ler genel (public) veya özel (private) olarak oluşturulabilir.

**Public Subnet**: İnternet erişimi bulunan kaynaklar için.

**Private Subnet**: İnternet erişimi olmayan, izole kaynaklar için.

### 3. Internet Gateway (IGW)

VPC'nizin dış dünya ile (internetle) bağlantısını sağlar. Bir VPC’ye yalnızca bir IGW ekleyebilirsiniz. IGW sayesinde Public Subnet'ler internete erişebilir.

### 4. Route Tables (Yönlendirme Tabloları)

Subnet'lerin trafik yönlendirme kurallarını belirlemek için kullanılır. Hangi trafiğin nereye yönlendirileceğini belirleyebilirsiniz.

**Örneğin**:

`0.0.0.0/0` yönlendirmesi, tüm internet trafiğini Internet Gateway'e yönlendirir.

Özel subnetler için NAT Gateway'e yönlendirme yapılır.

### 5. Security Groups ve Network ACLs

Security Group'lar, EC2 instance seviyesinde çalışan bir güvenlik duvarıdır (Firewall). Trafiği instance seviyesinde kontrol eder.

**Örneğin**:

HTTP (80), HTTPS (443) ve SSH (22) portlarını açabilirsiniz.

### 6. Elastic IP (EIP)

AWS'de sabit ve statik IP adresleri sağlar. EC2 instance'larınıza veya NAT Gateway’lere bağlanabilir ve adresler instance'lar arası taşınabilir.

### 7. Amazon Route 53

AWS’nin DNS (Domain Name System) servisidir. Alan adlarını IP adresleriyle eşleştirir ve DNS yönetimini kolaylaştırır.

**Route 53 Özellikleri**:
- Alan adı kaydı (domain registration)
- DNS yönetimi
- Sağlık kontrolü (Health Check)
- Yük dağılımı ve yönlendirme (Routing)

### 8. Amazon CloudFront

Amazon CloudFront, içerik dağıtım ağıdır (CDN - Content Delivery Network). İçeriğinizi dünya genelindeki kullanıcılarınıza daha hızlı ulaştırmak için kullanılır.

**CloudFront Özellikleri**:
- İçeriği dünya çapında konumlandırılmış sunucular üzerinden dağıtır.
- Performansı ve kullanıcı deneyimini artırır.
- DDoS koruması sağlar (AWS Shield entegrasyonu).

### AWS Ağ Altyapısı Örneği

```
VPC (10.0.0.0/16)
│
├── Public Subnet (10.0.1.0/24)
│   ├── EC2 (Web Sunucuları)
│   └── Internet Gateway (IGW)
│
├── Private Subnet (10.0.2.0/24)
│   ├── EC2 (Veritabanı Sunucuları)
│   └── NAT Gateway (internete çıkış için)
│
└── Route Tables
    ├── Public Subnet için: 0.0.0.0/0 → IGW
    └── Private Subnet için: 0.0.0.0/0 → NAT Gateway
```

---

## AWS Hizmetlerine Erişim Yolları Nelerdir?

AWS servislerine çeşitli yöntemlerle erişebilirsiniz. Bu yöntemler, kullanıcıların veya uygulamaların AWS hizmetleriyle nasıl etkileşimde bulunacağına göre belirlenir. Başlıca erişim yöntemleri şunlardır:

- AWS Management Console (Web Arayüzü)
- AWS CLI (Command Line Interface)
- AWS SDK'ları (Software Development Kits)
- API'ler (Application Programming Interface)

### 1. AWS Management Console (Web Arayüzü)

AWS hizmetlerine erişmenin en yaygın yolu AWS Management Console kullanmaktır. Bu yöntem, tarayıcı tabanlı, görsel arayüz sunar.

**Avantajları**:
- Kullanımı kolay ve kullanıcı dostudur.
- Görsel olarak kaynak yönetimini sağlar.
- Hızlı kurulum ve yapılandırma yapabilirsiniz.

### 2. AWS CLI (Command Line Interface)

AWS CLI, komut satırından AWS servisleriyle etkileşim kurmayı sağlar. İşlemleri hızlı ve otomatikleştirilmiş bir biçimde yapabilirsiniz.

**Avantajları**:
- Otomatikleştirme ve script'lerle kolay entegrasyon sağlar.
- Birden fazla işlemi hızlıca gerçekleştirme imkânı sunar.

**AWS CLI Kurulumu ve Kullanımı**:

Kurulum (Örnek: Linux):

```bash
pip install awscli
```

AWS hesabını yapılandırma:
```bash
aws configure
```

Örnek kullanım:
```bash
aws ec2 describe-instances
```

### 3. AWS SDK'ları (Software Development Kits)

AWS SDK'ları, popüler programlama dilleriyle uygulamalarınızdan AWS servislerini kullanmanızı sağlar.

**Desteklenen dillerden bazıları**:
- .NET
- Python (boto3)
- Java
- JavaScript
- Go
- Ruby
- PHP

**Avantajları**:

Kod tabanlı yönetim ve entegrasyon sağlar.

Servisleri uygulama seviyesinde kullanabilirsiniz.

### 4. AWS API (REST API)

AWS hizmetlerine REST API'leri üzerinden doğrudan erişebilirsiniz. AWS SDK ve CLI da arka planda bu API'leri kullanır.

**Avantajları**:

Tüm servislerle doğrudan HTTP istekleri üzerinden etkileşim.

SDK ve CLI kullanmadan doğrudan erişim.

**API Örneği (HTTP GET ile EC2 Örneklerini Listeleme)**:

```http request
GET https://ec2.amazonaws.com/?Action=DescribeInstances
&Version=2016-11-15
&AUTHPARAMS
```

### AWS Hizmetlerine Erişim İçin Güvenlik (IAM)

AWS üzerindeki kaynaklara erişimi kontrol etmek için IAM (Identity and Access Management) kullanılır:

- Kullanıcılara, gruplara ve servislere farklı yetkiler atanabilir.
- Güvenli erişim için IAM rollerini ve politikalarını kullanmak önerilir.

Örneğin:

- EC2 instance’ına sadece belirli kullanıcıların erişebilmesi.
- S3 bucket’ına sadece belirli uygulamanın yazabilmesi.


| Yöntem | Kullanım Kolaylığı | Otomasyon | Görsel Yönetim | Kimler İçin Uygun? |
|--------|-------------------|-----------|----------------|-------------------|
| AWS Console | ✅ Çok Kolay | ❌ Hayır | ✅ Evet | Başlangıç seviyesi, yöneticiler |
| AWS CLI | 🟡 Orta | ✅ Evet | ❌ Hayır | Sistem yöneticileri, geliştiriciler |
| AWS SDK | 🟡 Orta | ✅ Evet | ❌ Hayır | Yazılım geliştiriciler |
| AWS API | 🔴 Zor | ✅ Evet | ❌ Hayır | İleri seviye entegrasyon ve geliştirme |

---

## AWS Güvenlik ve Mevzuat Uyumluluğu

AWS, bulut platformunda güvenliği en yüksek öncelik olarak kabul eder ve kullanıcılarının güvenliğini sağlamak için birçok araç ve hizmet sunar. Ayrıca AWS, çeşitli mevzuat ve güvenlik standartlarına uyumlu olacak şekilde tasarlanmıştır.

### AWS'de Güvenlik Nasıl Sağlanır?

AWS güvenliği üç temel katmanda ele alınır:

- Bulutun Güvenliği (AWS tarafından sağlanır)
- Buluttaki Güvenlik (Kullanıcı tarafından sağlanır)
- Uyumluluk ve Mevzuat

### 1. Bulutun Güvenliği (AWS Tarafından Sağlanır)

AWS, altyapı güvenliğinden sorumludur. Bu katmanda sağlanan güvenlik önlemleri şunları içerir:

- Fiziksel veri merkezlerinin korunması (güvenlik kameraları, erişim kontrolü)
- Ağ altyapısının korunması (Firewall, DDoS saldırı koruması gibi)
- Veri merkezlerinde donanımsal izolasyon ve yedeklilik sağlanması

**AWS tarafından sağlanan güvenlik araçları**:
- AWS Shield (DDoS saldırı koruması)
- AWS WAF (Web uygulamaları için güvenlik duvarı)
- AWS Inspector (Güvenlik açıkları değerlendirme aracı)

### 2. Buluttaki Güvenlik (Kullanıcı Tarafından Sağlanır)

Kullanıcı olarak AWS üzerinde oluşturduğunuz kaynakların güvenliğinden sorumlusunuz. Bu katmanda sağlanması gereken güvenlik önlemleri şunları kapsar:

- IAM (Identity and Access Management) ile kullanıcı yetkilendirme
- Güvenlik Grupları (Security Groups) ile sunucu güvenliği
- Veri şifreleme (Encryption) uygulamaları
- Güvenli Ağ Yapılandırması (VPC, Subnet, NACL gibi)

**Kullanıcı tarafından yönetilen güvenlik araçları ve yöntemleri**:
- AWS IAM: Kullanıcı ve kaynak bazlı erişim yönetimi
- KMS (Key Management Service): Şifreleme anahtarlarının güvenli yönetimi
- CloudTrail: AWS kaynaklarının kullanım takibi ve kayıt altına alınması (audit logging)
- CloudWatch: İzleme ve alarm oluşturma

### 3. Mevzuat Uyumluluğu (Compliance)

AWS, kullanıcılarının çeşitli güvenlik standartlarına ve mevzuata uyum sağlamasına yardımcı olacak şekilde tasarlanmıştır. AWS, aşağıdaki mevzuatlara ve güvenlik standartlarına uyumludur:

- GDPR (Genel Veri Koruma Yönetmeliği)
- ISO 27001, 27017, 27018 (Bilgi Güvenliği Standartları)
- SOC 1, SOC 2, SOC 3 (Servis Organizasyonu Kontrolü Standartları)
- HIPAA (ABD Sağlık Sigortası Bilgi Taşınabilirlik ve Hesap Verebilirlik Yasası)
- PCI DSS (Ödeme Kartı Endüstrisi Veri Güvenliği Standardı)

Bu uyumluluklar, şirketlerin AWS platformunda çalıştırdıkları uygulamaların yasal gereksinimlerini daha kolay sağlamalarını mümkün kılar.

| Güvenlik Aracı | Kullanım Alanı | Kim Sağlar? |
|---------------|----------------|------------|
| AWS IAM | Kimlik ve erişim yönetimi | Kullanıcı |
| AWS KMS | Şifreleme anahtarlarının yönetimi | Kullanıcı |
| AWS CloudTrail | Kaynak kullanımını izleme (Audit log) | Kullanıcı |
| AWS CloudWatch | İzleme ve alarmlar | Kullanıcı |
| AWS Shield | DDoS saldırılarına karşı koruma | AWS |
| AWS WAF | Web uygulama firewall | Kullanıcı |
| AWS Inspector | Güvenlik açığı taraması | Kullanıcı |

### AWS Güvenlik için En İyi Uygulamalar

- En az ayrıcalık prensibini uygulayın (Least Privilege).
- IAM kullanıcıları yerine IAM Rollerini kullanın.
- Multi-Factor Authentication (MFA) kullanın.
- Hassas verilerinizi şifreleyin.
- Kaynaklarınızı düzenli olarak izleyin ve denetleyin (CloudWatch, CloudTrail).
- Güvenlik Gruplarını ve Network ACL'leri doğru yapılandırın.

---

## AWS Kimlik ve Erişim Yönetimi (IAM)

AWS Kimlik ve Erişim Yönetimi (Identity and Access Management - IAM), AWS kaynaklarınıza güvenli erişimi yönetmek için kullanılan temel hizmetlerden biridir. Kullanıcılarınızın veya uygulamalarınızın AWS üzerindeki kaynaklara hangi yetkilerle erişebileceğini belirlemek için kullanılır.

### IAM Nedir ve Neden Önemlidir?

IAM, kullanıcıları, grupları, rolleri ve izinleri yöneterek AWS kaynaklarınızı korumanızı sağlar. IAM ile her kullanıcıya veya uygulamaya, yalnızca gerekli olan minimum yetkiyi vererek güvenliği üst düzeye çıkarabilirsiniz (Least Privilege Principle).

**IAM'ın önemli özellikleri**:

- Kullanıcı (User) oluşturma ve yönetme
- Gruplar (Groups) oluşturup kullanıcıları gruplandırma
- Roller (Roles) ile geçici erişim sağlama
- Politikalar (Policies) ile yetkilendirme
- Çok Faktörlü Kimlik Doğrulama (MFA) desteği

### IAM Temel Kavramları Nelerdir?

- Kullanıcı (User): AWS hesabınıza erişen kişi veya uygulamalardır.
- Grup (Group): Birden fazla kullanıcıyı aynı yetkilerle gruplandırır.
- Rol (Role): Kullanıcıların veya AWS servislerinin geçici yetkiler almasını sağlar.
- Politika (Policy): Kullanıcı, grup veya rollere verilen erişim izinlerini tanımlar.

**IAM Kullanıcıları (Users)**

Kullanıcılar, AWS hesabınıza giriş yapabilen bireylerdir.

- Kullanıcılar için ayrı kullanıcı adı ve şifre belirleyebilirsiniz.
- Kullanıcılar IAM politikaları ile yetkilendirilir.
- MFA ile ek güvenlik sağlanabilir.

_Kullanıcı oluşturma örneği:_

- AWS konsolunda IAM → Users → Add user seçeneğini kullanın.
- Kullanıcı adı ve erişim türünü seçin (Programmatic veya Console).

**IAM Grupları (Groups)**

Gruplar, birden fazla kullanıcıya ortak izinler atamanızı kolaylaştırır.

_Örneğin_:
- "Developers" grubu: EC2, S3 gibi kaynaklara erişim yetkileri.
- "Admins" grubu: Tam yönetim yetkileri.

_Grup oluşturma örneği_:
- IAM → Groups → Create group
- Kullanıcıları gruba ekleyin ve politika atayın.

**IAM Roller (Roles)**

Roller, kullanıcılar veya AWS servisleri için geçici erişim yetkileri sağlar.

_Rollerin kullanım senaryoları_:

- Bir EC2 sunucusunun S3 bucket’a erişmesi için rol atanabilir.
- Farklı AWS hesapları arasında kaynak erişimi için rol kullanılabilir.

_Rol oluşturma örneği (EC2 için)_:
- IAM → Roles → Create Role
- "AWS Service" → "EC2" → Gerekli politikayı seçerek rol oluşturun.
EC2 instance oluştururken bu rolü atayın.

**IAM Politikaları (Policies)**

Politikalar, AWS kaynaklarına erişim izinlerini JSON formatında belirler.

_Politika türleri_:
- AWS Managed Policies: AWS tarafından önceden hazırlanmış politikalar.
- Customer Managed Policies: Kullanıcı tarafından özelleştirilmiş politikalar.
- Inline Policies: Kullanıcı veya rollere doğrudan atanmış politikalar.

_Örnek Politika (S3'e salt okunur erişim)_:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:Get*",
                "s3:List*"
            ],
            "Resource": "*"
        }
    ]
}
```

**Çok Faktörlü Kimlik Doğrulama (MFA)**

MFA, AWS hesaplarına ek güvenlik katmanı sağlar.

- IAM kullanıcıları ve root hesap için MFA etkinleştirilebilir.
- MFA, telefon uygulaması veya donanım cihazı ile sağlanabilir.

**IAM İçin En İyi Güvenlik Uygulamaları**

AWS üzerinde kimlik yönetimini daha güvenli hale getirmek için aşağıdaki yöntemleri uygulayın:

- Her kullanıcı için ayrı IAM kullanıcıları oluşturun.
- Root hesabınızı günlük işlemler için kullanmayın.
- Tüm kullanıcılarınız için MFA etkinleştirin.
- Kullanıcılara yalnızca ihtiyaçları olan minimum yetkileri verin (Least Privilege).
- Düzenli olarak IAM yetkilerini kontrol edip güncelleyin.
- Roller kullanarak uygulamalara geçici yetkiler verin.

---

### AWS Yönetim ve İdare Hizmetleri Nelerdir?

AWS Yönetim ve İdare (Management & Governance) hizmetleri, bulut ortamındaki kaynaklarınızı verimli, güvenli ve maliyet etkin biçimde yönetmenizi sağlar. AWS, bu yönetim süreçlerini kolaylaştırmak için çeşitli araç ve servisler sunmaktadır.

Bu araçlar sayesinde altyapınızı kolayca yönetebilir, otomatikleştirebilir, güvenlik politikalarınızı uygulayabilir ve kaynaklarınızı izleyebilirsiniz.

### 1. Amazon CloudWatch**

CloudWatch, AWS kaynaklarını izlemek, performans metriklerini toplamak ve bu metriklere göre alarmlar oluşturmak için kullanılan bir izleme servisidir.

**CloudWatch Özellikleri**:

- CPU kullanımı, bellek kullanımı gibi metrikleri izler.
- Alarmlar oluşturabilir ve otomatik aksiyonlar alabilirsiniz.
- Logları toplayıp analiz eder.

### 2. AWS CloudTrail

CloudTrail, AWS hesabınızda gerçekleşen tüm API çağrılarını ve aktivitelerini kayıt altına alarak güvenlik ve denetim süreçlerinize yardımcı olur.

**CloudTrail Özellikleri**:

- Kullanıcı aktivitelerini ve kaynak değişikliklerini kaydeder.
- Güvenlik ve uyumluluk denetimlerinde kullanılır.
- Güvenlik olaylarını analiz etmek için kullanılabilir.

### 3. AWS Config

AWS Config, AWS kaynaklarınızın yapılandırmasını sürekli olarak izler ve kaynaklarınızın yapılandırma geçmişini tutar.

**AWS Config Özellikleri**:

- Kaynak yapılandırmalarını izler.
- Kaynaklarda yapılan değişiklikleri bildirir.
- Uyumluluk kurallarınızı otomatik olarak değerlendirir.

### 4. AWS CloudFormation

CloudFormation, AWS kaynaklarınızı şablon dosyaları (JSON veya YAML) kullanarak yönetmenize olanak sağlar. Altyapınızı kod olarak oluşturabilirsiniz (Infrastructure as Code).

**CloudFormation Özellikleri**:

- Altyapıyı otomatik ve tutarlı bir biçimde oluşturur.
- Altyapı güncellemelerini yönetir.
- Kaynak yönetimini basitleştirir ve standartlaştırır.

### 5. AWS Trusted Advisor

Trusted Advisor, AWS kaynaklarınızı en iyi uygulamalara (best practices) göre analiz eder ve öneriler sunar. Böylece maliyetleri azaltabilir, güvenliği artırabilir ve performansı iyileştirebilirsiniz.

**Trusted Advisor Kontrolleri**:

- Maliyet optimizasyonu
- Güvenlik denetimleri
- Performans değerlendirmeleri
- Güvenilirlik (fault tolerance) analizleri

### 6. AWS Systems Manager

Systems Manager, AWS kaynaklarınızı tek bir yerden yönetmenizi sağlayan operasyonel yönetim hizmetidir.

**Systems Manager Özellikleri**:

- EC2 sunucularını uzaktan yönetebilirsiniz.
- Sunucu yapılandırmalarını otomatikleştirebilirsiniz.
- Yazılım güncellemelerini yönetebilirsiniz.
- Operasyonel görevleri otomatikleştirebilirsiniz.

### 7. AWS Organizations

AWS Organizations, birden fazla AWS hesabınızı merkezi olarak yönetmenize olanak sağlar.

**AWS Organizations Özellikleri**:

- Birden fazla hesabı tek bir merkezden yönetim.
- Organizasyon genelinde politikalar uygulama.
- Birleştirilmiş faturalama ve maliyet yönetimi.

### 8. AWS Budgets

AWS Budgets, harcamalarınızı izlemenize ve bütçe sınırlarını belirleyerek maliyetlerinizi kontrol etmenize yardımcı olur.

**AWS Budgets Özellikleri**:

- Bütçe oluşturma ve takip etme.
- Harcama sınırları aşıldığında uyarı alma.
- Maliyet yönetimini proaktif olarak gerçekleştirme.

### AWS Yönetimi İçin En İyi Uygulamalar

AWS yönetim süreçlerinizi daha verimli ve güvenli hale getirmek için aşağıdaki yöntemleri uygulayın:

- Altyapınızı CloudFormation ile kod olarak yönetin.
- Kaynaklarınızın durumunu ve değişikliklerini AWS Config ile sürekli izleyin.
- Güvenlik ve denetim süreçleri için CloudTrail kullanın.
- Performans takibi ve alarm sistemleri için CloudWatch kullanın.
- Organizasyon genelinde kaynak yönetimi ve maliyet kontrolü için AWS Organizations ve Budgets kullanın.
- Güvenlik ve performans optimizasyonları için Trusted Advisor önerilerini uygulayın.

| Hizmet | Kullanım Alanı | Temel Faydası |
|--------|----------------|---------------|
| CloudWatch | İzleme ve Alarm Yönetimi | Performans ve operasyon yönetimi |
| CloudTrail | Kullanıcı aktivitelerini kayıt etme | Güvenlik ve denetim süreçleri |
| AWS Config | Kaynak yapılandırmalarını takip etme | Uyumluluk ve yapılandırma yönetimi |
| CloudFormation | Altyapıyı kod olarak yönetme | Altyapı otomasyonu |
| Trusted Advisor | Best-practices denetimleri | Güvenlik, maliyet ve performans optimizasyonu |
| Systems Manager | Operasyonel görevleri yönetme | Merkezi operasyon yönetimi |
| Organizations | Çoklu hesap yönetimi | Merkezi yönetim ve maliyet kontrolü |
| Budgets | Maliyet yönetimi | Maliyetleri kontrol altında tutma |

---

## Kapanış ve Özet

Bu eğitim dokümanında, Amazon Web Servisleri (AWS) üzerinde temel kavramları, hizmetleri ve kullanım alanlarını detaylı olarak ele aldık. Bulut bilişim platformlarının öncülerinden olan AWS’in sunduğu geniş hizmet yelpazesi sayesinde, şirketler ve bireyler altyapılarını güvenli, ölçeklenebilir, esnek ve maliyet etkin bir şekilde yönetebilirler.

### Eğitim İçeriğinde Neler Öğrendik?

- **Amazon Web Servisleri (AWS) Nedir?**: AWS bulut platformunun genel tanımı ve avantajları.
- **EC2 (Elastic Compute Cloud)**: Sanal sunucu oluşturma ve yönetme, instance türleri ve EC2’nin kullanım alanları.
- **Autoscaler (Otomatik Ölçeklendirme)**: Uygulamalarınızın yük durumuna göre kaynakların otomatik olarak ölçeklendirilmesi.
- **Load Balancer (Yük Dengeleyici)**: Trafik yükünü birden fazla sunucuya dağıtarak yüksek erişilebilirlik ve performans sağlama.
- **Container Lambda**: AWS Lambda fonksiyonlarının Docker konteynerleriyle kullanımı ve avantajları.
- **Depolama Hizmetleri (Storage)**: Amazon S3, EBS, EFS ve Glacier hizmetlerinin tanımları ve kullanım senaryoları.
- **Veritabanı Hizmetleri (Database)**: RDS, Aurora, DynamoDB, ElastiCache ve Redshift veritabanı çözümlerinin özellikleri ve kullanım alanları.
- **Ağ Hizmetleri (Network)**: VPC, subnetler, Security Groups, Route 53 ve CloudFront gibi ağ yönetimi çözümleri.
- **Hizmetlere Erişim Yöntemleri**: AWS Management Console, CLI, SDK ve API’ler üzerinden AWS hizmetlerine erişim sağlama yolları.
- **Güvenlik ve Mevzuat Uyumluluğu**: AWS üzerinde güvenliği sağlama yöntemleri ve mevzuatlara (GDPR, ISO 27001, PCI DSS vb.) uyumluluk çözümleri.
- **Kimlik ve Erişim Yönetimi (IAM)**: AWS kaynaklarına erişimin güvenli şekilde yönetilmesi için IAM kullanımı ve en iyi uygulamalar.
- **Yönetim ve İdare Hizmetleri (Management & Governance)**: CloudWatch, CloudTrail, AWS Config, CloudFormation, Trusted Advisor, Systems Manager, Organizations ve Budgets gibi yönetim araçları.

> Bu dokümanın size AWS yolculuğunuzda rehber olmasını dilerim. Bol Şans! 🚀☁️
