---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 4bed76f6fa80e5f901d5deeba45940d16332fa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660438"
---
# <span data-ttu-id="f38ff-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f38ff-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f38ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f38ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f38ff-103">Entfernt ein Authentifizierungszertifikat von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f38ff-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="f38ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f38ff-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f38ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f38ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f38ff-106">Das Cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** entfernt ein Authentifizierungszertifikat von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f38ff-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="f38ff-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f38ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f38ff-108">Beispiel 1: Entfernen eines Authentifizierungszertifikats von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="f38ff-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="f38ff-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen appGwName ab und speichert das Ergebnis in der $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="f38ff-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="f38ff-110">Der zweite Befehl entfernt das Authentifizierungszertifikat mit dem Namen cert01 aus dem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f38ff-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="f38ff-111">Der dritte Befehl aktualisiert das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f38ff-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="f38ff-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f38ff-112">PARAMETERS</span></span>

### <span data-ttu-id="f38ff-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f38ff-113">-ApplicationGateway</span></span>
<span data-ttu-id="f38ff-114">Gibt den Namen des Anwendungs Gateways an, von dem dieses Cmdlet ein Authentifizierungszertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="f38ff-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="f38ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f38ff-115">-DefaultProfile</span></span>
<span data-ttu-id="f38ff-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f38ff-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f38ff-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f38ff-117">-Name</span></span>
<span data-ttu-id="f38ff-118">Gibt den Namen des Authentifizierungszertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f38ff-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f38ff-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f38ff-119">-Confirm</span></span>
<span data-ttu-id="f38ff-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f38ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f38ff-121">-WhatIf</span></span>
<span data-ttu-id="f38ff-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f38ff-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f38ff-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f38ff-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f38ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f38ff-124">CommonParameters</span></span>
<span data-ttu-id="f38ff-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f38ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f38ff-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f38ff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f38ff-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f38ff-127">INPUTS</span></span>

### <span data-ttu-id="f38ff-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f38ff-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f38ff-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f38ff-129">OUTPUTS</span></span>

### <span data-ttu-id="f38ff-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f38ff-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f38ff-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f38ff-131">NOTES</span></span>
* <span data-ttu-id="f38ff-132">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="f38ff-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f38ff-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f38ff-133">RELATED LINKS</span></span>

[<span data-ttu-id="f38ff-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f38ff-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f38ff-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f38ff-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f38ff-136">Neu – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f38ff-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f38ff-137">Satz-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f38ff-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


