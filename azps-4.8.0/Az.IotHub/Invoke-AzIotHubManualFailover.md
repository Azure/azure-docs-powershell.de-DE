---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167435"
---
# <span data-ttu-id="b4e2d-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="b4e2d-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="b4e2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e2d-103">Rufen Sie den Failoverprozess für den viel-Hub für den Geo-gekoppelten Disaster Recovery-Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="b4e2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4e2d-104">SYNTAX</span></span>

### <span data-ttu-id="b4e2d-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4e2d-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e2d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4e2d-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e2d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b4e2d-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e2d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4e2d-108">DESCRIPTION</span></span>
<span data-ttu-id="b4e2d-109">Dadurch wird das Failover Ihres viel-Hubs zum sekundären Standort ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="b4e2d-110">Diese Aktion führt zu Ausfallzeiten und Telemetrie-Verlust für Ihre Lösung.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="b4e2d-111">Hierbei handelt es sich um einen lang andauernden Vorgang, der einige Minuten dauern kann.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="b4e2d-112">Bitte üben Sie mit Vorsicht, wenn Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="b4e2d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4e2d-113">EXAMPLES</span></span>

### <span data-ttu-id="b4e2d-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4e2d-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b4e2d-115">Initiieren des Failover-Vorgangs des "myiothub"-Hubs</span><span class="sxs-lookup"><span data-stu-id="b4e2d-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="b4e2d-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b4e2d-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="b4e2d-117">Initiieren des Failover-Vorgangs des "myiothub"-Hubs im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b4e2d-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="b4e2d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4e2d-118">PARAMETERS</span></span>

### <span data-ttu-id="b4e2d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4e2d-119">-AsJob</span></span>
<span data-ttu-id="b4e2d-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b4e2d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4e2d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e2d-121">-DefaultProfile</span></span>
<span data-ttu-id="b4e2d-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4e2d-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4e2d-123">-InputObject</span></span>
<span data-ttu-id="b4e2d-124">Viel Hub-Objekt</span><span class="sxs-lookup"><span data-stu-id="b4e2d-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="b4e2d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b4e2d-125">-Name</span></span>
<span data-ttu-id="b4e2d-126">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="b4e2d-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b4e2d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4e2d-127">-PassThru</span></span>
<span data-ttu-id="b4e2d-128">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-128">Allows to return the boolean object.</span></span> <span data-ttu-id="b4e2d-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4e2d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e2d-130">-ResourceGroupName</span></span>
<span data-ttu-id="b4e2d-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b4e2d-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b4e2d-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b4e2d-132">-ResourceId</span></span>
<span data-ttu-id="b4e2d-133">Viel Hub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b4e2d-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="b4e2d-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4e2d-134">-Confirm</span></span>
<span data-ttu-id="b4e2d-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4e2d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e2d-136">-WhatIf</span></span>
<span data-ttu-id="b4e2d-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4e2d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4e2d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e2d-139">CommonParameters</span></span>
<span data-ttu-id="b4e2d-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e2d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e2d-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e2d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e2d-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4e2d-142">INPUTS</span></span>

### <span data-ttu-id="b4e2d-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b4e2d-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b4e2d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b4e2d-144">System.String</span></span>

## <span data-ttu-id="b4e2d-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4e2d-145">OUTPUTS</span></span>

### <span data-ttu-id="b4e2d-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4e2d-146">System.Boolean</span></span>

## <span data-ttu-id="b4e2d-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4e2d-147">NOTES</span></span>

## <span data-ttu-id="b4e2d-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4e2d-148">RELATED LINKS</span></span>
