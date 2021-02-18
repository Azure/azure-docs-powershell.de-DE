---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 37e8896389931f6909d783cbb07a694ed6186fc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173052"
---
# <span data-ttu-id="b3504-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="b3504-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="b3504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3504-102">SYNOPSIS</span></span>
<span data-ttu-id="b3504-103">Erstellt einen neuen Server.</span><span class="sxs-lookup"><span data-stu-id="b3504-103">Creates a new server.</span></span>

## <span data-ttu-id="b3504-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3504-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3504-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3504-105">DESCRIPTION</span></span>
<span data-ttu-id="b3504-106">Erstellt einen neuen Server.</span><span class="sxs-lookup"><span data-stu-id="b3504-106">Creates a new server.</span></span>

## <span data-ttu-id="b3504-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3504-107">EXAMPLES</span></span>

### <span data-ttu-id="b3504-108">Beispiel 1: Erstellen eines neuen Server in MySql</span><span class="sxs-lookup"><span data-stu-id="b3504-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="b3504-109">Diese Cmdlets erstellen einen neuen MySql-Server.</span><span class="sxs-lookup"><span data-stu-id="b3504-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="b3504-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3504-110">PARAMETERS</span></span>

### <span data-ttu-id="b3504-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b3504-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b3504-112">Das Kennwort des Administrators.</span><span class="sxs-lookup"><span data-stu-id="b3504-112">The password of the administrator.</span></span>
<span data-ttu-id="b3504-113">Mindestens 8 Zeichen und maximal 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3504-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="b3504-114">Das Kennwort muss Zeichen aus drei der folgenden Kategorien enthalten: englische Großbuchstaben, englische Kleinbuchstaben, Zahlen und nicht alphanumerische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3504-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="b3504-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="b3504-115">-AdministratorUserName</span></span>
<span data-ttu-id="b3504-116">Administratorbenutzername für den Server.</span><span class="sxs-lookup"><span data-stu-id="b3504-116">Administrator username for the server.</span></span>
<span data-ttu-id="b3504-117">Nach dem Festlegen kann sie nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b3504-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="b3504-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3504-118">-AsJob</span></span>
<span data-ttu-id="b3504-119">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="b3504-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="b3504-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="b3504-120">-BackupRetentionDay</span></span>
<span data-ttu-id="b3504-121">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="b3504-121">Backup retention days for the server.</span></span>
<span data-ttu-id="b3504-122">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="b3504-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="b3504-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3504-123">-DefaultProfile</span></span>
<span data-ttu-id="b3504-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3504-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3504-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="b3504-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="b3504-126">Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="b3504-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="b3504-127">-Location</span><span class="sxs-lookup"><span data-stu-id="b3504-127">-Location</span></span>
<span data-ttu-id="b3504-128">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="b3504-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b3504-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="b3504-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="b3504-130">Legen Sie die minimale Version von TLS für Verbindungen mit dem Server bei aktiviertem SSL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b3504-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="b3504-131">Der Standardwert ist "TLSEnforcementDisabled.accepted"-Werte: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="b3504-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3504-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b3504-132">-Name</span></span>
<span data-ttu-id="b3504-133">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="b3504-133">The name of the server.</span></span>

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

### <span data-ttu-id="b3504-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3504-134">-NoWait</span></span>
<span data-ttu-id="b3504-135">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="b3504-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b3504-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3504-136">-ResourceGroupName</span></span>
<span data-ttu-id="b3504-137">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="b3504-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b3504-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="b3504-138">-Sku</span></span>
<span data-ttu-id="b3504-139">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b3504-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="b3504-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="b3504-140">-SslEnforcement</span></span>
<span data-ttu-id="b3504-141">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="b3504-141">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="b3504-142">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="b3504-142">-StorageAutogrow</span></span>
<span data-ttu-id="b3504-143">Aktivieren Sie "Automatisches Anwachsen des Speichers".</span><span class="sxs-lookup"><span data-stu-id="b3504-143">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="b3504-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="b3504-144">-StorageInMb</span></span>
<span data-ttu-id="b3504-145">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="b3504-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="b3504-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3504-146">-SubscriptionId</span></span>
<span data-ttu-id="b3504-147">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b3504-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b3504-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3504-148">-Tag</span></span>
<span data-ttu-id="b3504-149">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="b3504-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="b3504-150">-Version</span><span class="sxs-lookup"><span data-stu-id="b3504-150">-Version</span></span>
<span data-ttu-id="b3504-151">Serverversion.</span><span class="sxs-lookup"><span data-stu-id="b3504-151">Server version.</span></span>

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

### <span data-ttu-id="b3504-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3504-152">-Confirm</span></span>
<span data-ttu-id="b3504-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3504-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3504-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b3504-154">-WhatIf</span></span>
<span data-ttu-id="b3504-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3504-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3504-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3504-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3504-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3504-157">CommonParameters</span></span>
<span data-ttu-id="b3504-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3504-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3504-159">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3504-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3504-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3504-160">INPUTS</span></span>

## <span data-ttu-id="b3504-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3504-161">OUTPUTS</span></span>

### <span data-ttu-id="b3504-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="b3504-162">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b3504-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3504-163">NOTES</span></span>

<span data-ttu-id="b3504-164">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b3504-164">ALIASES</span></span>

## <span data-ttu-id="b3504-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3504-165">RELATED LINKS</span></span>

