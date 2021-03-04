---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 4087725afbf845e42c2a00952a818f5eb356d421
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926763"
---
# <span data-ttu-id="f9e5b-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="f9e5b-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="f9e5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e5b-103">Entfernen/Löschen der Replikationsverbindung auf dem Zielvolume und Senden der Freigabe an die Quellreplikation</span><span class="sxs-lookup"><span data-stu-id="f9e5b-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="f9e5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9e5b-104">SYNTAX</span></span>

### <span data-ttu-id="f9e5b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9e5b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9e5b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9e5b-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9e5b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9e5b-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9e5b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9e5b-108">DESCRIPTION</span></span>
<span data-ttu-id="f9e5b-109">Entfernen/Löschen der Replikationsverbindung auf dem Zielvolume und Senden der Freigabe an die Quellreplikation</span><span class="sxs-lookup"><span data-stu-id="f9e5b-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="f9e5b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9e5b-110">EXAMPLES</span></span>

### <span data-ttu-id="f9e5b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9e5b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="f9e5b-112">Mit diesem Befehl wird die ANF-Replikationsverbindung auf volume "MyDestinationAnfVolume" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="f9e5b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f9e5b-113">PARAMETERS</span></span>

### <span data-ttu-id="f9e5b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f9e5b-114">-AccountName</span></span>
<span data-ttu-id="f9e5b-115">Der Name des ANF-Kontos des Replikationsvolumens</span><span class="sxs-lookup"><span data-stu-id="f9e5b-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="f9e5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e5b-116">-DefaultProfile</span></span>
<span data-ttu-id="f9e5b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9e5b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9e5b-118">-InputObject</span></span>
<span data-ttu-id="f9e5b-119">Das ANF-Zielvolume mit der zu entfernende Replikation</span><span class="sxs-lookup"><span data-stu-id="f9e5b-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="f9e5b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f9e5b-120">-Name</span></span>
<span data-ttu-id="f9e5b-121">Der Name des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="f9e5b-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="f9e5b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9e5b-122">-PassThru</span></span>
<span data-ttu-id="f9e5b-123">Zurückgeben, ob die angegebene ANF-Replikation erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="f9e5b-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="f9e5b-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f9e5b-124">-PoolName</span></span>
<span data-ttu-id="f9e5b-125">Der Name des ANF-Pools des Replikationsvolumes</span><span class="sxs-lookup"><span data-stu-id="f9e5b-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="f9e5b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e5b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f9e5b-127">Die Ressourcengruppe des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="f9e5b-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="f9e5b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e5b-128">-ResourceId</span></span>
<span data-ttu-id="f9e5b-129">Die Ressourcen-ID des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="f9e5b-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="f9e5b-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9e5b-130">-Confirm</span></span>
<span data-ttu-id="f9e5b-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9e5b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9e5b-132">-WhatIf</span></span>
<span data-ttu-id="f9e5b-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9e5b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9e5b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e5b-135">CommonParameters</span></span>
<span data-ttu-id="f9e5b-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9e5b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e5b-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9e5b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e5b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9e5b-138">INPUTS</span></span>

### <span data-ttu-id="f9e5b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f9e5b-139">System.String</span></span>

### <span data-ttu-id="f9e5b-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f9e5b-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f9e5b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9e5b-141">OUTPUTS</span></span>

### <span data-ttu-id="f9e5b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f9e5b-142">System.Boolean</span></span>

## <span data-ttu-id="f9e5b-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f9e5b-143">NOTES</span></span>

## <span data-ttu-id="f9e5b-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f9e5b-144">RELATED LINKS</span></span>
