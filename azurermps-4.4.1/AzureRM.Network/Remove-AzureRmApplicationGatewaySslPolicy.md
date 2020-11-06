---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 81928913565c6e95f3768ccd5c05e8baa2c14b74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505606"
---
# <span data-ttu-id="c4470-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c4470-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c4470-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4470-102">SYNOPSIS</span></span>
<span data-ttu-id="c4470-103">Entfernt eine SSL-Richtlinie aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c4470-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4470-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4470-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4470-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4470-105">DESCRIPTION</span></span>
<span data-ttu-id="c4470-106">Das Remove-AzureRmApplicationGatewaySslPolicy-Cmdlet entfernt die SSL-Richtlinie aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c4470-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="c4470-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4470-107">EXAMPLES</span></span>

### <span data-ttu-id="c4470-108">Beispiel 1: Entfernen einer SSL-Richtlinie von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="c4470-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="c4470-109">Dieser Befehl entfernt die SSL-Richtlinie aus dem Anwendungsgateway mit dem Namen ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="c4470-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="c4470-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4470-110">PARAMETERS</span></span>

### <span data-ttu-id="c4470-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4470-111">-ApplicationGateway</span></span>
<span data-ttu-id="c4470-112">Gibt das Anwendungsgateway an, von dem dieses Cmdlet die SSL-Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="c4470-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="c4470-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c4470-113">-Force</span></span>
<span data-ttu-id="c4470-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c4470-114">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4470-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4470-115">-Confirm</span></span>
<span data-ttu-id="c4470-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4470-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4470-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4470-117">-WhatIf</span></span>
<span data-ttu-id="c4470-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4470-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4470-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4470-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4470-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4470-120">-DefaultProfile</span></span>
<span data-ttu-id="c4470-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4470-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4470-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4470-122">CommonParameters</span></span>
<span data-ttu-id="c4470-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4470-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4470-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4470-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4470-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4470-125">INPUTS</span></span>

### <span data-ttu-id="c4470-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c4470-126">System.String</span></span>

## <span data-ttu-id="c4470-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4470-127">OUTPUTS</span></span>

### <span data-ttu-id="c4470-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4470-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c4470-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4470-129">NOTES</span></span>
<span data-ttu-id="c4470-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="c4470-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c4470-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4470-131">RELATED LINKS</span></span>

[<span data-ttu-id="c4470-132">Satz-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c4470-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="c4470-133">Neu – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c4470-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="c4470-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c4470-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

