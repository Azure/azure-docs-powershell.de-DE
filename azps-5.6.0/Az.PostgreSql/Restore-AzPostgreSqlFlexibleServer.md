---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 503d20a8473c83a9b2ca7ca1ec19deab6db7103c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919416"
---
# <span data-ttu-id="6fdc3-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="6fdc3-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="6fdc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fdc3-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdc3-103">Wiederherstellen eines flexiblen PostgreSQL-Servers aus einer vorhandenen Sicherung</span><span class="sxs-lookup"><span data-stu-id="6fdc3-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="6fdc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fdc3-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6fdc3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fdc3-105">DESCRIPTION</span></span>
<span data-ttu-id="6fdc3-106">Wiederherstellen eines Servers aus einer vorhandenen Sicherung</span><span class="sxs-lookup"><span data-stu-id="6fdc3-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="6fdc3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6fdc3-107">EXAMPLES</span></span>

### <span data-ttu-id="6fdc3-108">Beispiel 1: Wiederherstellen des PostgreSql-Servers mithilfe von PointInTime Restore</span><span class="sxs-lookup"><span data-stu-id="6fdc3-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="6fdc3-109">Diese Cmdlets wiederherstellen den PostgreSql-Server mithilfe von PointInTime Restore.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="6fdc3-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6fdc3-110">PARAMETERS</span></span>

### <span data-ttu-id="6fdc3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fdc3-111">-AsJob</span></span>
<span data-ttu-id="6fdc3-112">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="6fdc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdc3-113">-DefaultProfile</span></span>
<span data-ttu-id="6fdc3-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fdc3-115">-Location</span><span class="sxs-lookup"><span data-stu-id="6fdc3-115">-Location</span></span>
<span data-ttu-id="6fdc3-116">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-116">The location the resource resides in.</span></span>

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

### <span data-ttu-id="6fdc3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6fdc3-117">-Name</span></span>
<span data-ttu-id="6fdc3-118">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-118">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdc3-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6fdc3-119">-NoWait</span></span>
<span data-ttu-id="6fdc3-120">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6fdc3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fdc3-121">-ResourceGroupName</span></span>
<span data-ttu-id="6fdc3-122">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6fdc3-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="6fdc3-123">-RestorePointInTime</span></span>
<span data-ttu-id="6fdc3-124">Der Zeitpunkt der Wiederherstellung aus (ISO8601-Format), z. B. 2017-04-26T02:10:00+08:00.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdc3-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="6fdc3-125">-SourceServerName</span></span>
<span data-ttu-id="6fdc3-126">Der Name des Quellservers.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-126">The name of the source server.</span></span>

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

### <span data-ttu-id="6fdc3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6fdc3-127">-SubscriptionId</span></span>
<span data-ttu-id="6fdc3-128">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6fdc3-129">-Zone</span><span class="sxs-lookup"><span data-stu-id="6fdc3-129">-Zone</span></span>
<span data-ttu-id="6fdc3-130">Verfügbarkeitszone, in der die Ressource bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-130">Availability zone into which to provision the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdc3-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6fdc3-131">-Confirm</span></span>
<span data-ttu-id="6fdc3-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fdc3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fdc3-133">-WhatIf</span></span>
<span data-ttu-id="6fdc3-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fdc3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fdc3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdc3-136">CommonParameters</span></span>
<span data-ttu-id="6fdc3-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fdc3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdc3-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fdc3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdc3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6fdc3-139">INPUTS</span></span>

## <span data-ttu-id="6fdc3-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6fdc3-140">OUTPUTS</span></span>

### <span data-ttu-id="6fdc3-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="6fdc3-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="6fdc3-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6fdc3-142">NOTES</span></span>

<span data-ttu-id="6fdc3-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6fdc3-143">ALIASES</span></span>

## <span data-ttu-id="6fdc3-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6fdc3-144">RELATED LINKS</span></span>

