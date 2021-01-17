---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380622"
---
# <span data-ttu-id="0c2d9-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="0c2d9-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="0c2d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2d9-103">Entfernen/Löschen der Replikationsverbindung für das Zielvolume und Senden der Freigabe an die Quellreplikation</span><span class="sxs-lookup"><span data-stu-id="0c2d9-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="0c2d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c2d9-104">SYNTAX</span></span>

### <span data-ttu-id="0c2d9-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c2d9-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c2d9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c2d9-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c2d9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c2d9-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c2d9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c2d9-108">DESCRIPTION</span></span>
<span data-ttu-id="0c2d9-109">Entfernen/Löschen der Replikationsverbindung für das Zielvolume und Senden der Freigabe an die Quellreplikation</span><span class="sxs-lookup"><span data-stu-id="0c2d9-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="0c2d9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c2d9-110">EXAMPLES</span></span>

### <span data-ttu-id="0c2d9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c2d9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="0c2d9-112">Dieser Befehl entfernt die ANF-Replikationsverbindung für "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="0c2d9-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="0c2d9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c2d9-113">PARAMETERS</span></span>

### <span data-ttu-id="0c2d9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c2d9-114">-AccountName</span></span>
<span data-ttu-id="0c2d9-115">Der Name des ANF-Kontos des Replikationsvolumes</span><span class="sxs-lookup"><span data-stu-id="0c2d9-115">The name of the ANF account of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2d9-116">-DefaultProfile</span></span>
<span data-ttu-id="0c2d9-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c2d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c2d9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c2d9-118">-InputObject</span></span>
<span data-ttu-id="0c2d9-119">Das ANF-Zielvolume mit der zu entfernende Replikation</span><span class="sxs-lookup"><span data-stu-id="0c2d9-119">The ANF destination volume with the replication to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2d9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0c2d9-120">-Name</span></span>
<span data-ttu-id="0c2d9-121">Der Name des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="0c2d9-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2d9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c2d9-122">-PassThru</span></span>
<span data-ttu-id="0c2d9-123">Zurückgeben, ob die angegebene ANF-Replikation erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="0c2d9-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="0c2d9-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="0c2d9-124">-PoolName</span></span>
<span data-ttu-id="0c2d9-125">Der Name des ANF-Pools des Replikationsvolumens</span><span class="sxs-lookup"><span data-stu-id="0c2d9-125">The name of the ANF pool of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c2d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c2d9-127">Die Ressourcengruppe des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="0c2d9-127">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2d9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c2d9-128">-ResourceId</span></span>
<span data-ttu-id="0c2d9-129">Die Ressourcen-ID des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="0c2d9-129">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2d9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c2d9-130">-Confirm</span></span>
<span data-ttu-id="0c2d9-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c2d9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c2d9-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0c2d9-132">-WhatIf</span></span>
<span data-ttu-id="0c2d9-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c2d9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c2d9-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c2d9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c2d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2d9-135">CommonParameters</span></span>
<span data-ttu-id="0c2d9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c2d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2d9-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c2d9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2d9-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c2d9-138">INPUTS</span></span>

### <span data-ttu-id="0c2d9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0c2d9-139">System.String</span></span>

### <span data-ttu-id="0c2d9-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="0c2d9-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="0c2d9-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c2d9-141">OUTPUTS</span></span>

### <span data-ttu-id="0c2d9-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c2d9-142">System.Boolean</span></span>

## <span data-ttu-id="0c2d9-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0c2d9-143">NOTES</span></span>

## <span data-ttu-id="0c2d9-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0c2d9-144">RELATED LINKS</span></span>
