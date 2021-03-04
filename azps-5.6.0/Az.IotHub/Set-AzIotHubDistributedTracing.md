---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: b1bdc6b5910f47fdca8e8b66ab99939945547a08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945137"
---
# <span data-ttu-id="fd258-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="fd258-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="fd258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd258-102">SYNOPSIS</span></span>
<span data-ttu-id="fd258-103">Aktualisieren Sie die Optionen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="fd258-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="fd258-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd258-104">SYNTAX</span></span>

### <span data-ttu-id="fd258-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd258-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd258-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd258-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd258-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd258-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd258-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd258-108">DESCRIPTION</span></span>
<span data-ttu-id="fd258-109">Aktualisieren Sie die Optionen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="fd258-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="fd258-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd258-110">EXAMPLES</span></span>

### <span data-ttu-id="fd258-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd258-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="fd258-112">Aktualisieren Sie die Optionen für die verteilte Ablaufverfolgung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="fd258-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="fd258-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fd258-113">PARAMETERS</span></span>

### <span data-ttu-id="fd258-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd258-114">-DefaultProfile</span></span>
<span data-ttu-id="fd258-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd258-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd258-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fd258-116">-DeviceId</span></span>
<span data-ttu-id="fd258-117">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="fd258-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd258-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd258-118">-InputObject</span></span>
<span data-ttu-id="fd258-119">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="fd258-119">IotHub object</span></span>

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

### <span data-ttu-id="fd258-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fd258-120">-IotHubName</span></span>
<span data-ttu-id="fd258-121">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="fd258-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fd258-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd258-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd258-123">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fd258-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fd258-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd258-124">-ResourceId</span></span>
<span data-ttu-id="fd258-125">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fd258-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fd258-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="fd258-126">-SamplingMode</span></span>
<span data-ttu-id="fd258-127">Aktiviert und deaktiviert die Stichproben für die verteilte Ablaufverfolgung.</span><span class="sxs-lookup"><span data-stu-id="fd258-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd258-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="fd258-128">-SamplingRate</span></span>
<span data-ttu-id="fd258-129">Steuert die Anzahl der Nachrichten, die zum Hinzufügen des Ablaufverfolgungskontexts in der Stichprobe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fd258-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="fd258-130">Dieser Wert ist ein Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="fd258-130">This value is a percentage.</span></span>
<span data-ttu-id="fd258-131">Nur Werte von 0 bis 100 (einschließlich) sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="fd258-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd258-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd258-132">-Confirm</span></span>
<span data-ttu-id="fd258-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd258-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd258-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd258-134">-WhatIf</span></span>
<span data-ttu-id="fd258-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd258-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd258-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd258-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd258-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd258-137">CommonParameters</span></span>
<span data-ttu-id="fd258-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd258-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd258-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd258-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd258-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd258-140">INPUTS</span></span>

### <span data-ttu-id="fd258-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fd258-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fd258-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fd258-142">System.String</span></span>

## <span data-ttu-id="fd258-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd258-143">OUTPUTS</span></span>

### <span data-ttu-id="fd258-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="fd258-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="fd258-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fd258-145">NOTES</span></span>

## <span data-ttu-id="fd258-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fd258-146">RELATED LINKS</span></span>
