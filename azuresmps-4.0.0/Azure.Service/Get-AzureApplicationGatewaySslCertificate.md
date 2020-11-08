---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005870"
---
# <span data-ttu-id="89c00-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="89c00-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="89c00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89c00-102">SYNOPSIS</span></span>
<span data-ttu-id="89c00-103">Ruft Application Gateway-Zertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="89c00-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="89c00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89c00-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="89c00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89c00-105">DESCRIPTION</span></span>
<span data-ttu-id="89c00-106">Das Cmdlet " **Get-AzureApplicationGatewaySslCertificate** " ruft SSL-Zertifikate (Secure Sockets Layer) für ein Azure Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="89c00-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="89c00-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89c00-107">EXAMPLES</span></span>

### <span data-ttu-id="89c00-108">Beispiel 1: Abrufen eines SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="89c00-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="89c00-109">Dieser Befehl ruft ein SSL-Zertifikat mit dem Namen SslCertificate13 auf dem Anwendungs Gateway mit dem Namen ApplicationGateway08 ab.</span><span class="sxs-lookup"><span data-stu-id="89c00-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="89c00-110">Beispiel 2: Abrufen aller SSL-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="89c00-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="89c00-111">Dieser Befehl ruft alle SSL-Zertifikate auf dem Application Gateway mit dem Namen ApplicationGateway08 ab.</span><span class="sxs-lookup"><span data-stu-id="89c00-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="89c00-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="89c00-112">PARAMETERS</span></span>

### <span data-ttu-id="89c00-113">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="89c00-113">-CertificateName</span></span>
<span data-ttu-id="89c00-114">Gibt den Namen eines SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="89c00-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="89c00-115">Dieses Cmdlet ruft das Zertifikat ab, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="89c00-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89c00-116">-Name</span><span class="sxs-lookup"><span data-stu-id="89c00-116">-Name</span></span>
<span data-ttu-id="89c00-117">Gibt den Namen des Anwendungs Gateways an, von dem dieses Cmdlet ein SSL-Zertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="89c00-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89c00-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="89c00-118">-Profile</span></span>
<span data-ttu-id="89c00-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="89c00-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89c00-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="89c00-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c00-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c00-121">CommonParameters</span></span>
<span data-ttu-id="89c00-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89c00-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c00-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c00-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c00-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89c00-124">INPUTS</span></span>

### <span data-ttu-id="89c00-125">System. String</span><span class="sxs-lookup"><span data-stu-id="89c00-125">System.String</span></span>

## <span data-ttu-id="89c00-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89c00-126">OUTPUTS</span></span>

### <span data-ttu-id="89c00-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, List<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate></span><span class="sxs-lookup"><span data-stu-id="89c00-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="89c00-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="89c00-128">NOTES</span></span>

## <span data-ttu-id="89c00-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89c00-129">RELATED LINKS</span></span>

[<span data-ttu-id="89c00-130">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="89c00-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="89c00-131">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="89c00-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
