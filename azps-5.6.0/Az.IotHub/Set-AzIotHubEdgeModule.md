---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: f3bc819c7050300c82f039981b1df34010771eb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918928"
---
# <span data-ttu-id="00545-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="00545-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="00545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00545-102">SYNOPSIS</span></span>
<span data-ttu-id="00545-103">Festlegen von Edgemodulen auf einem Gerät mit nur einer Kante</span><span class="sxs-lookup"><span data-stu-id="00545-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="00545-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00545-104">SYNTAX</span></span>

### <span data-ttu-id="00545-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="00545-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00545-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="00545-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00545-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="00545-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00545-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00545-108">DESCRIPTION</span></span>
<span data-ttu-id="00545-109">Wendet den bereitgestellten Modulkonfigurationsinhalt auf das angegebene Edgegerät an.</span><span class="sxs-lookup"><span data-stu-id="00545-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="00545-110">Hinweis: Bei der Ausführung gibt der Befehl die Sammlung der Module aus, die auf das Gerät angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="00545-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="00545-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00545-111">EXAMPLES</span></span>

### <span data-ttu-id="00545-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00545-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="00545-113">Testen Sie Edgemodule während der Entwicklung, indem Sie Module auf einem Zielgerät festlegen.</span><span class="sxs-lookup"><span data-stu-id="00545-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="00545-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="00545-114">PARAMETERS</span></span>

### <span data-ttu-id="00545-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00545-115">-DefaultProfile</span></span>
<span data-ttu-id="00545-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00545-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00545-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="00545-117">-DeviceId</span></span>
<span data-ttu-id="00545-118">Target Edge Device Id.</span><span class="sxs-lookup"><span data-stu-id="00545-118">Target Edge Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00545-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00545-119">-InputObject</span></span>
<span data-ttu-id="00545-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="00545-120">IotHub object</span></span>

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

### <span data-ttu-id="00545-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="00545-121">-IotHubName</span></span>
<span data-ttu-id="00545-122">Name des Iot-Hubs</span><span class="sxs-lookup"><span data-stu-id="00545-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="00545-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="00545-123">-ModulesContent</span></span>
<span data-ttu-id="00545-124">Konfigurationsinhalt von Modulen für IoT Edge-Geräte.</span><span class="sxs-lookup"><span data-stu-id="00545-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00545-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00545-125">-ResourceGroupName</span></span>
<span data-ttu-id="00545-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="00545-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="00545-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00545-127">-ResourceId</span></span>
<span data-ttu-id="00545-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="00545-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="00545-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00545-129">-Confirm</span></span>
<span data-ttu-id="00545-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00545-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00545-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00545-131">-WhatIf</span></span>
<span data-ttu-id="00545-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00545-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00545-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00545-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00545-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00545-134">CommonParameters</span></span>
<span data-ttu-id="00545-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00545-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00545-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00545-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00545-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00545-137">INPUTS</span></span>

### <span data-ttu-id="00545-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="00545-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="00545-139">System.String</span><span class="sxs-lookup"><span data-stu-id="00545-139">System.String</span></span>

## <span data-ttu-id="00545-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00545-140">OUTPUTS</span></span>

### <span data-ttu-id="00545-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="00545-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="00545-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="00545-142">NOTES</span></span>

## <span data-ttu-id="00545-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="00545-143">RELATED LINKS</span></span>
