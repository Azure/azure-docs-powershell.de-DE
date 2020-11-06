---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499478"
---
# <span data-ttu-id="a9070-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9070-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a9070-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9070-102">SYNOPSIS</span></span>
<span data-ttu-id="a9070-103">Aktualisiert die Konfiguration von AutoScale eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="a9070-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9070-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9070-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9070-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9070-105">DESCRIPTION</span></span>
<span data-ttu-id="a9070-106">Das Cmdlet " **Satz-AzureRmApplicationGatewayAutoscaleConfiguration** " ändert die vorhandene AutoScale-Konfiguration eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="a9070-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="a9070-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9070-107">EXAMPLES</span></span>

### <span data-ttu-id="a9070-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9070-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="a9070-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $GW Variablen.</span><span class="sxs-lookup"><span data-stu-id="a9070-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a9070-110">Der zweite Befehl aktualisiert die AutoScale-Konfiguration vom applicationg-Gateway.</span><span class="sxs-lookup"><span data-stu-id="a9070-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="a9070-111">Der dritte Befehl aktualisiert das Anwendungsgateway auf Azure.</span><span class="sxs-lookup"><span data-stu-id="a9070-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="a9070-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9070-112">PARAMETERS</span></span>

### <span data-ttu-id="a9070-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9070-113">-ApplicationGateway</span></span>
<span data-ttu-id="a9070-114">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9070-114">The applicationGateway</span></span>

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

### <span data-ttu-id="a9070-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9070-115">-DefaultProfile</span></span>
<span data-ttu-id="a9070-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9070-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9070-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="a9070-117">-MinCapacity</span></span>
<span data-ttu-id="a9070-118">Minimale capcity für Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a9070-118">Minimum capcity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9070-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9070-119">-Confirm</span></span>
<span data-ttu-id="a9070-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9070-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9070-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9070-121">-WhatIf</span></span>
<span data-ttu-id="a9070-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9070-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9070-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9070-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9070-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9070-124">CommonParameters</span></span>
<span data-ttu-id="a9070-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9070-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9070-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9070-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9070-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9070-127">INPUTS</span></span>

### <span data-ttu-id="a9070-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9070-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a9070-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9070-129">OUTPUTS</span></span>

### <span data-ttu-id="a9070-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9070-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a9070-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9070-131">NOTES</span></span>

## <span data-ttu-id="a9070-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9070-132">RELATED LINKS</span></span>
