---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 71e1cd6ea8f7aaa228ccdc5032971decfb21b2f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366020"
---
# <span data-ttu-id="1ae52-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1ae52-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="1ae52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae52-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae52-103">Aktualisiert eine Rolle für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="1ae52-103">Updates a Role for a device</span></span>

## <span data-ttu-id="1ae52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ae52-104">SYNTAX</span></span>

### <span data-ttu-id="1ae52-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ae52-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae52-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae52-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae52-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ae52-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae52-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ae52-108">DESCRIPTION</span></span>
<span data-ttu-id="1ae52-109">Das **Cmdlet "Set-AzDataBoxEdgeRole"** aktualisiert eine IoT-Rolle für ein Data Box-Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="1ae52-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="1ae52-110">Die alten bereitgestellten Freigaben werden durch die neu bereitgestellten Freigaben im Parameter "ShareName" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1ae52-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="1ae52-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ae52-111">EXAMPLES</span></span>

### <span data-ttu-id="1ae52-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ae52-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="1ae52-113">"Freigabenamen" ersetzt die alten bereitgestellten Freigaben durch die neu bereitgestellten Freigaben.</span><span class="sxs-lookup"><span data-stu-id="1ae52-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="1ae52-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1ae52-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="1ae52-115">So teilen Sie die Bereitstellung aller Freigaben auf</span><span class="sxs-lookup"><span data-stu-id="1ae52-115">To unmount all shares</span></span>

## <span data-ttu-id="1ae52-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ae52-116">PARAMETERS</span></span>

### <span data-ttu-id="1ae52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae52-117">-DefaultProfile</span></span>
<span data-ttu-id="1ae52-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ae52-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae52-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1ae52-119">-DeviceName</span></span>
<span data-ttu-id="1ae52-120">Gerätename</span><span class="sxs-lookup"><span data-stu-id="1ae52-120">Device Name</span></span>

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

### <span data-ttu-id="1ae52-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ae52-121">-InputObject</span></span>
<span data-ttu-id="1ae52-122">Geben Sie bitte ein entsprechendes Geräteobjekt an.</span><span class="sxs-lookup"><span data-stu-id="1ae52-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae52-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1ae52-123">-Name</span></span>
<span data-ttu-id="1ae52-124">Name der Rolle</span><span class="sxs-lookup"><span data-stu-id="1ae52-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae52-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae52-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ae52-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="1ae52-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1ae52-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ae52-127">-ResourceId</span></span>
<span data-ttu-id="1ae52-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ae52-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1ae52-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1ae52-129">-ShareName</span></span>
<span data-ttu-id="1ae52-130">Teilen(en) in einer Rolle</span><span class="sxs-lookup"><span data-stu-id="1ae52-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae52-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ae52-131">-Confirm</span></span>
<span data-ttu-id="1ae52-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ae52-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae52-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1ae52-133">-WhatIf</span></span>
<span data-ttu-id="1ae52-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ae52-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ae52-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ae52-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae52-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae52-136">CommonParameters</span></span>
<span data-ttu-id="1ae52-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae52-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae52-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ae52-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae52-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ae52-139">INPUTS</span></span>

### <span data-ttu-id="1ae52-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1ae52-140">System.String</span></span>

### <span data-ttu-id="1ae52-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1ae52-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="1ae52-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ae52-142">OUTPUTS</span></span>

### <span data-ttu-id="1ae52-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1ae52-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="1ae52-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1ae52-144">NOTES</span></span>

## <span data-ttu-id="1ae52-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1ae52-145">RELATED LINKS</span></span>
