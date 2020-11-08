---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175086"
---
# <span data-ttu-id="ece57-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ece57-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ece57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ece57-102">SYNOPSIS</span></span>
<span data-ttu-id="ece57-103">Erstellt eine AutoScale-Konfiguration für das Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="ece57-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="ece57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ece57-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece57-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ece57-105">DESCRIPTION</span></span>
<span data-ttu-id="ece57-106">Das Cmdlet **New-AzApplicationGatewayAutoscaleConfiguration** erstellt die Konfiguration von AutoScale für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ece57-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="ece57-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ece57-107">EXAMPLES</span></span>

### <span data-ttu-id="ece57-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ece57-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="ece57-109">Der erste Befehl erstellt eine AutoScale-Konfiguration mit minimaler Kapazität 3.</span><span class="sxs-lookup"><span data-stu-id="ece57-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="ece57-110">Mit dem zweiten Befehl wird ein Anwendungsgateway mit der Konfiguration für das AutoSkalieren erstellt.</span><span class="sxs-lookup"><span data-stu-id="ece57-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="ece57-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ece57-111">PARAMETERS</span></span>

### <span data-ttu-id="ece57-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece57-112">-DefaultProfile</span></span>
<span data-ttu-id="ece57-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ece57-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece57-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="ece57-114">-MaxCapacity</span></span>
<span data-ttu-id="ece57-115">Maximale Kapazitätseinheiten, die für Application Gateway immer verfügbar [und aufgeladen] sind.</span><span class="sxs-lookup"><span data-stu-id="ece57-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece57-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="ece57-116">-MinCapacity</span></span>
<span data-ttu-id="ece57-117">Minimale Kapazitätseinheiten, die für Application Gateway immer verfügbar [und aufgeladen] sind.</span><span class="sxs-lookup"><span data-stu-id="ece57-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="ece57-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ece57-118">-Confirm</span></span>
<span data-ttu-id="ece57-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ece57-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece57-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece57-120">-WhatIf</span></span>
<span data-ttu-id="ece57-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ece57-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece57-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ece57-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece57-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece57-123">CommonParameters</span></span>
<span data-ttu-id="ece57-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece57-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece57-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece57-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece57-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ece57-126">INPUTS</span></span>

### <span data-ttu-id="ece57-127">Keine</span><span class="sxs-lookup"><span data-stu-id="ece57-127">None</span></span>

## <span data-ttu-id="ece57-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ece57-128">OUTPUTS</span></span>

### <span data-ttu-id="ece57-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ece57-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ece57-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ece57-130">NOTES</span></span>

## <span data-ttu-id="ece57-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ece57-131">RELATED LINKS</span></span>

[<span data-ttu-id="ece57-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ece57-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ece57-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ece57-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ece57-134">Satz-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ece57-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
