---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 22dee84aadc590d140d64cbd71eeaed3c16f03e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842400"
---
# <span data-ttu-id="ddee6-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ddee6-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="ddee6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ddee6-102">SYNOPSIS</span></span>
<span data-ttu-id="ddee6-103">Aktualisiert eine Rolle für ein Gerät</span><span class="sxs-lookup"><span data-stu-id="ddee6-103">Updates a Role for a device</span></span>

## <span data-ttu-id="ddee6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddee6-104">SYNTAX</span></span>

### <span data-ttu-id="ddee6-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ddee6-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddee6-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddee6-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddee6-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddee6-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddee6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ddee6-108">DESCRIPTION</span></span>
<span data-ttu-id="ddee6-109">Das Cmdlet " **Satz-AzDataBoxEdgeRole** " aktualisiert eine viel-Rolle für ein Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="ddee6-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="ddee6-110">Die alten gemounteten Freigaben werden durch die neu bereitgestellten Freigaben im Parameter Freigabename ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ddee6-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="ddee6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddee6-111">EXAMPLES</span></span>

### <span data-ttu-id="ddee6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddee6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="ddee6-113">Freigabenamen ersetzen die alten gemounteten Freigaben durch die neu bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="ddee6-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="ddee6-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ddee6-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="ddee6-115">So heben Sie die Bereitstellung aller Freigaben auf</span><span class="sxs-lookup"><span data-stu-id="ddee6-115">To unmount all shares</span></span>

## <span data-ttu-id="ddee6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddee6-116">PARAMETERS</span></span>

### <span data-ttu-id="ddee6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddee6-117">-DefaultProfile</span></span>
<span data-ttu-id="ddee6-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ddee6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddee6-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ddee6-119">-DeviceName</span></span>
<span data-ttu-id="ddee6-120">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="ddee6-120">Device Name</span></span>

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

### <span data-ttu-id="ddee6-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ddee6-121">-InputObject</span></span>
<span data-ttu-id="ddee6-122">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="ddee6-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="ddee6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ddee6-123">-Name</span></span>
<span data-ttu-id="ddee6-124">Name der Rolle</span><span class="sxs-lookup"><span data-stu-id="ddee6-124">Name of the Role</span></span>

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

### <span data-ttu-id="ddee6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddee6-125">-ResourceGroupName</span></span>
<span data-ttu-id="ddee6-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ddee6-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ddee6-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ddee6-127">-ResourceId</span></span>
<span data-ttu-id="ddee6-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="ddee6-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="ddee6-129">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="ddee6-129">-ShareName</span></span>
<span data-ttu-id="ddee6-130">Freigeben (en) in einer Rolle</span><span class="sxs-lookup"><span data-stu-id="ddee6-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="ddee6-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ddee6-131">-Confirm</span></span>
<span data-ttu-id="ddee6-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ddee6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddee6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddee6-133">-WhatIf</span></span>
<span data-ttu-id="ddee6-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddee6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddee6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddee6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddee6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddee6-136">CommonParameters</span></span>
<span data-ttu-id="ddee6-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddee6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddee6-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddee6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddee6-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ddee6-139">INPUTS</span></span>

### <span data-ttu-id="ddee6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ddee6-140">System.String</span></span>

### <span data-ttu-id="ddee6-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ddee6-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="ddee6-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ddee6-142">OUTPUTS</span></span>

### <span data-ttu-id="ddee6-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ddee6-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="ddee6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="ddee6-144">NOTES</span></span>

## <span data-ttu-id="ddee6-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ddee6-145">RELATED LINKS</span></span>
