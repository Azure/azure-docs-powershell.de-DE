---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363067"
---
# <span data-ttu-id="493f8-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="493f8-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="493f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="493f8-102">SYNOPSIS</span></span>
<span data-ttu-id="493f8-103">Erstellt ein Speicherziel.</span><span class="sxs-lookup"><span data-stu-id="493f8-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="493f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="493f8-104">SYNTAX</span></span>

### <span data-ttu-id="493f8-105">ClfsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="493f8-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="493f8-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="493f8-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="493f8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="493f8-107">DESCRIPTION</span></span>
<span data-ttu-id="493f8-108">Das **Cmdlet "New-AzHpcCacheStorageTarget"** fügt dem Azure -HPC-Cache ein Speicherziel hinzu.</span><span class="sxs-lookup"><span data-stu-id="493f8-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="493f8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="493f8-109">EXAMPLES</span></span>

### <span data-ttu-id="493f8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="493f8-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="493f8-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="493f8-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="493f8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="493f8-112">PARAMETERS</span></span>

### <span data-ttu-id="493f8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="493f8-113">-AsJob</span></span>
<span data-ttu-id="493f8-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="493f8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="493f8-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="493f8-115">-CacheName</span></span>
<span data-ttu-id="493f8-116">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="493f8-116">Name of cache.</span></span>

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

### <span data-ttu-id="493f8-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="493f8-117">-CLFS</span></span>
<span data-ttu-id="493f8-118">Aktualisieren Sie den CLFS-Speicherzieltyp.</span><span class="sxs-lookup"><span data-stu-id="493f8-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="493f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493f8-119">-DefaultProfile</span></span>
<span data-ttu-id="493f8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="493f8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="493f8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="493f8-121">-Force</span></span>
<span data-ttu-id="493f8-122">Zeigt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="493f8-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="493f8-123">Dieses Cmdlet fordert Sie standardmäßig auf zu bestätigen, dass Sie den Cache leeren möchten.</span><span class="sxs-lookup"><span data-stu-id="493f8-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="493f8-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="493f8-124">-HostName</span></span>
<span data-ttu-id="493f8-125">NFS-Hostname.</span><span class="sxs-lookup"><span data-stu-id="493f8-125">NFS host name.</span></span>

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

### <span data-ttu-id="493f8-126">-Junction</span><span class="sxs-lookup"><span data-stu-id="493f8-126">-Junction</span></span>
<span data-ttu-id="493f8-127">Verbindung.</span><span class="sxs-lookup"><span data-stu-id="493f8-127">Junction.</span></span>

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

### <span data-ttu-id="493f8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="493f8-128">-Name</span></span>
<span data-ttu-id="493f8-129">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="493f8-129">Name of storage target.</span></span>

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

### <span data-ttu-id="493f8-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="493f8-130">-NFS</span></span>
<span data-ttu-id="493f8-131">Aktualisieren Sie den NFS-Speicherzieltyp.</span><span class="sxs-lookup"><span data-stu-id="493f8-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="493f8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="493f8-132">-ResourceGroupName</span></span>
<span data-ttu-id="493f8-133">"Name der Ressourcengruppe, unter der Sie ein Speicherziel für einen bestimmten Cache erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="493f8-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="493f8-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="493f8-134">-StorageContainerID</span></span>
<span data-ttu-id="493f8-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="493f8-135">StorageContainerID</span></span>

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

### <span data-ttu-id="493f8-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="493f8-136">-UsageModel</span></span>
<span data-ttu-id="493f8-137">NFS-Verwendungsmodell.</span><span class="sxs-lookup"><span data-stu-id="493f8-137">NFS usage model.</span></span>

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

### <span data-ttu-id="493f8-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="493f8-138">-Confirm</span></span>
<span data-ttu-id="493f8-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="493f8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="493f8-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="493f8-140">-WhatIf</span></span>
<span data-ttu-id="493f8-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="493f8-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="493f8-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="493f8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="493f8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493f8-143">CommonParameters</span></span>
<span data-ttu-id="493f8-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="493f8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493f8-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="493f8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493f8-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="493f8-146">INPUTS</span></span>

### <span data-ttu-id="493f8-147">System.String</span><span class="sxs-lookup"><span data-stu-id="493f8-147">System.String</span></span>

## <span data-ttu-id="493f8-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="493f8-148">OUTPUTS</span></span>

### <span data-ttu-id="493f8-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="493f8-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="493f8-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="493f8-150">NOTES</span></span>

## <span data-ttu-id="493f8-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="493f8-151">RELATED LINKS</span></span>
