---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502018"
---
# <span data-ttu-id="3e744-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e744-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="3e744-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e744-102">SYNOPSIS</span></span>
<span data-ttu-id="3e744-103">Erstellt eine AutoScale-Konfiguration für das Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="3e744-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e744-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e744-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e744-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e744-105">DESCRIPTION</span></span>
<span data-ttu-id="3e744-106">Das Cmdlet **New-AzureRmApplicationGatewayAutoscaleConfiguration** erstellt die Konfiguration von AutoScale für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3e744-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="3e744-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e744-107">EXAMPLES</span></span>

### <span data-ttu-id="3e744-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e744-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="3e744-109">Der erste Befehl erstellt eine AutoScale-Konfiguration mit minimaler Kapazität 3.</span><span class="sxs-lookup"><span data-stu-id="3e744-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="3e744-110">Mit dem zweiten Befehl wird ein Anwendungsgateway mit der Konfiguration für das AutoSkalieren erstellt.</span><span class="sxs-lookup"><span data-stu-id="3e744-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="3e744-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e744-111">PARAMETERS</span></span>

### <span data-ttu-id="3e744-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e744-112">-DefaultProfile</span></span>
<span data-ttu-id="3e744-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e744-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e744-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="3e744-114">-MinCapacity</span></span>
<span data-ttu-id="3e744-115">Minimale Kapazitätseinheiten, die für Application Gateway immer verfügbar [und aufgeladen] sind.</span><span class="sxs-lookup"><span data-stu-id="3e744-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="3e744-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3e744-116">-Confirm</span></span>
<span data-ttu-id="3e744-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e744-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e744-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e744-118">-WhatIf</span></span>
<span data-ttu-id="3e744-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e744-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e744-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e744-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e744-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e744-121">CommonParameters</span></span>
<span data-ttu-id="3e744-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e744-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e744-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e744-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e744-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e744-124">INPUTS</span></span>

### <span data-ttu-id="3e744-125">Keine</span><span class="sxs-lookup"><span data-stu-id="3e744-125">None</span></span>

## <span data-ttu-id="3e744-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e744-126">OUTPUTS</span></span>

### <span data-ttu-id="3e744-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e744-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="3e744-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e744-128">NOTES</span></span>

## <span data-ttu-id="3e744-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e744-129">RELATED LINKS</span></span>
