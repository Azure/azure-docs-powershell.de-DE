---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293357"
---
# <span data-ttu-id="ce0b1-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="ce0b1-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="ce0b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0b1-103">Erstellt einen neuen Server.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-103">Creates a new server.</span></span>

## <span data-ttu-id="ce0b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce0b1-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce0b1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce0b1-105">DESCRIPTION</span></span>
<span data-ttu-id="ce0b1-106">Erstellt einen neuen Server.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-106">Creates a new server.</span></span>

## <span data-ttu-id="ce0b1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce0b1-107">EXAMPLES</span></span>

### <span data-ttu-id="ce0b1-108">Beispiel 1: Erstellen eines neuen PostgreSql-Servers</span><span class="sxs-lookup"><span data-stu-id="ce0b1-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="ce0b1-109">Diese Cmdlets erstellen einen neuen PostgreSql-Server.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="ce0b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce0b1-110">PARAMETERS</span></span>

### <span data-ttu-id="ce0b1-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ce0b1-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ce0b1-112">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-112">The location the resource resides in.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0b1-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="ce0b1-113">-AdministratorUserName</span></span>
<span data-ttu-id="ce0b1-114">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ce0b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce0b1-115">-AsJob</span></span>
<span data-ttu-id="ce0b1-116">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="ce0b1-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ce0b1-117">-BackupRetentionDay</span></span>
<span data-ttu-id="ce0b1-118">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-118">Backup retention days for the server.</span></span>
<span data-ttu-id="ce0b1-119">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-119">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0b1-120">-DefaultProfile</span></span>
<span data-ttu-id="ce0b1-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce0b1-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="ce0b1-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="ce0b1-123">Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0b1-124">-Location</span><span class="sxs-lookup"><span data-stu-id="ce0b1-124">-Location</span></span>
<span data-ttu-id="ce0b1-125">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ce0b1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ce0b1-126">-Name</span></span>
<span data-ttu-id="ce0b1-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-127">The name of the server.</span></span>

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

### <span data-ttu-id="ce0b1-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ce0b1-128">-NoWait</span></span>
<span data-ttu-id="ce0b1-129">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ce0b1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0b1-130">-ResourceGroupName</span></span>
<span data-ttu-id="ce0b1-131">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ce0b1-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="ce0b1-132">-Sku</span></span>
<span data-ttu-id="ce0b1-133">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="ce0b1-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="ce0b1-134">-SslEnforcement</span></span>
<span data-ttu-id="ce0b1-135">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-135">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0b1-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="ce0b1-136">-StorageAutogrow</span></span>
<span data-ttu-id="ce0b1-137">Aktivieren Sie "Automatisches Anwachsen des Speichers".</span><span class="sxs-lookup"><span data-stu-id="ce0b1-137">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0b1-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ce0b1-138">-StorageInMb</span></span>
<span data-ttu-id="ce0b1-139">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-139">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0b1-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce0b1-140">-SubscriptionId</span></span>
<span data-ttu-id="ce0b1-141">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ce0b1-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce0b1-142">-Tag</span></span>
<span data-ttu-id="ce0b1-143">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-143">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0b1-144">-Version</span><span class="sxs-lookup"><span data-stu-id="ce0b1-144">-Version</span></span>
<span data-ttu-id="ce0b1-145">Serverversion.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0b1-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce0b1-146">-Confirm</span></span>
<span data-ttu-id="ce0b1-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce0b1-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ce0b1-148">-WhatIf</span></span>
<span data-ttu-id="ce0b1-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce0b1-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce0b1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0b1-151">CommonParameters</span></span>
<span data-ttu-id="ce0b1-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0b1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0b1-153">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce0b1-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0b1-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce0b1-154">INPUTS</span></span>

## <span data-ttu-id="ce0b1-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce0b1-155">OUTPUTS</span></span>

### <span data-ttu-id="ce0b1-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="ce0b1-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="ce0b1-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce0b1-157">NOTES</span></span>

<span data-ttu-id="ce0b1-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ce0b1-158">ALIASES</span></span>

## <span data-ttu-id="ce0b1-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce0b1-159">RELATED LINKS</span></span>

