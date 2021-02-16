---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151017"
---
# <span data-ttu-id="64c79-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="64c79-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="64c79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64c79-102">SYNOPSIS</span></span>
<span data-ttu-id="64c79-103">Exportiert eine Datenbankdatei aus der Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="64c79-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="64c79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64c79-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="64c79-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64c79-105">DESCRIPTION</span></span>
<span data-ttu-id="64c79-106">Exportiert eine Datenbankdatei aus der Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="64c79-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="64c79-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64c79-107">EXAMPLES</span></span>

### <span data-ttu-id="64c79-108">Beispiel 1: Exportieren einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="64c79-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="64c79-109">Mit diesem Befehl wird die Datenbank des Redis Enterprise-Caches namens "MyCache" in eine Datenbankdatei exportiert.</span><span class="sxs-lookup"><span data-stu-id="64c79-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="64c79-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64c79-110">PARAMETERS</span></span>

### <span data-ttu-id="64c79-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64c79-111">-AsJob</span></span>
<span data-ttu-id="64c79-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="64c79-112">Run the command as a job</span></span>

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

### <span data-ttu-id="64c79-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64c79-113">-ClusterName</span></span>
<span data-ttu-id="64c79-114">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="64c79-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="64c79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c79-115">-DefaultProfile</span></span>
<span data-ttu-id="64c79-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64c79-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64c79-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64c79-117">-NoWait</span></span>
<span data-ttu-id="64c79-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="64c79-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64c79-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64c79-119">-PassThru</span></span>
<span data-ttu-id="64c79-120">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="64c79-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64c79-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c79-121">-ResourceGroupName</span></span>
<span data-ttu-id="64c79-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64c79-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="64c79-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="64c79-123">-SasUri</span></span>
<span data-ttu-id="64c79-124">SAS-URI für das Zielverzeichnis, in das exportiert werden soll</span><span class="sxs-lookup"><span data-stu-id="64c79-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="64c79-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64c79-125">-SubscriptionId</span></span>
<span data-ttu-id="64c79-126">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="64c79-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="64c79-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="64c79-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64c79-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64c79-128">-Confirm</span></span>
<span data-ttu-id="64c79-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64c79-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64c79-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="64c79-130">-WhatIf</span></span>
<span data-ttu-id="64c79-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64c79-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64c79-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64c79-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64c79-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c79-133">CommonParameters</span></span>
<span data-ttu-id="64c79-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c79-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c79-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64c79-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c79-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64c79-136">INPUTS</span></span>

## <span data-ttu-id="64c79-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64c79-137">OUTPUTS</span></span>

### <span data-ttu-id="64c79-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64c79-138">System.Boolean</span></span>

## <span data-ttu-id="64c79-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="64c79-139">NOTES</span></span>

<span data-ttu-id="64c79-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="64c79-140">ALIASES</span></span>

## <span data-ttu-id="64c79-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="64c79-141">RELATED LINKS</span></span>

