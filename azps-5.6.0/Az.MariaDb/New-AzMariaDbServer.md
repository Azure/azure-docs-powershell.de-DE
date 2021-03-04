---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: ccd05d8c0a7678b16831659fb0ca119adf94ddae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923536"
---
# <span data-ttu-id="423e2-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="423e2-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="423e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="423e2-102">SYNOPSIS</span></span>
<span data-ttu-id="423e2-103">Erstellt eine neue MariaDB.</span><span class="sxs-lookup"><span data-stu-id="423e2-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="423e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="423e2-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="423e2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="423e2-105">DESCRIPTION</span></span>
<span data-ttu-id="423e2-106">Erstellt eine neue MariaDB.</span><span class="sxs-lookup"><span data-stu-id="423e2-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="423e2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="423e2-107">EXAMPLES</span></span>

### <span data-ttu-id="423e2-108">Beispiel 1: Erstellen einer neuen MariaDB</span><span class="sxs-lookup"><span data-stu-id="423e2-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="423e2-109">Mit diesem Befehl wird eine neue MariaDB erstellt.</span><span class="sxs-lookup"><span data-stu-id="423e2-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="423e2-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="423e2-110">PARAMETERS</span></span>

### <span data-ttu-id="423e2-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="423e2-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="423e2-112">Kennwort des Administrators sollte SecureString sein.</span><span class="sxs-lookup"><span data-stu-id="423e2-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="423e2-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="423e2-113">-AdministratorUsername</span></span>
<span data-ttu-id="423e2-114">Benutzername des Administrators.</span><span class="sxs-lookup"><span data-stu-id="423e2-114">Username of administrator.</span></span>

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

### <span data-ttu-id="423e2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="423e2-115">-AsJob</span></span>
<span data-ttu-id="423e2-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="423e2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="423e2-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="423e2-117">-BackupRetentionDay</span></span>
<span data-ttu-id="423e2-118">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="423e2-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="423e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423e2-119">-DefaultProfile</span></span>
<span data-ttu-id="423e2-120">region DefaultParameters Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="423e2-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="423e2-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="423e2-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="423e2-122">Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="423e2-122">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423e2-123">-Location</span><span class="sxs-lookup"><span data-stu-id="423e2-123">-Location</span></span>
<span data-ttu-id="423e2-124">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="423e2-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="423e2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="423e2-125">-Name</span></span>
<span data-ttu-id="423e2-126">MariaDB-Servername.</span><span class="sxs-lookup"><span data-stu-id="423e2-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="423e2-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="423e2-127">-NoWait</span></span>
<span data-ttu-id="423e2-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="423e2-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="423e2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="423e2-129">-ResourceGroupName</span></span>
<span data-ttu-id="423e2-130">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="423e2-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="423e2-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="423e2-131">-Sku</span></span>
<span data-ttu-id="423e2-132">Der Name der Sku ist in der Regel Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="423e2-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="423e2-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="423e2-133">-SslEnforcement</span></span>
<span data-ttu-id="423e2-134">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="423e2-134">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423e2-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="423e2-135">-StorageAutogrow</span></span>
<span data-ttu-id="423e2-136">Aktivieren Sie "Automatisches Wachstum" für "Speicher".</span><span class="sxs-lookup"><span data-stu-id="423e2-136">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423e2-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="423e2-137">-StorageInMb</span></span>
<span data-ttu-id="423e2-138">Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="423e2-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="423e2-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="423e2-139">-SubscriptionId</span></span>
<span data-ttu-id="423e2-140">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="423e2-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="423e2-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="423e2-141">-Tag</span></span>
<span data-ttu-id="423e2-142">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="423e2-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="423e2-143">-Version</span><span class="sxs-lookup"><span data-stu-id="423e2-143">-Version</span></span>
<span data-ttu-id="423e2-144">Serverversion.</span><span class="sxs-lookup"><span data-stu-id="423e2-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423e2-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="423e2-145">-Confirm</span></span>
<span data-ttu-id="423e2-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="423e2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="423e2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="423e2-147">-WhatIf</span></span>
<span data-ttu-id="423e2-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="423e2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="423e2-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="423e2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="423e2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423e2-150">CommonParameters</span></span>
<span data-ttu-id="423e2-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="423e2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423e2-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="423e2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423e2-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="423e2-153">INPUTS</span></span>

## <span data-ttu-id="423e2-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="423e2-154">OUTPUTS</span></span>

### <span data-ttu-id="423e2-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="423e2-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="423e2-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="423e2-156">NOTES</span></span>

<span data-ttu-id="423e2-157">ALIASE</span><span class="sxs-lookup"><span data-stu-id="423e2-157">ALIASES</span></span>

## <span data-ttu-id="423e2-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="423e2-158">RELATED LINKS</span></span>

