---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170496"
---
# <span data-ttu-id="583f6-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="583f6-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="583f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="583f6-102">SYNOPSIS</span></span>
<span data-ttu-id="583f6-103">Rufen Sie den Failoverprozess für den IoT Hub in die geokoppelte Notfallwiederherstellungsregion auf.</span><span class="sxs-lookup"><span data-stu-id="583f6-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="583f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="583f6-104">SYNTAX</span></span>

### <span data-ttu-id="583f6-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="583f6-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="583f6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="583f6-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="583f6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="583f6-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="583f6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="583f6-108">DESCRIPTION</span></span>
<span data-ttu-id="583f6-109">Damit wird der Failover Ihres IoT-Hubs zum sekundären Speicherort ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="583f6-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="583f6-110">Diese Aktion verursacht einen Ausfall von Zeit- und Telemetriedaten für Ihre Lösung.</span><span class="sxs-lookup"><span data-stu-id="583f6-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="583f6-111">Dies ist ein Vorgang mit langer Ausführung, der einige Minuten dauern kann.</span><span class="sxs-lookup"><span data-stu-id="583f6-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="583f6-112">Gehen Sie bei der Verwendung mit Bedacht vor.</span><span class="sxs-lookup"><span data-stu-id="583f6-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="583f6-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="583f6-113">EXAMPLES</span></span>

### <span data-ttu-id="583f6-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="583f6-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="583f6-115">Initiieren des Failoverprozesses von "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="583f6-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="583f6-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="583f6-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="583f6-117">Initiieren des Failoverprozesses von "myiothub" IoT Hub im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="583f6-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="583f6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="583f6-118">PARAMETERS</span></span>

### <span data-ttu-id="583f6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="583f6-119">-AsJob</span></span>
<span data-ttu-id="583f6-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="583f6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="583f6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583f6-121">-DefaultProfile</span></span>
<span data-ttu-id="583f6-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="583f6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="583f6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="583f6-123">-InputObject</span></span>
<span data-ttu-id="583f6-124">Iot Hub Object</span><span class="sxs-lookup"><span data-stu-id="583f6-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="583f6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="583f6-125">-Name</span></span>
<span data-ttu-id="583f6-126">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="583f6-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="583f6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="583f6-127">-PassThru</span></span>
<span data-ttu-id="583f6-128">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="583f6-128">Allows to return the boolean object.</span></span> <span data-ttu-id="583f6-129">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="583f6-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="583f6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="583f6-130">-ResourceGroupName</span></span>
<span data-ttu-id="583f6-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="583f6-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="583f6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="583f6-132">-ResourceId</span></span>
<span data-ttu-id="583f6-133">Iot Hub Resource Id</span><span class="sxs-lookup"><span data-stu-id="583f6-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="583f6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="583f6-134">-Confirm</span></span>
<span data-ttu-id="583f6-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="583f6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="583f6-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="583f6-136">-WhatIf</span></span>
<span data-ttu-id="583f6-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="583f6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="583f6-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="583f6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="583f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583f6-139">CommonParameters</span></span>
<span data-ttu-id="583f6-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="583f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583f6-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="583f6-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583f6-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="583f6-142">INPUTS</span></span>

### <span data-ttu-id="583f6-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="583f6-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="583f6-144">System.String</span><span class="sxs-lookup"><span data-stu-id="583f6-144">System.String</span></span>

## <span data-ttu-id="583f6-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="583f6-145">OUTPUTS</span></span>

### <span data-ttu-id="583f6-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="583f6-146">System.Boolean</span></span>

## <span data-ttu-id="583f6-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="583f6-147">NOTES</span></span>

## <span data-ttu-id="583f6-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="583f6-148">RELATED LINKS</span></span>
