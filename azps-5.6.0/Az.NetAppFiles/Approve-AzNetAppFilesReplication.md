---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: ac562f95ad6d5cbc97e31cd3832b90d2aa2362e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926963"
---
# <span data-ttu-id="46e9f-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="46e9f-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="46e9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="46e9f-103">Genehmigen/Autorisieren der Replikationsverbindung auf dem Quellvolume</span><span class="sxs-lookup"><span data-stu-id="46e9f-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="46e9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46e9f-104">SYNTAX</span></span>

### <span data-ttu-id="46e9f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="46e9f-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46e9f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46e9f-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46e9f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46e9f-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e9f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46e9f-108">DESCRIPTION</span></span>
<span data-ttu-id="46e9f-109">Genehmigen der Replikationsverbindung auf dem Quellvolume</span><span class="sxs-lookup"><span data-stu-id="46e9f-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="46e9f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46e9f-110">EXAMPLES</span></span>

### <span data-ttu-id="46e9f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46e9f-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="46e9f-112">Mit diesem Befehl wird die Replikation in MyAnfVolume genehmigt.</span><span class="sxs-lookup"><span data-stu-id="46e9f-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="46e9f-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="46e9f-113">PARAMETERS</span></span>

### <span data-ttu-id="46e9f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46e9f-114">-AccountName</span></span>
<span data-ttu-id="46e9f-115">Der Name des ANF-Kontos des Replikationsquellenvolumes</span><span class="sxs-lookup"><span data-stu-id="46e9f-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="46e9f-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="46e9f-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="46e9f-117">Die Dateisystem-ID des Zieldatenschutzvolumes</span><span class="sxs-lookup"><span data-stu-id="46e9f-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="46e9f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e9f-118">-DefaultProfile</span></span>
<span data-ttu-id="46e9f-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46e9f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46e9f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46e9f-120">-InputObject</span></span>
<span data-ttu-id="46e9f-121">Das ANF-Quellvolumeobjekt für autorisiertes Replikationsziel</span><span class="sxs-lookup"><span data-stu-id="46e9f-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="46e9f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="46e9f-122">-Name</span></span>
<span data-ttu-id="46e9f-123">Der Name des ANF-Replikationsquellenvolumes</span><span class="sxs-lookup"><span data-stu-id="46e9f-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="46e9f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46e9f-124">-PassThru</span></span>
<span data-ttu-id="46e9f-125">Geben Sie zurück, ob die Replikationsautorisierung des angegebenen Volumes ausgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="46e9f-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="46e9f-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="46e9f-126">-PoolName</span></span>
<span data-ttu-id="46e9f-127">Der Name des ANF-Pools des Replikationsquellenvolumes</span><span class="sxs-lookup"><span data-stu-id="46e9f-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="46e9f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e9f-128">-ResourceGroupName</span></span>
<span data-ttu-id="46e9f-129">Die Ressourcengruppe des ANF-Replikationsquellenvolumes</span><span class="sxs-lookup"><span data-stu-id="46e9f-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="46e9f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46e9f-130">-ResourceId</span></span>
<span data-ttu-id="46e9f-131">Die Ressourcen-ID des ANF-Replikationsquellenvolumes</span><span class="sxs-lookup"><span data-stu-id="46e9f-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="46e9f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46e9f-132">-Confirm</span></span>
<span data-ttu-id="46e9f-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46e9f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e9f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e9f-134">-WhatIf</span></span>
<span data-ttu-id="46e9f-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46e9f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e9f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46e9f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e9f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e9f-137">CommonParameters</span></span>
<span data-ttu-id="46e9f-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e9f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e9f-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46e9f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e9f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46e9f-140">INPUTS</span></span>

### <span data-ttu-id="46e9f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="46e9f-141">System.String</span></span>

### <span data-ttu-id="46e9f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="46e9f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="46e9f-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46e9f-143">OUTPUTS</span></span>

### <span data-ttu-id="46e9f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46e9f-144">System.Boolean</span></span>

## <span data-ttu-id="46e9f-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="46e9f-145">NOTES</span></span>

## <span data-ttu-id="46e9f-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="46e9f-146">RELATED LINKS</span></span>
