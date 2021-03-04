---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: deb359905086d68edb4129e023ce6dd8d2ceaf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949379"
---
# <span data-ttu-id="3dc86-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="3dc86-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="3dc86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dc86-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc86-103">Erstellt ein Speicherziel.</span><span class="sxs-lookup"><span data-stu-id="3dc86-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="3dc86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3dc86-104">SYNTAX</span></span>

### <span data-ttu-id="3dc86-105">ClfsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3dc86-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dc86-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dc86-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc86-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3dc86-107">DESCRIPTION</span></span>
<span data-ttu-id="3dc86-108">Das **Cmdlet New-AzHpcCacheStorageTarget** fügt dem Azure HPC-Cache ein Speicherziel hinzu.</span><span class="sxs-lookup"><span data-stu-id="3dc86-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="3dc86-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3dc86-109">EXAMPLES</span></span>

### <span data-ttu-id="3dc86-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3dc86-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="3dc86-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3dc86-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="3dc86-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3dc86-112">PARAMETERS</span></span>

### <span data-ttu-id="3dc86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dc86-113">-AsJob</span></span>
<span data-ttu-id="3dc86-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3dc86-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dc86-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="3dc86-115">-CacheName</span></span>
<span data-ttu-id="3dc86-116">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="3dc86-116">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc86-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="3dc86-117">-CLFS</span></span>
<span data-ttu-id="3dc86-118">Aktualisieren sie den CLFS-Speicherzieltyp.</span><span class="sxs-lookup"><span data-stu-id="3dc86-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc86-119">-DefaultProfile</span></span>
<span data-ttu-id="3dc86-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3dc86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dc86-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3dc86-121">-Force</span></span>
<span data-ttu-id="3dc86-122">Gibt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="3dc86-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="3dc86-123">Standardmäßig werden Sie in diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den Cache leeren möchten.</span><span class="sxs-lookup"><span data-stu-id="3dc86-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="3dc86-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="3dc86-124">-HostName</span></span>
<span data-ttu-id="3dc86-125">NFS-Hostname.</span><span class="sxs-lookup"><span data-stu-id="3dc86-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc86-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="3dc86-126">-Junction</span></span>
<span data-ttu-id="3dc86-127">Junction.</span><span class="sxs-lookup"><span data-stu-id="3dc86-127">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc86-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3dc86-128">-Name</span></span>
<span data-ttu-id="3dc86-129">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="3dc86-129">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc86-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="3dc86-130">-NFS</span></span>
<span data-ttu-id="3dc86-131">Aktualisieren Sie den NFS-Speicherzieltyp.</span><span class="sxs-lookup"><span data-stu-id="3dc86-131">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc86-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc86-132">-ResourceGroupName</span></span>
<span data-ttu-id="3dc86-133">"Name der Ressourcengruppe, unter der Sie das Speicherziel für einen bestimmten Cache erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="3dc86-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc86-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="3dc86-134">-StorageContainerID</span></span>
<span data-ttu-id="3dc86-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="3dc86-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc86-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="3dc86-136">-UsageModel</span></span>
<span data-ttu-id="3dc86-137">NFS-Nutzungsmodell.</span><span class="sxs-lookup"><span data-stu-id="3dc86-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc86-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3dc86-138">-Confirm</span></span>
<span data-ttu-id="3dc86-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3dc86-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc86-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc86-140">-WhatIf</span></span>
<span data-ttu-id="3dc86-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3dc86-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dc86-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3dc86-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc86-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc86-143">CommonParameters</span></span>
<span data-ttu-id="3dc86-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc86-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc86-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dc86-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc86-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3dc86-146">INPUTS</span></span>

### <span data-ttu-id="3dc86-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3dc86-147">System.String</span></span>

## <span data-ttu-id="3dc86-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3dc86-148">OUTPUTS</span></span>

### <span data-ttu-id="3dc86-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="3dc86-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="3dc86-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3dc86-150">NOTES</span></span>

## <span data-ttu-id="3dc86-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3dc86-151">RELATED LINKS</span></span>
