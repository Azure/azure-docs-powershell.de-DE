---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006700"
---
# <span data-ttu-id="53eb7-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53eb7-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="53eb7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="53eb7-103">Entfernt ein SSL-Zertifikat von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="53eb7-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="53eb7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53eb7-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="53eb7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="53eb7-106">Das Cmdlet **Remove-AzureApplicationGatewaySslCertificate** entfernt ein SSL-Zertifikat (Secure Sockets Layer) von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="53eb7-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="53eb7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53eb7-107">EXAMPLES</span></span>

### <span data-ttu-id="53eb7-108">Beispiel 1: Entfernen eines SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="53eb7-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="53eb7-109">Dieser Befehl entfernt ein SSL-Zertifikat mit dem Namen SslCertificate13 aus dem Anwendungsgateway namens ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="53eb7-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="53eb7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53eb7-110">PARAMETERS</span></span>

### <span data-ttu-id="53eb7-111">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="53eb7-111">-CertificateName</span></span>
<span data-ttu-id="53eb7-112">Gibt den Namen eines SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="53eb7-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="53eb7-113">Dieses Cmdlet entfernt das Zertifikat, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="53eb7-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="53eb7-114">-Name</span><span class="sxs-lookup"><span data-stu-id="53eb7-114">-Name</span></span>
<span data-ttu-id="53eb7-115">Gibt den Namen des Anwendungs Gateways an, von dem dieses Cmdlet ein SSL-Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="53eb7-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="53eb7-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="53eb7-116">-Profile</span></span>
<span data-ttu-id="53eb7-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="53eb7-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53eb7-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="53eb7-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53eb7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53eb7-119">CommonParameters</span></span>
<span data-ttu-id="53eb7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53eb7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53eb7-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53eb7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53eb7-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53eb7-122">INPUTS</span></span>

### <span data-ttu-id="53eb7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="53eb7-123">System.String</span></span>

## <span data-ttu-id="53eb7-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53eb7-124">OUTPUTS</span></span>

### <span data-ttu-id="53eb7-125">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="53eb7-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="53eb7-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="53eb7-126">NOTES</span></span>

## <span data-ttu-id="53eb7-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53eb7-127">RELATED LINKS</span></span>

[<span data-ttu-id="53eb7-128">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53eb7-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="53eb7-129">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53eb7-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
