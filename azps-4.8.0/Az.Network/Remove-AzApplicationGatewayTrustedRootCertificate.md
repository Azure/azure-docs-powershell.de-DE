---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175001"
---
# <span data-ttu-id="139dc-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="139dc-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="139dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="139dc-102">SYNOPSIS</span></span>
<span data-ttu-id="139dc-103">Entfernt ein vertrauenswürdiges Stammzertifikat von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="139dc-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="139dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="139dc-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="139dc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="139dc-105">DESCRIPTION</span></span>
<span data-ttu-id="139dc-106">Das Cmdlet **Remove-AzApplicationGatewayTrustedRootCertificate** entfernt ein vertrauenswürdiges Stammzertifikat aus einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="139dc-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="139dc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="139dc-107">EXAMPLES</span></span>

### <span data-ttu-id="139dc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="139dc-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="139dc-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $GW-Variablen.</span><span class="sxs-lookup"><span data-stu-id="139dc-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="139dc-110">Mit dem zweiten Befehl wird das vertrauenswürdige Stammzertifikat mit dem Namen myRootCA aus dem Anwendungsgateway entfernt, das in $GW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="139dc-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="139dc-111">Der dritte Befehl aktualisiert das Anwendungsgateway auf Azure.</span><span class="sxs-lookup"><span data-stu-id="139dc-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="139dc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="139dc-112">PARAMETERS</span></span>

### <span data-ttu-id="139dc-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="139dc-113">-ApplicationGateway</span></span>
<span data-ttu-id="139dc-114">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="139dc-114">The applicationGateway</span></span>

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

### <span data-ttu-id="139dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139dc-115">-DefaultProfile</span></span>
<span data-ttu-id="139dc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="139dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="139dc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="139dc-117">-Name</span></span>
<span data-ttu-id="139dc-118">Der Name des TrustedRoot-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="139dc-118">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139dc-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="139dc-119">-Confirm</span></span>
<span data-ttu-id="139dc-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="139dc-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139dc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="139dc-121">-WhatIf</span></span>
<span data-ttu-id="139dc-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="139dc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="139dc-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="139dc-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139dc-124">CommonParameters</span></span>
<span data-ttu-id="139dc-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="139dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139dc-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="139dc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139dc-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="139dc-127">INPUTS</span></span>

### <span data-ttu-id="139dc-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="139dc-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="139dc-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="139dc-129">OUTPUTS</span></span>

### <span data-ttu-id="139dc-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="139dc-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="139dc-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="139dc-131">NOTES</span></span>

## <span data-ttu-id="139dc-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="139dc-132">RELATED LINKS</span></span>

[<span data-ttu-id="139dc-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="139dc-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="139dc-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="139dc-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="139dc-135">Neu – AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="139dc-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="139dc-136">Satz-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="139dc-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
