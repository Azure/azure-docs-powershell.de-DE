---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176572"
---
# <span data-ttu-id="d50e3-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="d50e3-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="d50e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d50e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d50e3-103">Erstellt einen neuen Server.</span><span class="sxs-lookup"><span data-stu-id="d50e3-103">Creates a new server.</span></span>

## <span data-ttu-id="d50e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d50e3-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d50e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d50e3-105">DESCRIPTION</span></span>
<span data-ttu-id="d50e3-106">Erstellt einen neuen Server.</span><span class="sxs-lookup"><span data-stu-id="d50e3-106">Creates a new server.</span></span>

## <span data-ttu-id="d50e3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d50e3-107">EXAMPLES</span></span>

### <span data-ttu-id="d50e3-108">Beispiel 1: Erstellen eines neuen PostgreSQL-Servers</span><span class="sxs-lookup"><span data-stu-id="d50e3-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d50e3-109">Diese Cmdlets erstellen einen neuen PostgreSQL-Server.</span><span class="sxs-lookup"><span data-stu-id="d50e3-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="d50e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d50e3-110">PARAMETERS</span></span>

### <span data-ttu-id="d50e3-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d50e3-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d50e3-112">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="d50e3-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="d50e3-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="d50e3-113">-AdministratorUserName</span></span>
<span data-ttu-id="d50e3-114">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="d50e3-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="d50e3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d50e3-115">-AsJob</span></span>
<span data-ttu-id="d50e3-116">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="d50e3-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="d50e3-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="d50e3-117">-BackupRetentionDay</span></span>
<span data-ttu-id="d50e3-118">Aufbewahrungstage für Backups für den Server.</span><span class="sxs-lookup"><span data-stu-id="d50e3-118">Backup retention days for the server.</span></span>
<span data-ttu-id="d50e3-119">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="d50e3-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="d50e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d50e3-120">-DefaultProfile</span></span>
<span data-ttu-id="d50e3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d50e3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d50e3-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="d50e3-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="d50e3-123">Aktivieren Sie Geo-redundante oder nicht für Server-Backups.</span><span class="sxs-lookup"><span data-stu-id="d50e3-123">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="d50e3-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="d50e3-124">-Location</span></span>
<span data-ttu-id="d50e3-125">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="d50e3-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="d50e3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d50e3-126">-Name</span></span>
<span data-ttu-id="d50e3-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="d50e3-127">The name of the server.</span></span>

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

### <span data-ttu-id="d50e3-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d50e3-128">-NoWait</span></span>
<span data-ttu-id="d50e3-129">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="d50e3-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="d50e3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d50e3-130">-ResourceGroupName</span></span>
<span data-ttu-id="d50e3-131">Der Name der Ressourcengruppe, die die Ressource enthält, Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d50e3-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d50e3-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="d50e3-132">-Sku</span></span>
<span data-ttu-id="d50e3-133">Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d50e3-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="d50e3-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="d50e3-134">-SslEnforcement</span></span>
<span data-ttu-id="d50e3-135">Aktivieren der SSL-Erzwingung oder nicht beim Herstellen einer Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="d50e3-135">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="d50e3-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="d50e3-136">-StorageAutogrow</span></span>
<span data-ttu-id="d50e3-137">Aktivieren der automatischen Vergrößerung von Speicher.</span><span class="sxs-lookup"><span data-stu-id="d50e3-137">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="d50e3-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="d50e3-138">-StorageInMb</span></span>
<span data-ttu-id="d50e3-139">Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="d50e3-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="d50e3-140">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d50e3-140">-SubscriptionId</span></span>
<span data-ttu-id="d50e3-141">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d50e3-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d50e3-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="d50e3-142">-Tag</span></span>
<span data-ttu-id="d50e3-143">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="d50e3-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="d50e3-144">-Version</span><span class="sxs-lookup"><span data-stu-id="d50e3-144">-Version</span></span>
<span data-ttu-id="d50e3-145">Server Version.</span><span class="sxs-lookup"><span data-stu-id="d50e3-145">Server version.</span></span>

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

### <span data-ttu-id="d50e3-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d50e3-146">-Confirm</span></span>
<span data-ttu-id="d50e3-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d50e3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d50e3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d50e3-148">-WhatIf</span></span>
<span data-ttu-id="d50e3-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d50e3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d50e3-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d50e3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d50e3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50e3-151">CommonParameters</span></span>
<span data-ttu-id="d50e3-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d50e3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50e3-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d50e3-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50e3-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d50e3-154">INPUTS</span></span>

## <span data-ttu-id="d50e3-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d50e3-155">OUTPUTS</span></span>

### <span data-ttu-id="d50e3-156">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="d50e3-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="d50e3-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="d50e3-157">NOTES</span></span>

<span data-ttu-id="d50e3-158">Aliase</span><span class="sxs-lookup"><span data-stu-id="d50e3-158">ALIASES</span></span>

## <span data-ttu-id="d50e3-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d50e3-159">RELATED LINKS</span></span>

