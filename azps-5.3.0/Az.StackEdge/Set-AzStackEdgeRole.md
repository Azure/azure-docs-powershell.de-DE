---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374281"
---
# <span data-ttu-id="d44b1-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d44b1-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="d44b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d44b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d44b1-103">Aktualisiert eine Rolle für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="d44b1-103">Updates a Role for a device</span></span>

## <span data-ttu-id="d44b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d44b1-104">SYNTAX</span></span>

### <span data-ttu-id="d44b1-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d44b1-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44b1-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d44b1-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d44b1-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d44b1-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d44b1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d44b1-108">DESCRIPTION</span></span>
<span data-ttu-id="d44b1-109">Das **Cmdlet "Set-AzStackEdgeRole"** aktualisiert eine IoT-Rolle für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="d44b1-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="d44b1-110">Die alten bereitgestellten Freigaben werden durch die neu bereitgestellten Freigaben im Parameter "ShareName" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d44b1-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="d44b1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d44b1-111">EXAMPLES</span></span>

### <span data-ttu-id="d44b1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d44b1-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="d44b1-113">"Freigabenamen" ersetzt die alten bereitgestellten Freigaben durch die neu bereitgestellten Freigaben.</span><span class="sxs-lookup"><span data-stu-id="d44b1-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="d44b1-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d44b1-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="d44b1-115">So teilen Sie die Bereitstellung aller Freigaben auf</span><span class="sxs-lookup"><span data-stu-id="d44b1-115">To unmount all shares</span></span>

## <span data-ttu-id="d44b1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d44b1-116">PARAMETERS</span></span>

### <span data-ttu-id="d44b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d44b1-117">-DefaultProfile</span></span>
<span data-ttu-id="d44b1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d44b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d44b1-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d44b1-119">-DeviceName</span></span>
<span data-ttu-id="d44b1-120">Gerätename</span><span class="sxs-lookup"><span data-stu-id="d44b1-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d44b1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d44b1-121">-InputObject</span></span>
<span data-ttu-id="d44b1-122">Geben Sie ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="d44b1-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d44b1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d44b1-123">-Name</span></span>
<span data-ttu-id="d44b1-124">Name der Rolle</span><span class="sxs-lookup"><span data-stu-id="d44b1-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d44b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d44b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="d44b1-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d44b1-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d44b1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d44b1-127">-ResourceId</span></span>
<span data-ttu-id="d44b1-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d44b1-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d44b1-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d44b1-129">-ShareName</span></span>
<span data-ttu-id="d44b1-130">Teilen(en) in einer Rolle</span><span class="sxs-lookup"><span data-stu-id="d44b1-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d44b1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d44b1-131">-Confirm</span></span>
<span data-ttu-id="d44b1-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d44b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d44b1-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d44b1-133">-WhatIf</span></span>
<span data-ttu-id="d44b1-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d44b1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d44b1-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d44b1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d44b1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d44b1-136">CommonParameters</span></span>
<span data-ttu-id="d44b1-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d44b1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d44b1-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d44b1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d44b1-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d44b1-139">INPUTS</span></span>

### <span data-ttu-id="d44b1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d44b1-140">System.String</span></span>

### <span data-ttu-id="d44b1-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d44b1-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="d44b1-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d44b1-142">OUTPUTS</span></span>

### <span data-ttu-id="d44b1-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d44b1-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="d44b1-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d44b1-144">NOTES</span></span>

## <span data-ttu-id="d44b1-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d44b1-145">RELATED LINKS</span></span>
