---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467707"
---
# <span data-ttu-id="3c53c-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="3c53c-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="3c53c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c53c-102">SYNOPSIS</span></span>
<span data-ttu-id="3c53c-103">Erstellt ein Speicherziel.</span><span class="sxs-lookup"><span data-stu-id="3c53c-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="3c53c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c53c-104">SYNTAX</span></span>

### <span data-ttu-id="3c53c-105">ClfsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c53c-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c53c-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c53c-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c53c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c53c-107">DESCRIPTION</span></span>
<span data-ttu-id="3c53c-108">Das **Cmdlet "New-AzHpcCacheStorageTarget"** fügt dem Azure -HPC-Cache ein Speicherziel hinzu.</span><span class="sxs-lookup"><span data-stu-id="3c53c-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="3c53c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c53c-109">EXAMPLES</span></span>

### <span data-ttu-id="3c53c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c53c-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="3c53c-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3c53c-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="3c53c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c53c-112">PARAMETERS</span></span>

### <span data-ttu-id="3c53c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c53c-113">-AsJob</span></span>
<span data-ttu-id="3c53c-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3c53c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c53c-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="3c53c-115">-CacheName</span></span>
<span data-ttu-id="3c53c-116">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="3c53c-116">Name of cache.</span></span>

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

### <span data-ttu-id="3c53c-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="3c53c-117">-CLFS</span></span>
<span data-ttu-id="3c53c-118">Aktualisieren Sie den CLFS-Speicherzieltyp.</span><span class="sxs-lookup"><span data-stu-id="3c53c-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="3c53c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c53c-119">-DefaultProfile</span></span>
<span data-ttu-id="3c53c-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c53c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c53c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3c53c-121">-Force</span></span>
<span data-ttu-id="3c53c-122">Zeigt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="3c53c-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="3c53c-123">Dieses Cmdlet fordert Sie standardmäßig auf zu bestätigen, dass Sie den Cache leeren möchten.</span><span class="sxs-lookup"><span data-stu-id="3c53c-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="3c53c-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="3c53c-124">-HostName</span></span>
<span data-ttu-id="3c53c-125">NFS-Hostname.</span><span class="sxs-lookup"><span data-stu-id="3c53c-125">NFS host name.</span></span>

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

### <span data-ttu-id="3c53c-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="3c53c-126">-Junction</span></span>
<span data-ttu-id="3c53c-127">Verbindung.</span><span class="sxs-lookup"><span data-stu-id="3c53c-127">Junction.</span></span>

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

### <span data-ttu-id="3c53c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3c53c-128">-Name</span></span>
<span data-ttu-id="3c53c-129">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="3c53c-129">Name of storage target.</span></span>

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

### <span data-ttu-id="3c53c-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="3c53c-130">-NFS</span></span>
<span data-ttu-id="3c53c-131">Aktualisieren Sie den NFS-Speicherzieltyp.</span><span class="sxs-lookup"><span data-stu-id="3c53c-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="3c53c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c53c-132">-ResourceGroupName</span></span>
<span data-ttu-id="3c53c-133">"Name der Ressourcengruppe, unter der Sie ein Speicherziel für einen bestimmten Cache erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="3c53c-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="3c53c-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="3c53c-134">-StorageContainerID</span></span>
<span data-ttu-id="3c53c-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="3c53c-135">StorageContainerID</span></span>

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

### <span data-ttu-id="3c53c-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="3c53c-136">-UsageModel</span></span>
<span data-ttu-id="3c53c-137">NFS-Verwendungsmodell.</span><span class="sxs-lookup"><span data-stu-id="3c53c-137">NFS usage model.</span></span>

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

### <span data-ttu-id="3c53c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c53c-138">-Confirm</span></span>
<span data-ttu-id="3c53c-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c53c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c53c-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3c53c-140">-WhatIf</span></span>
<span data-ttu-id="3c53c-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c53c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c53c-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c53c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c53c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c53c-143">CommonParameters</span></span>
<span data-ttu-id="3c53c-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c53c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c53c-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c53c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c53c-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c53c-146">INPUTS</span></span>

### <span data-ttu-id="3c53c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3c53c-147">System.String</span></span>

## <span data-ttu-id="3c53c-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c53c-148">OUTPUTS</span></span>

### <span data-ttu-id="3c53c-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="3c53c-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="3c53c-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3c53c-150">NOTES</span></span>

## <span data-ttu-id="3c53c-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3c53c-151">RELATED LINKS</span></span>
