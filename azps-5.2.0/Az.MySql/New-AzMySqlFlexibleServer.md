---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 1dbd998cdafc92de6541e25c2cb2bf6477e2d5b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292505"
---
# <span data-ttu-id="ac86f-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="ac86f-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="ac86f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac86f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac86f-103">Erstellt einen neuen flexiblen MySQL-Server.</span><span class="sxs-lookup"><span data-stu-id="ac86f-103">Creates a new MySQL flexible server</span></span>

## <span data-ttu-id="ac86f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac86f-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> -AdministratorUserName <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-Location <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac86f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac86f-105">DESCRIPTION</span></span>
<span data-ttu-id="ac86f-106">Erstellt einen neuen Server.</span><span class="sxs-lookup"><span data-stu-id="ac86f-106">Creates a new server.</span></span>

## <span data-ttu-id="ac86f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac86f-107">EXAMPLES</span></span>

### <span data-ttu-id="ac86f-108">Beispiel 1: Erstellen eines neuen flexiblen MySql-Servers</span><span class="sxs-lookup"><span data-stu-id="ac86f-108">Example 1: Create a new MySql flexible server</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      10240                  Standard_B1ms   Burstable
```



### <span data-ttu-id="ac86f-109">Beispiel 2: Erstellen eines neuen flexiblen MySql-Servers mit Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="ac86f-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-AdministratorUserName mysqltest -AdministratorLoginPassword $password

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      131072                  Standard_B1ms   Burstable
```

<span data-ttu-id="ac86f-110">Erstellen Sie einen MySql-Server mit Standardwerten.</span><span class="sxs-lookup"><span data-stu-id="ac86f-110">Create MySql server with default values.</span></span>
<span data-ttu-id="ac86f-111">Die Standardwerte für den Speicherort sind "USA 2", "SKU" ist Standard_B1ms, die SKU-Stufe ist "Burstable", und die Speichergröße ist "10GiB".</span><span class="sxs-lookup"><span data-stu-id="ac86f-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>

## <span data-ttu-id="ac86f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac86f-112">PARAMETERS</span></span>

### <span data-ttu-id="ac86f-113">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ac86f-113">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ac86f-114">Das Kennwort des Administrators.</span><span class="sxs-lookup"><span data-stu-id="ac86f-114">The password of the administrator.</span></span>
<span data-ttu-id="ac86f-115">Mindestens 8 Zeichen und maximal 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ac86f-115">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="ac86f-116">Das Kennwort muss Zeichen aus drei der folgenden Kategorien enthalten: englische Großbuchstaben, englische Kleinbuchstaben, Zahlen und nicht alphanumerische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ac86f-116">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="ac86f-117">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="ac86f-117">-AdministratorUserName</span></span>
<span data-ttu-id="ac86f-118">Administratorbenutzername für den Server.</span><span class="sxs-lookup"><span data-stu-id="ac86f-118">Administrator username for the server.</span></span>
<span data-ttu-id="ac86f-119">Nach dem Festlegen kann es nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ac86f-119">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="ac86f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac86f-120">-AsJob</span></span>
<span data-ttu-id="ac86f-121">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="ac86f-121">Run the command as a job.</span></span>

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

### <span data-ttu-id="ac86f-122">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ac86f-122">-BackupRetentionDay</span></span>
<span data-ttu-id="ac86f-123">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="ac86f-123">Backup retention days for the server.</span></span>
<span data-ttu-id="ac86f-124">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="ac86f-124">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="ac86f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac86f-125">-DefaultProfile</span></span>
<span data-ttu-id="ac86f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac86f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac86f-127">-Location</span><span class="sxs-lookup"><span data-stu-id="ac86f-127">-Location</span></span>
<span data-ttu-id="ac86f-128">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="ac86f-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ac86f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ac86f-129">-Name</span></span>
<span data-ttu-id="ac86f-130">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="ac86f-130">The name of the server.</span></span>

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

### <span data-ttu-id="ac86f-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ac86f-131">-NoWait</span></span>
<span data-ttu-id="ac86f-132">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="ac86f-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ac86f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac86f-133">-ResourceGroupName</span></span>
<span data-ttu-id="ac86f-134">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="ac86f-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ac86f-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="ac86f-135">-Sku</span></span>
<span data-ttu-id="ac86f-136">Der Name der SKU, normalerweise Stufen + Familie + Kerne, z. B. Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="ac86f-136">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="ac86f-137">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ac86f-137">-SkuTier</span></span>
<span data-ttu-id="ac86f-138">Rechenstufe des Servers.</span><span class="sxs-lookup"><span data-stu-id="ac86f-138">Compute tier of the server.</span></span>
<span data-ttu-id="ac86f-139">Akzeptierte Werte: "Burstable", "GeneralPurpose", "Memory Optimized".</span><span class="sxs-lookup"><span data-stu-id="ac86f-139">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="ac86f-140">Standard: Auftplatzierbar.</span><span class="sxs-lookup"><span data-stu-id="ac86f-140">Default: Burstable.</span></span>

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

### <span data-ttu-id="ac86f-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ac86f-141">-StorageInMb</span></span>
<span data-ttu-id="ac86f-142">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="ac86f-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="ac86f-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac86f-143">-SubscriptionId</span></span>
<span data-ttu-id="ac86f-144">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ac86f-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ac86f-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac86f-145">-Tag</span></span>
<span data-ttu-id="ac86f-146">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="ac86f-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="ac86f-147">-Version</span><span class="sxs-lookup"><span data-stu-id="ac86f-147">-Version</span></span>
<span data-ttu-id="ac86f-148">Serverversion.</span><span class="sxs-lookup"><span data-stu-id="ac86f-148">Server version.</span></span>

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

### <span data-ttu-id="ac86f-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac86f-149">-Confirm</span></span>
<span data-ttu-id="ac86f-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac86f-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac86f-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ac86f-151">-WhatIf</span></span>
<span data-ttu-id="ac86f-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac86f-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac86f-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac86f-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac86f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac86f-154">CommonParameters</span></span>
<span data-ttu-id="ac86f-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac86f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac86f-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac86f-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac86f-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac86f-157">INPUTS</span></span>

## <span data-ttu-id="ac86f-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac86f-158">OUTPUTS</span></span>

### <span data-ttu-id="ac86f-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ac86f-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="ac86f-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ac86f-160">NOTES</span></span>

<span data-ttu-id="ac86f-161">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ac86f-161">ALIASES</span></span>

## <span data-ttu-id="ac86f-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ac86f-162">RELATED LINKS</span></span>

