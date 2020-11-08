---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 3e7010309c6aed367e3771971a8b1c2841548fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167194"
---
# <span data-ttu-id="78846-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="78846-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="78846-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78846-102">SYNOPSIS</span></span>
<span data-ttu-id="78846-103">Ruft ein SSL-Zertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="78846-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="78846-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78846-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78846-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78846-105">DESCRIPTION</span></span>
<span data-ttu-id="78846-106">Das Cmdlet " **Get-AzApplicationGatewaySslCertificate** " Ruft ein SSL-Zertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="78846-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="78846-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78846-107">EXAMPLES</span></span>

### <span data-ttu-id="78846-108">Beispiel 1: Abrufen eines bestimmten SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="78846-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="78846-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="78846-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="78846-110">Der zweite Befehl ruft das SSL-Zertifikat mit dem Namen Cert01 aus dem Anwendungsgateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="78846-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="78846-111">Der Befehl speichert das Zertifikat in der Variablen mit dem Namen $cert.</span><span class="sxs-lookup"><span data-stu-id="78846-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="78846-112">Beispiel 2: Abrufen einer Liste mit SSL-Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="78846-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="78846-113">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="78846-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="78846-114">Dieser zweite Befehl ruft eine Liste mit SSL-Zertifikaten aus dem Anwendungsgateway ab, die in der Variablen mit dem Namen $AppGW gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="78846-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="78846-115">Der Befehl speichert die Ergebnisse dann in der Variablen mit dem Namen $certs.</span><span class="sxs-lookup"><span data-stu-id="78846-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="78846-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="78846-116">PARAMETERS</span></span>

### <span data-ttu-id="78846-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78846-117">-ApplicationGateway</span></span>
<span data-ttu-id="78846-118">Gibt das Application Gateway-Objekt an, das das SSL-Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="78846-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="78846-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78846-119">-DefaultProfile</span></span>
<span data-ttu-id="78846-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78846-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78846-121">-Name</span><span class="sxs-lookup"><span data-stu-id="78846-121">-Name</span></span>
<span data-ttu-id="78846-122">Gibt den Namen des SSL-Zertifikat Pools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="78846-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78846-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78846-123">CommonParameters</span></span>
<span data-ttu-id="78846-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78846-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78846-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78846-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78846-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78846-126">INPUTS</span></span>

### <span data-ttu-id="78846-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78846-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="78846-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78846-128">OUTPUTS</span></span>

### <span data-ttu-id="78846-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="78846-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="78846-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="78846-130">NOTES</span></span>

## <span data-ttu-id="78846-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78846-131">RELATED LINKS</span></span>

[<span data-ttu-id="78846-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="78846-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="78846-133">Neu – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="78846-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="78846-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="78846-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="78846-135">Satz-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="78846-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


