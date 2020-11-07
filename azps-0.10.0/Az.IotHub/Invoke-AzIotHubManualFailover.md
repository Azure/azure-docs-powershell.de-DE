---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: 5055960ae541ef93d57eee53078413143fad7839
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843955"
---
# <span data-ttu-id="50b79-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="50b79-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="50b79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50b79-102">SYNOPSIS</span></span>
<span data-ttu-id="50b79-103">Rufen Sie den Failoverprozess für den viel-Hub für den Geo-gekoppelten Disaster Recovery-Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="50b79-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="50b79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50b79-104">SYNTAX</span></span>

### <span data-ttu-id="50b79-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="50b79-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50b79-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="50b79-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50b79-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="50b79-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50b79-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50b79-108">DESCRIPTION</span></span>
<span data-ttu-id="50b79-109">Dadurch wird das Failover Ihres viel-Hubs zum sekundären Standort ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="50b79-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="50b79-110">Diese Aktion führt zu Ausfallzeiten und Telemetrie-Verlust für Ihre Lösung.</span><span class="sxs-lookup"><span data-stu-id="50b79-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="50b79-111">Hierbei handelt es sich um einen lang andauernden Vorgang, der einige Minuten dauern kann.</span><span class="sxs-lookup"><span data-stu-id="50b79-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="50b79-112">Bitte üben Sie mit Vorsicht, wenn Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="50b79-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="50b79-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50b79-113">EXAMPLES</span></span>

### <span data-ttu-id="50b79-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50b79-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="50b79-115">Initiieren des Failover-Vorgangs des "myiothub"-Hubs</span><span class="sxs-lookup"><span data-stu-id="50b79-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="50b79-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="50b79-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="50b79-117">Initiieren des Failover-Vorgangs des "myiothub"-Hubs im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="50b79-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="50b79-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="50b79-118">PARAMETERS</span></span>

### <span data-ttu-id="50b79-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50b79-119">-AsJob</span></span>
<span data-ttu-id="50b79-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="50b79-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50b79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b79-121">-DefaultProfile</span></span>
<span data-ttu-id="50b79-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50b79-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50b79-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="50b79-123">-InputObject</span></span>
<span data-ttu-id="50b79-124">Viel Hub-Objekt</span><span class="sxs-lookup"><span data-stu-id="50b79-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="50b79-125">-Name</span><span class="sxs-lookup"><span data-stu-id="50b79-125">-Name</span></span>
<span data-ttu-id="50b79-126">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="50b79-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="50b79-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50b79-127">-PassThru</span></span>
<span data-ttu-id="50b79-128">Ermöglicht das Zurückgeben des booleschen Objekts.</span><span class="sxs-lookup"><span data-stu-id="50b79-128">Allows to return the boolean object.</span></span> <span data-ttu-id="50b79-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="50b79-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="50b79-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50b79-130">-ResourceGroupName</span></span>
<span data-ttu-id="50b79-131">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="50b79-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="50b79-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="50b79-132">-ResourceId</span></span>
<span data-ttu-id="50b79-133">Viel Hub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="50b79-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="50b79-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="50b79-134">-Confirm</span></span>
<span data-ttu-id="50b79-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50b79-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50b79-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50b79-136">-WhatIf</span></span>
<span data-ttu-id="50b79-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50b79-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50b79-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50b79-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50b79-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b79-139">CommonParameters</span></span>
<span data-ttu-id="50b79-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50b79-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b79-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b79-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b79-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50b79-142">INPUTS</span></span>

### <span data-ttu-id="50b79-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="50b79-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="50b79-144">System. String</span><span class="sxs-lookup"><span data-stu-id="50b79-144">System.String</span></span>

## <span data-ttu-id="50b79-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50b79-145">OUTPUTS</span></span>

### <span data-ttu-id="50b79-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50b79-146">System.Boolean</span></span>

## <span data-ttu-id="50b79-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="50b79-147">NOTES</span></span>

## <span data-ttu-id="50b79-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50b79-148">RELATED LINKS</span></span>
