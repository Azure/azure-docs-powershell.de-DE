---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 3b9ca8c4aa236b690bbe0dfe09c35f0ebc8a5b22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008380"
---
# <span data-ttu-id="da40c-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="da40c-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="da40c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da40c-102">SYNOPSIS</span></span>
<span data-ttu-id="da40c-103">Erstellt einen neuen Server.</span><span class="sxs-lookup"><span data-stu-id="da40c-103">Creates a new server.</span></span>

## <span data-ttu-id="da40c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da40c-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da40c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da40c-105">DESCRIPTION</span></span>
<span data-ttu-id="da40c-106">Erstellt einen neuen Server.</span><span class="sxs-lookup"><span data-stu-id="da40c-106">Creates a new server.</span></span>

## <span data-ttu-id="da40c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da40c-107">EXAMPLES</span></span>

### <span data-ttu-id="da40c-108">Beispiel 1: Erstellen eines neuen MySQL-Servers</span><span class="sxs-lookup"><span data-stu-id="da40c-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="da40c-109">Diese Cmdlets erstellen einen neuen MySQL-Server.</span><span class="sxs-lookup"><span data-stu-id="da40c-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="da40c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="da40c-110">PARAMETERS</span></span>

### <span data-ttu-id="da40c-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="da40c-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="da40c-112">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="da40c-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="da40c-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="da40c-113">-AdministratorUserName</span></span>
<span data-ttu-id="da40c-114">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="da40c-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="da40c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da40c-115">-AsJob</span></span>
<span data-ttu-id="da40c-116">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="da40c-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="da40c-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="da40c-117">-BackupRetentionDay</span></span>
<span data-ttu-id="da40c-118">Aufbewahrungstage für Backups für den Server.</span><span class="sxs-lookup"><span data-stu-id="da40c-118">Backup retention days for the server.</span></span>
<span data-ttu-id="da40c-119">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="da40c-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="da40c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da40c-120">-DefaultProfile</span></span>
<span data-ttu-id="da40c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da40c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da40c-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="da40c-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="da40c-123">Aktivieren Sie Geo-redundante oder nicht für Server-Backups.</span><span class="sxs-lookup"><span data-stu-id="da40c-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da40c-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="da40c-124">-Location</span></span>
<span data-ttu-id="da40c-125">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="da40c-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="da40c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="da40c-126">-Name</span></span>
<span data-ttu-id="da40c-127">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="da40c-127">The name of the server.</span></span>

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

### <span data-ttu-id="da40c-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="da40c-128">-NoWait</span></span>
<span data-ttu-id="da40c-129">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="da40c-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="da40c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da40c-130">-ResourceGroupName</span></span>
<span data-ttu-id="da40c-131">Der Name der Ressourcengruppe, die die Ressource enthält, Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="da40c-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="da40c-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="da40c-132">-Sku</span></span>
<span data-ttu-id="da40c-133">Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="da40c-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="da40c-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="da40c-134">-SslEnforcement</span></span>
<span data-ttu-id="da40c-135">Aktivieren der SSL-Erzwingung oder nicht beim Herstellen einer Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="da40c-135">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da40c-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="da40c-136">-StorageAutogrow</span></span>
<span data-ttu-id="da40c-137">Aktivieren der automatischen Vergrößerung von Speicher.</span><span class="sxs-lookup"><span data-stu-id="da40c-137">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da40c-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="da40c-138">-StorageInMb</span></span>
<span data-ttu-id="da40c-139">Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="da40c-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="da40c-140">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="da40c-140">-SubscriptionId</span></span>
<span data-ttu-id="da40c-141">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="da40c-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="da40c-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="da40c-142">-Tag</span></span>
<span data-ttu-id="da40c-143">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="da40c-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="da40c-144">-Version</span><span class="sxs-lookup"><span data-stu-id="da40c-144">-Version</span></span>
<span data-ttu-id="da40c-145">Server Version.</span><span class="sxs-lookup"><span data-stu-id="da40c-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da40c-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da40c-146">-Confirm</span></span>
<span data-ttu-id="da40c-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da40c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da40c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da40c-148">-WhatIf</span></span>
<span data-ttu-id="da40c-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da40c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da40c-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da40c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da40c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da40c-151">CommonParameters</span></span>
<span data-ttu-id="da40c-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da40c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da40c-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da40c-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da40c-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da40c-154">INPUTS</span></span>

## <span data-ttu-id="da40c-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da40c-155">OUTPUTS</span></span>

### <span data-ttu-id="da40c-156">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="da40c-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="da40c-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="da40c-157">NOTES</span></span>

<span data-ttu-id="da40c-158">Aliase</span><span class="sxs-lookup"><span data-stu-id="da40c-158">ALIASES</span></span>

## <span data-ttu-id="da40c-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da40c-159">RELATED LINKS</span></span>

