---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 455ee170ffba9f601cd8e3034e0c774966f92eba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841187"
---
# <span data-ttu-id="79bd3-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="79bd3-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="79bd3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="79bd3-103">Entfernt eine SSL-Richtlinie aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="79bd3-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="79bd3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79bd3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79bd3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79bd3-105">DESCRIPTION</span></span>
<span data-ttu-id="79bd3-106">Das Remove-AzApplicationGatewaySslPolicy-Cmdlet entfernt die SSL-Richtlinie aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="79bd3-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="79bd3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79bd3-107">EXAMPLES</span></span>

### <span data-ttu-id="79bd3-108">Beispiel 1: Entfernen einer SSL-Richtlinie von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="79bd3-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="79bd3-109">Dieser Befehl entfernt die SSL-Richtlinie aus dem Anwendungsgateway mit dem Namen ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="79bd3-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="79bd3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="79bd3-110">PARAMETERS</span></span>

### <span data-ttu-id="79bd3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79bd3-111">-ApplicationGateway</span></span>
<span data-ttu-id="79bd3-112">Gibt das Anwendungsgateway an, von dem dieses Cmdlet die SSL-Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="79bd3-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79bd3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bd3-113">-DefaultProfile</span></span>
<span data-ttu-id="79bd3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79bd3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bd3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="79bd3-115">-Force</span></span>
<span data-ttu-id="79bd3-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="79bd3-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bd3-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79bd3-117">-Confirm</span></span>
<span data-ttu-id="79bd3-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79bd3-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bd3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79bd3-119">-WhatIf</span></span>
<span data-ttu-id="79bd3-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79bd3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79bd3-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79bd3-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bd3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bd3-122">CommonParameters</span></span>
<span data-ttu-id="79bd3-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79bd3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bd3-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79bd3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bd3-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79bd3-125">INPUTS</span></span>

### <span data-ttu-id="79bd3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="79bd3-126">System.String</span></span>

## <span data-ttu-id="79bd3-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79bd3-127">OUTPUTS</span></span>

### <span data-ttu-id="79bd3-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79bd3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79bd3-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="79bd3-129">NOTES</span></span>
<span data-ttu-id="79bd3-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="79bd3-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="79bd3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79bd3-131">RELATED LINKS</span></span>

[<span data-ttu-id="79bd3-132">Satz-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="79bd3-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="79bd3-133">Neu – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="79bd3-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="79bd3-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="79bd3-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

