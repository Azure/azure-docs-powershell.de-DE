---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 5f5dac2f2028de9b90941ef91c38361c4357fc8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926731"
---
# <span data-ttu-id="8f03f-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="8f03f-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="8f03f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f03f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f03f-103">Fortsetzen/Erneutes Synchronisieren der Verbindung auf dem Zielvolume</span><span class="sxs-lookup"><span data-stu-id="8f03f-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="8f03f-104">Wenn der Vorgang auf dem Quellvolume verwendet wird, wird die Verbindung umgekehrt synchronisiert und von Quelle zu Ziel synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="8f03f-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="8f03f-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f03f-105">SYNTAX</span></span>

### <span data-ttu-id="8f03f-106">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f03f-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f03f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f03f-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f03f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f03f-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f03f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f03f-109">DESCRIPTION</span></span>
<span data-ttu-id="8f03f-110">Fortsetzen/Erneutes Synchronisieren der Verbindung auf dem Zielvolume</span><span class="sxs-lookup"><span data-stu-id="8f03f-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="8f03f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f03f-111">EXAMPLES</span></span>

### <span data-ttu-id="8f03f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f03f-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="8f03f-113">Mit diesem Befehl wird die ANF-Replikationsverbindung auf volume "MyDestinationAnfVolume" fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="8f03f-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="8f03f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8f03f-114">PARAMETERS</span></span>

### <span data-ttu-id="8f03f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8f03f-115">-AccountName</span></span>
<span data-ttu-id="8f03f-116">Der Name des ANF-Kontos des Replikationsvolumens</span><span class="sxs-lookup"><span data-stu-id="8f03f-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="8f03f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f03f-117">-DefaultProfile</span></span>
<span data-ttu-id="8f03f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f03f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f03f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f03f-119">-InputObject</span></span>
<span data-ttu-id="8f03f-120">Das neu zu synchronisierende ANF-Replikationszielvolumeobjekt</span><span class="sxs-lookup"><span data-stu-id="8f03f-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="8f03f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8f03f-121">-Name</span></span>
<span data-ttu-id="8f03f-122">Der Name des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="8f03f-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="8f03f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f03f-123">-PassThru</span></span>
<span data-ttu-id="8f03f-124">Gibt zurück, ob eine Erneute Synchronisierung des angegebenen Replikationsvolumens ausgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="8f03f-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="8f03f-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8f03f-125">-PoolName</span></span>
<span data-ttu-id="8f03f-126">Der Name des ANF-Pools des Replikationsvolumes</span><span class="sxs-lookup"><span data-stu-id="8f03f-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="8f03f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f03f-127">-ResourceGroupName</span></span>
<span data-ttu-id="8f03f-128">Die Ressourcengruppe des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="8f03f-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="8f03f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f03f-129">-ResourceId</span></span>
<span data-ttu-id="8f03f-130">Die Ressourcen-ID des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="8f03f-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="8f03f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f03f-131">-Confirm</span></span>
<span data-ttu-id="8f03f-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f03f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f03f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f03f-133">-WhatIf</span></span>
<span data-ttu-id="8f03f-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f03f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f03f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f03f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f03f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f03f-136">CommonParameters</span></span>
<span data-ttu-id="8f03f-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f03f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f03f-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f03f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f03f-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f03f-139">INPUTS</span></span>

### <span data-ttu-id="8f03f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8f03f-140">System.String</span></span>

### <span data-ttu-id="8f03f-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8f03f-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8f03f-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f03f-142">OUTPUTS</span></span>

### <span data-ttu-id="8f03f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f03f-143">System.Boolean</span></span>

## <span data-ttu-id="8f03f-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8f03f-144">NOTES</span></span>

## <span data-ttu-id="8f03f-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8f03f-145">RELATED LINKS</span></span>
