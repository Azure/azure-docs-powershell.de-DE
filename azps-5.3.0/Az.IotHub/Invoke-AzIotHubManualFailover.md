---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472478"
---
# <span data-ttu-id="9bf3b-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="9bf3b-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="9bf3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bf3b-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf3b-103">Rufen Sie den Failoverprozess für den IoT Hub in die geokoppelte Notfallwiederherstellungsregion auf.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="9bf3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bf3b-104">SYNTAX</span></span>

### <span data-ttu-id="9bf3b-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9bf3b-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf3b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9bf3b-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf3b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9bf3b-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bf3b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bf3b-108">DESCRIPTION</span></span>
<span data-ttu-id="9bf3b-109">Damit wird der Failover Ihres IoT-Hubs zum sekundären Speicherort ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="9bf3b-110">Diese Aktion verursacht einen Zeit- und Telemetrieverlust für Ihre Lösung.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="9bf3b-111">Dies ist ein Vorgang mit langer Ausführung, der einige Minuten dauern kann.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="9bf3b-112">Gehen Sie bei der Verwendung mit Bedacht vor.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="9bf3b-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9bf3b-113">EXAMPLES</span></span>

### <span data-ttu-id="9bf3b-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9bf3b-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9bf3b-115">Initiieren des Failoverprozesses von "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="9bf3b-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9bf3b-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="9bf3b-117">Initiieren des Failoverprozesses von "myiothub" IoT Hub im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="9bf3b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bf3b-118">PARAMETERS</span></span>

### <span data-ttu-id="9bf3b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bf3b-119">-AsJob</span></span>
<span data-ttu-id="9bf3b-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9bf3b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bf3b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf3b-121">-DefaultProfile</span></span>
<span data-ttu-id="9bf3b-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf3b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bf3b-123">-InputObject</span></span>
<span data-ttu-id="9bf3b-124">Iot Hub Object</span><span class="sxs-lookup"><span data-stu-id="9bf3b-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="9bf3b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9bf3b-125">-Name</span></span>
<span data-ttu-id="9bf3b-126">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="9bf3b-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9bf3b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bf3b-127">-PassThru</span></span>
<span data-ttu-id="9bf3b-128">Ermöglicht die Rückgabe des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-128">Allows to return the boolean object.</span></span> <span data-ttu-id="9bf3b-129">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9bf3b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf3b-130">-ResourceGroupName</span></span>
<span data-ttu-id="9bf3b-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9bf3b-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9bf3b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf3b-132">-ResourceId</span></span>
<span data-ttu-id="9bf3b-133">Iot Hub Resource Id</span><span class="sxs-lookup"><span data-stu-id="9bf3b-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="9bf3b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bf3b-134">-Confirm</span></span>
<span data-ttu-id="9bf3b-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf3b-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9bf3b-136">-WhatIf</span></span>
<span data-ttu-id="9bf3b-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9bf3b-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf3b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf3b-139">CommonParameters</span></span>
<span data-ttu-id="9bf3b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf3b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf3b-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf3b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf3b-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9bf3b-142">INPUTS</span></span>

### <span data-ttu-id="9bf3b-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9bf3b-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9bf3b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9bf3b-144">System.String</span></span>

## <span data-ttu-id="9bf3b-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9bf3b-145">OUTPUTS</span></span>

### <span data-ttu-id="9bf3b-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9bf3b-146">System.Boolean</span></span>

## <span data-ttu-id="9bf3b-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9bf3b-147">NOTES</span></span>

## <span data-ttu-id="9bf3b-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9bf3b-148">RELATED LINKS</span></span>
