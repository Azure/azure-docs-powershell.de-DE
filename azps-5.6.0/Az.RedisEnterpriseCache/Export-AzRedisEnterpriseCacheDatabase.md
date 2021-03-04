---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 3576cfb8185898ea7bb0fa2052a18b651d1d5cc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943901"
---
# <span data-ttu-id="3c63a-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="3c63a-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="3c63a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c63a-102">SYNOPSIS</span></span>
<span data-ttu-id="3c63a-103">Exportiert eine Datenbankdatei aus der Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="3c63a-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="3c63a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c63a-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3c63a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c63a-105">DESCRIPTION</span></span>
<span data-ttu-id="3c63a-106">Exportiert eine Datenbankdatei aus der Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="3c63a-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="3c63a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c63a-107">EXAMPLES</span></span>

### <span data-ttu-id="3c63a-108">Beispiel 1: Exportieren einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="3c63a-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="3c63a-109">Mit diesem Befehl wird die Datenbank des Redis Enterprise Cache namens MyCache in eine Datenbankdatei exportiert.</span><span class="sxs-lookup"><span data-stu-id="3c63a-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="3c63a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3c63a-110">PARAMETERS</span></span>

### <span data-ttu-id="3c63a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c63a-111">-AsJob</span></span>
<span data-ttu-id="3c63a-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3c63a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3c63a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3c63a-113">-ClusterName</span></span>
<span data-ttu-id="3c63a-114">Der Name des RedisEnterprise-Clusters.</span><span class="sxs-lookup"><span data-stu-id="3c63a-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="3c63a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c63a-115">-DefaultProfile</span></span>
<span data-ttu-id="3c63a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c63a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c63a-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3c63a-117">-NoWait</span></span>
<span data-ttu-id="3c63a-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3c63a-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3c63a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c63a-119">-PassThru</span></span>
<span data-ttu-id="3c63a-120">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c63a-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3c63a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c63a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3c63a-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3c63a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c63a-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="3c63a-123">-SasUri</span></span>
<span data-ttu-id="3c63a-124">SAS-Uri für das Zielverzeichnis, in das exportiert werden soll</span><span class="sxs-lookup"><span data-stu-id="3c63a-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="3c63a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c63a-125">-SubscriptionId</span></span>
<span data-ttu-id="3c63a-126">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3c63a-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c63a-127">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="3c63a-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3c63a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c63a-128">-Confirm</span></span>
<span data-ttu-id="3c63a-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c63a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c63a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c63a-130">-WhatIf</span></span>
<span data-ttu-id="3c63a-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c63a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c63a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c63a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c63a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c63a-133">CommonParameters</span></span>
<span data-ttu-id="3c63a-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c63a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c63a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c63a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c63a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c63a-136">INPUTS</span></span>

## <span data-ttu-id="3c63a-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c63a-137">OUTPUTS</span></span>

### <span data-ttu-id="3c63a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c63a-138">System.Boolean</span></span>

## <span data-ttu-id="3c63a-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3c63a-139">NOTES</span></span>

<span data-ttu-id="3c63a-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3c63a-140">ALIASES</span></span>

## <span data-ttu-id="3c63a-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3c63a-141">RELATED LINKS</span></span>

