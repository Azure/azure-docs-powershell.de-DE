---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 71e1cd6ea8f7aaa228ccdc5032971decfb21b2f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298660"
---
# <span data-ttu-id="e130e-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e130e-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="e130e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e130e-102">SYNOPSIS</span></span>
<span data-ttu-id="e130e-103">Aktualisiert eine Rolle für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="e130e-103">Updates a Role for a device</span></span>

## <span data-ttu-id="e130e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e130e-104">SYNTAX</span></span>

### <span data-ttu-id="e130e-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e130e-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e130e-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e130e-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e130e-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e130e-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e130e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e130e-108">DESCRIPTION</span></span>
<span data-ttu-id="e130e-109">Das Cmdlet " **Satz-AzDataBoxEdgeRole** " aktualisiert eine viel-Rolle für ein Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="e130e-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="e130e-110">Die alten gemounteten Freigaben werden durch die neu bereitgestellten Freigaben im Parameter Freigabename ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e130e-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="e130e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e130e-111">EXAMPLES</span></span>

### <span data-ttu-id="e130e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e130e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="e130e-113">Freigabenamen ersetzen die alten gemounteten Freigaben durch die neu bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="e130e-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="e130e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e130e-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="e130e-115">So heben Sie die Bereitstellung aller Freigaben auf</span><span class="sxs-lookup"><span data-stu-id="e130e-115">To unmount all shares</span></span>

## <span data-ttu-id="e130e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="e130e-116">PARAMETERS</span></span>

### <span data-ttu-id="e130e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e130e-117">-DefaultProfile</span></span>
<span data-ttu-id="e130e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e130e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e130e-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e130e-119">-DeviceName</span></span>
<span data-ttu-id="e130e-120">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="e130e-120">Device Name</span></span>

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

### <span data-ttu-id="e130e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e130e-121">-InputObject</span></span>
<span data-ttu-id="e130e-122">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="e130e-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e130e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e130e-123">-Name</span></span>
<span data-ttu-id="e130e-124">Name der Rolle</span><span class="sxs-lookup"><span data-stu-id="e130e-124">Name of the Role</span></span>

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

### <span data-ttu-id="e130e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e130e-125">-ResourceGroupName</span></span>
<span data-ttu-id="e130e-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e130e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e130e-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e130e-127">-ResourceId</span></span>
<span data-ttu-id="e130e-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="e130e-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="e130e-129">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="e130e-129">-ShareName</span></span>
<span data-ttu-id="e130e-130">Freigeben (en) in einer Rolle</span><span class="sxs-lookup"><span data-stu-id="e130e-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="e130e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e130e-131">-Confirm</span></span>
<span data-ttu-id="e130e-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e130e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e130e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e130e-133">-WhatIf</span></span>
<span data-ttu-id="e130e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e130e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e130e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e130e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e130e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e130e-136">CommonParameters</span></span>
<span data-ttu-id="e130e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e130e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e130e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e130e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e130e-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e130e-139">INPUTS</span></span>

### <span data-ttu-id="e130e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e130e-140">System.String</span></span>

### <span data-ttu-id="e130e-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e130e-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="e130e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e130e-142">OUTPUTS</span></span>

### <span data-ttu-id="e130e-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e130e-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="e130e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e130e-144">NOTES</span></span>

## <span data-ttu-id="e130e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e130e-145">RELATED LINKS</span></span>
