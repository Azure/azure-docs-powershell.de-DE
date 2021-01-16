---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307755"
---
# <span data-ttu-id="4f85a-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="4f85a-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="4f85a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f85a-102">SYNOPSIS</span></span>
<span data-ttu-id="4f85a-103">Festlegen von Edgemodulen auf einem einzelnen Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="4f85a-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="4f85a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f85a-104">SYNTAX</span></span>

### <span data-ttu-id="4f85a-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f85a-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f85a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4f85a-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f85a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4f85a-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f85a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f85a-108">DESCRIPTION</span></span>
<span data-ttu-id="4f85a-109">Wendet den bereitgestellten Modulkonfigurationsinhalt auf das angegebene Edgegerät an.</span><span class="sxs-lookup"><span data-stu-id="4f85a-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="4f85a-110">Hinweis: Bei der Ausführung gibt der Befehl die Sammlung von Modulen aus, die auf das Gerät angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="4f85a-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="4f85a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f85a-111">EXAMPLES</span></span>

### <span data-ttu-id="4f85a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f85a-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="4f85a-113">Testen Sie Edgemodule während der Entwicklung, indem Sie Module auf einem Zielgerät festlegen.</span><span class="sxs-lookup"><span data-stu-id="4f85a-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="4f85a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f85a-114">PARAMETERS</span></span>

### <span data-ttu-id="4f85a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f85a-115">-DefaultProfile</span></span>
<span data-ttu-id="4f85a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f85a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f85a-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4f85a-117">-DeviceId</span></span>
<span data-ttu-id="4f85a-118">Ziel Edge-Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="4f85a-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="4f85a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f85a-119">-InputObject</span></span>
<span data-ttu-id="4f85a-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="4f85a-120">IotHub object</span></span>

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

### <span data-ttu-id="4f85a-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4f85a-121">-IotHubName</span></span>
<span data-ttu-id="4f85a-122">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="4f85a-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4f85a-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="4f85a-123">-ModulesContent</span></span>
<span data-ttu-id="4f85a-124">Konfigurationsinhalt von Modulen für IoT Edge-Geräte.</span><span class="sxs-lookup"><span data-stu-id="4f85a-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="4f85a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f85a-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f85a-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4f85a-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4f85a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f85a-127">-ResourceId</span></span>
<span data-ttu-id="4f85a-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4f85a-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4f85a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f85a-129">-Confirm</span></span>
<span data-ttu-id="4f85a-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f85a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f85a-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f85a-131">-WhatIf</span></span>
<span data-ttu-id="4f85a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f85a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f85a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f85a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f85a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f85a-134">CommonParameters</span></span>
<span data-ttu-id="4f85a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f85a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f85a-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f85a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f85a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f85a-137">INPUTS</span></span>

### <span data-ttu-id="4f85a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4f85a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4f85a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4f85a-139">System.String</span></span>

## <span data-ttu-id="4f85a-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f85a-140">OUTPUTS</span></span>

### <span data-ttu-id="4f85a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="4f85a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="4f85a-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f85a-142">NOTES</span></span>

## <span data-ttu-id="4f85a-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f85a-143">RELATED LINKS</span></span>
