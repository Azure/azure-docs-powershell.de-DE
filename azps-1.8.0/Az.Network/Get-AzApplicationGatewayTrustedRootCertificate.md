---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 1e617ef1283937116bd97c24a968f247fa7552de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660830"
---
# <span data-ttu-id="8e66c-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e66c-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="8e66c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e66c-102">SYNOPSIS</span></span>
<span data-ttu-id="8e66c-103">Ruft das vertrauenswürdige Stammzertifikat mit einem bestimmten Namen aus dem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="8e66c-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="8e66c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e66c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e66c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e66c-105">DESCRIPTION</span></span>
<span data-ttu-id="8e66c-106">Das Cmdlet " **Get-AzApplicationGatewayTrustedRootCertificate** " Ruft ein vertrauenswürdiges Stammzertifikat mit einem bestimmten Namen vom Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="8e66c-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="8e66c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e66c-107">EXAMPLES</span></span>

### <span data-ttu-id="8e66c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e66c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="8e66c-109">Der erste Befehl ruft das Anwendungs Gateway ab und speichert es in $GW Variablen.</span><span class="sxs-lookup"><span data-stu-id="8e66c-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="8e66c-110">Der zweite Befehl ruft das vertrauenswürdige Stammzertifikat mit einem angegebenen Namen aus dem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="8e66c-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="8e66c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e66c-111">PARAMETERS</span></span>

### <span data-ttu-id="8e66c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e66c-112">-ApplicationGateway</span></span>
<span data-ttu-id="8e66c-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e66c-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8e66c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e66c-114">-DefaultProfile</span></span>
<span data-ttu-id="8e66c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e66c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e66c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8e66c-116">-Name</span></span>
<span data-ttu-id="8e66c-117">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="8e66c-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="8e66c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e66c-118">CommonParameters</span></span>
<span data-ttu-id="8e66c-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e66c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e66c-120">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e66c-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e66c-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e66c-121">INPUTS</span></span>

### <span data-ttu-id="8e66c-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e66c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e66c-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e66c-123">OUTPUTS</span></span>

### <span data-ttu-id="8e66c-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e66c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="8e66c-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e66c-125">NOTES</span></span>

## <span data-ttu-id="8e66c-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e66c-126">RELATED LINKS</span></span>

[<span data-ttu-id="8e66c-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e66c-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8e66c-128">Neu – AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e66c-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8e66c-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e66c-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="8e66c-130">Satz-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8e66c-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
