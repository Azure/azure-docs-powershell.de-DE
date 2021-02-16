---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175308"
---
# <span data-ttu-id="cda61-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="cda61-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="cda61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cda61-102">SYNOPSIS</span></span>
<span data-ttu-id="cda61-103">Erstellt ein Speicherziel.</span><span class="sxs-lookup"><span data-stu-id="cda61-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="cda61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cda61-104">SYNTAX</span></span>

### <span data-ttu-id="cda61-105">ClfsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cda61-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cda61-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="cda61-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cda61-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cda61-107">DESCRIPTION</span></span>
<span data-ttu-id="cda61-108">Das **Cmdlet "New-AzHpcCacheStorageTarget"** fügt dem Azure -HPC-Cache ein Speicherziel hinzu.</span><span class="sxs-lookup"><span data-stu-id="cda61-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="cda61-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cda61-109">EXAMPLES</span></span>

### <span data-ttu-id="cda61-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cda61-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="cda61-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cda61-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="cda61-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cda61-112">PARAMETERS</span></span>

### <span data-ttu-id="cda61-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cda61-113">-AsJob</span></span>
<span data-ttu-id="cda61-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cda61-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cda61-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="cda61-115">-CacheName</span></span>
<span data-ttu-id="cda61-116">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="cda61-116">Name of cache.</span></span>

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

### <span data-ttu-id="cda61-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="cda61-117">-CLFS</span></span>
<span data-ttu-id="cda61-118">Aktualisieren Sie den CLFS-Speicherzieltyp.</span><span class="sxs-lookup"><span data-stu-id="cda61-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="cda61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda61-119">-DefaultProfile</span></span>
<span data-ttu-id="cda61-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cda61-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cda61-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cda61-121">-Force</span></span>
<span data-ttu-id="cda61-122">Zeigt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="cda61-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="cda61-123">Dieses Cmdlet fordert Sie standardmäßig auf zu bestätigen, dass Sie den Cache leeren möchten.</span><span class="sxs-lookup"><span data-stu-id="cda61-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="cda61-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="cda61-124">-HostName</span></span>
<span data-ttu-id="cda61-125">NFS-Hostname.</span><span class="sxs-lookup"><span data-stu-id="cda61-125">NFS host name.</span></span>

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

### <span data-ttu-id="cda61-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="cda61-126">-Junction</span></span>
<span data-ttu-id="cda61-127">Verbindung.</span><span class="sxs-lookup"><span data-stu-id="cda61-127">Junction.</span></span>

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

### <span data-ttu-id="cda61-128">-Name</span><span class="sxs-lookup"><span data-stu-id="cda61-128">-Name</span></span>
<span data-ttu-id="cda61-129">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="cda61-129">Name of storage target.</span></span>

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

### <span data-ttu-id="cda61-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="cda61-130">-NFS</span></span>
<span data-ttu-id="cda61-131">Aktualisieren Sie den NFS-Speicherzieltyp.</span><span class="sxs-lookup"><span data-stu-id="cda61-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="cda61-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda61-132">-ResourceGroupName</span></span>
<span data-ttu-id="cda61-133">"Name der Ressourcengruppe, unter der Sie ein Speicherziel für einen bestimmten Cache erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="cda61-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="cda61-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="cda61-134">-StorageContainerID</span></span>
<span data-ttu-id="cda61-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="cda61-135">StorageContainerID</span></span>

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

### <span data-ttu-id="cda61-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="cda61-136">-UsageModel</span></span>
<span data-ttu-id="cda61-137">NFS-Verwendungsmodell.</span><span class="sxs-lookup"><span data-stu-id="cda61-137">NFS usage model.</span></span>

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

### <span data-ttu-id="cda61-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cda61-138">-Confirm</span></span>
<span data-ttu-id="cda61-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cda61-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda61-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cda61-140">-WhatIf</span></span>
<span data-ttu-id="cda61-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cda61-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cda61-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cda61-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cda61-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda61-143">CommonParameters</span></span>
<span data-ttu-id="cda61-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda61-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda61-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cda61-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda61-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cda61-146">INPUTS</span></span>

### <span data-ttu-id="cda61-147">System.String</span><span class="sxs-lookup"><span data-stu-id="cda61-147">System.String</span></span>

## <span data-ttu-id="cda61-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cda61-148">OUTPUTS</span></span>

### <span data-ttu-id="cda61-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="cda61-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="cda61-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cda61-150">NOTES</span></span>

## <span data-ttu-id="cda61-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cda61-151">RELATED LINKS</span></span>
