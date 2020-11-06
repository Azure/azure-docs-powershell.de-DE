---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: da831810461e763acc51319ea4d6662c45a1c3ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495557"
---
# <span data-ttu-id="bdbbf-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bdbbf-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="bdbbf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdbbf-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbbf-103">Ruft ein SSL-Zertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdbbf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdbbf-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdbbf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdbbf-105">DESCRIPTION</span></span>
<span data-ttu-id="bdbbf-106">Das Cmdlet " **Get-AzureRmApplicationGatewaySslCertificate** " Ruft ein SSL-Zertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="bdbbf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdbbf-107">EXAMPLES</span></span>

### <span data-ttu-id="bdbbf-108">Beispiel 1: Abrufen eines bestimmten SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="bdbbf-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="bdbbf-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bdbbf-110">Der zweite Befehl ruft das SSL-Zertifikat mit dem Namen Cert01 aus dem Anwendungsgateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="bdbbf-111">Der Befehl speichert das Zertifikat in der Variablen mit dem Namen $cert.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="bdbbf-112">Beispiel 2: Abrufen einer Liste mit SSL-Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="bdbbf-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="bdbbf-113">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bdbbf-114">Dieser zweite Befehl ruft eine Liste mit SSL-Zertifikaten aus dem Anwendungsgateway ab, die in der Variablen mit dem Namen $AppGW gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="bdbbf-115">Der Befehl speichert die Ergebnisse dann in der Variablen mit dem Namen $certs.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="bdbbf-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdbbf-116">PARAMETERS</span></span>

### <span data-ttu-id="bdbbf-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdbbf-117">-ApplicationGateway</span></span>
<span data-ttu-id="bdbbf-118">Gibt das Application Gateway-Objekt an, das das SSL-Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdbbf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bdbbf-119">-Name</span></span>
<span data-ttu-id="bdbbf-120">Gibt den Namen des SSL-Zertifikat Pools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-120">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbbf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbbf-121">-DefaultProfile</span></span>
<span data-ttu-id="bdbbf-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbbf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbbf-123">CommonParameters</span></span>
<span data-ttu-id="bdbbf-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdbbf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbbf-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdbbf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbbf-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdbbf-126">INPUTS</span></span>

### <span data-ttu-id="bdbbf-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bdbbf-127">System.String</span></span>

## <span data-ttu-id="bdbbf-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdbbf-128">OUTPUTS</span></span>

### <span data-ttu-id="bdbbf-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bdbbf-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="bdbbf-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdbbf-130">NOTES</span></span>

## <span data-ttu-id="bdbbf-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdbbf-131">RELATED LINKS</span></span>

[<span data-ttu-id="bdbbf-132">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bdbbf-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="bdbbf-133">Neu – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bdbbf-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="bdbbf-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bdbbf-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="bdbbf-135">Satz-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bdbbf-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


