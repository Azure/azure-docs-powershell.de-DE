---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 383ad627ff7a633d508daccde70e3de395e4ad57
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848743"
---
# <span data-ttu-id="39a0a-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="39a0a-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="39a0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="39a0a-103">Entfernt eine SSL-Richtlinie aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="39a0a-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39a0a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39a0a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39a0a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39a0a-105">DESCRIPTION</span></span>
<span data-ttu-id="39a0a-106">Das Remove-AzureRmApplicationGatewaySslPolicy-Cmdlet entfernt die SSL-Richtlinie aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="39a0a-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="39a0a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39a0a-107">EXAMPLES</span></span>

### <span data-ttu-id="39a0a-108">Beispiel 1: Entfernen einer SSL-Richtlinie von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="39a0a-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="39a0a-109">Dieser Befehl entfernt die SSL-Richtlinie aus dem Anwendungsgateway mit dem Namen ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="39a0a-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="39a0a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="39a0a-110">PARAMETERS</span></span>

### <span data-ttu-id="39a0a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39a0a-111">-ApplicationGateway</span></span>
<span data-ttu-id="39a0a-112">Gibt das Anwendungsgateway an, von dem dieses Cmdlet die SSL-Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="39a0a-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="39a0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a0a-113">-DefaultProfile</span></span>
<span data-ttu-id="39a0a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39a0a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39a0a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="39a0a-115">-Force</span></span>
<span data-ttu-id="39a0a-116">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="39a0a-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="39a0a-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39a0a-117">-Confirm</span></span>
<span data-ttu-id="39a0a-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39a0a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39a0a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39a0a-119">-WhatIf</span></span>
<span data-ttu-id="39a0a-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39a0a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39a0a-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39a0a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39a0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a0a-122">CommonParameters</span></span>
<span data-ttu-id="39a0a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a0a-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39a0a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a0a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39a0a-125">INPUTS</span></span>

### <span data-ttu-id="39a0a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="39a0a-126">System.String</span></span>

## <span data-ttu-id="39a0a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39a0a-127">OUTPUTS</span></span>

### <span data-ttu-id="39a0a-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39a0a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="39a0a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="39a0a-129">NOTES</span></span>
<span data-ttu-id="39a0a-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="39a0a-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="39a0a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39a0a-131">RELATED LINKS</span></span>

[<span data-ttu-id="39a0a-132">Satz-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="39a0a-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="39a0a-133">Neu – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="39a0a-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="39a0a-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="39a0a-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

