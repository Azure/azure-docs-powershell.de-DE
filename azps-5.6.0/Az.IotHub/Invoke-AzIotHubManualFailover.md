---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: f9372a246e16e719db60f52922a8a416f3de10c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928019"
---
# <span data-ttu-id="12afe-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="12afe-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="12afe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12afe-102">SYNOPSIS</span></span>
<span data-ttu-id="12afe-103">Rufen Sie den Failoverprozess für den IoT Hub für die Region für die geokoppelte Notfallwiederherstellung auf.</span><span class="sxs-lookup"><span data-stu-id="12afe-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="12afe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12afe-104">SYNTAX</span></span>

### <span data-ttu-id="12afe-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="12afe-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12afe-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="12afe-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12afe-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12afe-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12afe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12afe-108">DESCRIPTION</span></span>
<span data-ttu-id="12afe-109">Es löst das Failover Ihres IoT-Hubs zum sekundären Speicherort aus.</span><span class="sxs-lookup"><span data-stu-id="12afe-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="12afe-110">Diese Aktion verursacht Zeit- und Telemetrieverluste für Ihre Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="12afe-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="12afe-111">Dies ist ein langer Vorgang, der einige Minuten dauern kann.</span><span class="sxs-lookup"><span data-stu-id="12afe-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="12afe-112">Gehen Sie bei der Verwendung mit Vorsicht vor.</span><span class="sxs-lookup"><span data-stu-id="12afe-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="12afe-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12afe-113">EXAMPLES</span></span>

### <span data-ttu-id="12afe-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12afe-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="12afe-115">Initiieren des Failoverprozesses von "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="12afe-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="12afe-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="12afe-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="12afe-117">Initiieren des Failoverprozesses von "myiothub" IoT Hub im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="12afe-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="12afe-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12afe-118">PARAMETERS</span></span>

### <span data-ttu-id="12afe-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12afe-119">-AsJob</span></span>
<span data-ttu-id="12afe-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="12afe-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12afe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12afe-121">-DefaultProfile</span></span>
<span data-ttu-id="12afe-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12afe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12afe-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12afe-123">-InputObject</span></span>
<span data-ttu-id="12afe-124">Iot Hub Object</span><span class="sxs-lookup"><span data-stu-id="12afe-124">Iot Hub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12afe-125">-Name</span><span class="sxs-lookup"><span data-stu-id="12afe-125">-Name</span></span>
<span data-ttu-id="12afe-126">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="12afe-126">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12afe-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12afe-127">-PassThru</span></span>
<span data-ttu-id="12afe-128">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="12afe-128">Allows to return the boolean object.</span></span> <span data-ttu-id="12afe-129">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="12afe-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12afe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12afe-130">-ResourceGroupName</span></span>
<span data-ttu-id="12afe-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="12afe-131">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12afe-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12afe-132">-ResourceId</span></span>
<span data-ttu-id="12afe-133">Iot Hub Resource Id</span><span class="sxs-lookup"><span data-stu-id="12afe-133">Iot Hub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12afe-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12afe-134">-Confirm</span></span>
<span data-ttu-id="12afe-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12afe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12afe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12afe-136">-WhatIf</span></span>
<span data-ttu-id="12afe-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12afe-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12afe-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12afe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12afe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12afe-139">CommonParameters</span></span>
<span data-ttu-id="12afe-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12afe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12afe-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12afe-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12afe-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12afe-142">INPUTS</span></span>

### <span data-ttu-id="12afe-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="12afe-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="12afe-144">System.String</span><span class="sxs-lookup"><span data-stu-id="12afe-144">System.String</span></span>

## <span data-ttu-id="12afe-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12afe-145">OUTPUTS</span></span>

### <span data-ttu-id="12afe-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="12afe-146">System.Boolean</span></span>

## <span data-ttu-id="12afe-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="12afe-147">NOTES</span></span>

## <span data-ttu-id="12afe-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="12afe-148">RELATED LINKS</span></span>
