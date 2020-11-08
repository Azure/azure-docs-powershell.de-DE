---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177598"
---
# <span data-ttu-id="48714-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="48714-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="48714-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48714-102">SYNOPSIS</span></span>
<span data-ttu-id="48714-103">Aktualisiert ein Speicherziel.</span><span class="sxs-lookup"><span data-stu-id="48714-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="48714-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48714-104">SYNTAX</span></span>

### <span data-ttu-id="48714-105">ClfsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="48714-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48714-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="48714-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48714-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48714-107">DESCRIPTION</span></span>
<span data-ttu-id="48714-108">Das Cmdlet " **Satz-AzHpcCacheStorageTarget** " aktualisiert ein Speicherziel, das an den Azure HPC-Cache angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="48714-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="48714-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48714-109">EXAMPLES</span></span>

### <span data-ttu-id="48714-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48714-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="48714-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="48714-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="48714-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="48714-112">PARAMETERS</span></span>

### <span data-ttu-id="48714-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48714-113">-AsJob</span></span>
<span data-ttu-id="48714-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="48714-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48714-115">-Cachename</span><span class="sxs-lookup"><span data-stu-id="48714-115">-CacheName</span></span>
<span data-ttu-id="48714-116">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="48714-116">Name of cache.</span></span>

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

### <span data-ttu-id="48714-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="48714-117">-CLFS</span></span>
<span data-ttu-id="48714-118">Aktualisieren Sie den CLFS-Speicher Zieltyp.</span><span class="sxs-lookup"><span data-stu-id="48714-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="48714-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48714-119">-DefaultProfile</span></span>
<span data-ttu-id="48714-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="48714-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48714-121">-Force</span><span class="sxs-lookup"><span data-stu-id="48714-121">-Force</span></span>
<span data-ttu-id="48714-122">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="48714-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="48714-123">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den Cache leeren möchten.</span><span class="sxs-lookup"><span data-stu-id="48714-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="48714-124">-Junction</span><span class="sxs-lookup"><span data-stu-id="48714-124">-Junction</span></span>
<span data-ttu-id="48714-125">Junction.</span><span class="sxs-lookup"><span data-stu-id="48714-125">Junction.</span></span>

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

### <span data-ttu-id="48714-126">-Name</span><span class="sxs-lookup"><span data-stu-id="48714-126">-Name</span></span>
<span data-ttu-id="48714-127">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="48714-127">Name of storage target.</span></span>

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

### <span data-ttu-id="48714-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="48714-128">-NFS</span></span>
<span data-ttu-id="48714-129">Aktualisieren des NFS-Speicher Zieltyps</span><span class="sxs-lookup"><span data-stu-id="48714-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="48714-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48714-130">-ResourceGroupName</span></span>
<span data-ttu-id="48714-131">Name der Ressourcengruppe, unter der Sie das Speicherziel aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="48714-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="48714-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="48714-132">-Confirm</span></span>
<span data-ttu-id="48714-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48714-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48714-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48714-134">-WhatIf</span></span>
<span data-ttu-id="48714-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48714-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48714-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48714-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48714-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48714-137">CommonParameters</span></span>
<span data-ttu-id="48714-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48714-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48714-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48714-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48714-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48714-140">INPUTS</span></span>

### <span data-ttu-id="48714-141">System. String</span><span class="sxs-lookup"><span data-stu-id="48714-141">System.String</span></span>

## <span data-ttu-id="48714-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48714-142">OUTPUTS</span></span>

### <span data-ttu-id="48714-143">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="48714-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="48714-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="48714-144">NOTES</span></span>

## <span data-ttu-id="48714-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48714-145">RELATED LINKS</span></span>
