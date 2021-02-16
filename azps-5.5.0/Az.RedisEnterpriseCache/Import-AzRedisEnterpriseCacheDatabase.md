---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 6ab4babd894a3c639db6e41e6088653604072c7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169204"
---
# <span data-ttu-id="4261c-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="4261c-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="4261c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4261c-102">SYNOPSIS</span></span>
<span data-ttu-id="4261c-103">Importiert eine Datenbankdatei in die Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="4261c-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="4261c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4261c-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4261c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4261c-105">DESCRIPTION</span></span>
<span data-ttu-id="4261c-106">Importiert eine Datenbankdatei in die Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="4261c-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="4261c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4261c-107">EXAMPLES</span></span>

### <span data-ttu-id="4261c-108">Beispiel 1: Importieren einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="4261c-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="4261c-109">Mit diesem Befehl wird eine Datenbankdatei in die Datenbank des Redis Enterprise-Caches namens "MyCache" importiert.</span><span class="sxs-lookup"><span data-stu-id="4261c-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="4261c-110">Beispiel 2: Importieren einer Datenbank (unter Verwendung des Beispieldateinamens)</span><span class="sxs-lookup"><span data-stu-id="4261c-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="4261c-111">Mit diesem Befehl wird eine Datenbankdatei in die Datenbank des Redis Enterprise-Caches namens "MyCache" importiert.</span><span class="sxs-lookup"><span data-stu-id="4261c-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="4261c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4261c-112">PARAMETERS</span></span>

### <span data-ttu-id="4261c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4261c-113">-AsJob</span></span>
<span data-ttu-id="4261c-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="4261c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4261c-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4261c-115">-ClusterName</span></span>
<span data-ttu-id="4261c-116">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4261c-116">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4261c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4261c-117">-DefaultProfile</span></span>
<span data-ttu-id="4261c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4261c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4261c-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4261c-119">-NoWait</span></span>
<span data-ttu-id="4261c-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="4261c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4261c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4261c-121">-PassThru</span></span>
<span data-ttu-id="4261c-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4261c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4261c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4261c-123">-ResourceGroupName</span></span>
<span data-ttu-id="4261c-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4261c-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4261c-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="4261c-125">-SasUri</span></span>
<span data-ttu-id="4261c-126">SAS-URI für das ziel-BLOB, aus dem importiert werden soll</span><span class="sxs-lookup"><span data-stu-id="4261c-126">SAS Uri for the target blob to import from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4261c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4261c-127">-SubscriptionId</span></span>
<span data-ttu-id="4261c-128">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="4261c-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4261c-129">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="4261c-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4261c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4261c-130">-Confirm</span></span>
<span data-ttu-id="4261c-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4261c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4261c-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4261c-132">-WhatIf</span></span>
<span data-ttu-id="4261c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4261c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4261c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4261c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4261c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4261c-135">CommonParameters</span></span>
<span data-ttu-id="4261c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4261c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4261c-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4261c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4261c-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4261c-138">INPUTS</span></span>

## <span data-ttu-id="4261c-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4261c-139">OUTPUTS</span></span>

### <span data-ttu-id="4261c-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4261c-140">System.Boolean</span></span>

## <span data-ttu-id="4261c-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4261c-141">NOTES</span></span>

<span data-ttu-id="4261c-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4261c-142">ALIASES</span></span>

## <span data-ttu-id="4261c-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4261c-143">RELATED LINKS</span></span>

