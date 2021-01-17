---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: 6c7576023e4902caacd204edc97feba0a378f63b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467516"
---
# <span data-ttu-id="83d08-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="83d08-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="83d08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d08-102">SYNOPSIS</span></span>
<span data-ttu-id="83d08-103">Aktualisiert die Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="83d08-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="83d08-104">Verwenden Update-AzMySqlServer, wenn Sie "AdministratorLoginPassword", "SKU" usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="83d08-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="83d08-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83d08-105">SYNTAX</span></span>

### <span data-ttu-id="83d08-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="83d08-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83d08-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="83d08-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83d08-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83d08-108">DESCRIPTION</span></span>
<span data-ttu-id="83d08-109">Aktualisiert die Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="83d08-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="83d08-110">Verwenden Update-AzMySqlServer, wenn Sie "AdministratorLoginPassword", "SKU" usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="83d08-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="83d08-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83d08-111">EXAMPLES</span></span>

### <span data-ttu-id="83d08-112">Beispiel 1: Aktualisieren der Konfiguration von MySql nach Name</span><span class="sxs-lookup"><span data-stu-id="83d08-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="83d08-113">Dieses Cmdlet aktualisiert die Konfiguration von MySql nach Name.</span><span class="sxs-lookup"><span data-stu-id="83d08-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="83d08-114">Beispiel 2: Aktualisieren der Konfiguration von MySql nach Identität.</span><span class="sxs-lookup"><span data-stu-id="83d08-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="83d08-115">Diese Cmdlets aktualisieren die Konfiguration von MySql nach Identität.</span><span class="sxs-lookup"><span data-stu-id="83d08-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="83d08-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83d08-116">PARAMETERS</span></span>

### <span data-ttu-id="83d08-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83d08-117">-AsJob</span></span>
<span data-ttu-id="83d08-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="83d08-118">Run the command as a job</span></span>

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

### <span data-ttu-id="83d08-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d08-119">-DefaultProfile</span></span>
<span data-ttu-id="83d08-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83d08-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83d08-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83d08-121">-InputObject</span></span>
<span data-ttu-id="83d08-122">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="83d08-122">Identity Parameter.</span></span>
<span data-ttu-id="83d08-123">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="83d08-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d08-124">-Name</span><span class="sxs-lookup"><span data-stu-id="83d08-124">-Name</span></span>
<span data-ttu-id="83d08-125">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="83d08-125">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d08-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="83d08-126">-NoWait</span></span>
<span data-ttu-id="83d08-127">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="83d08-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83d08-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d08-128">-ResourceGroupName</span></span>
<span data-ttu-id="83d08-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="83d08-129">The name of the resource group.</span></span>
<span data-ttu-id="83d08-130">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="83d08-130">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d08-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83d08-131">-ServerName</span></span>
<span data-ttu-id="83d08-132">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="83d08-132">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d08-133">-Source</span><span class="sxs-lookup"><span data-stu-id="83d08-133">-Source</span></span>
<span data-ttu-id="83d08-134">Quelle der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="83d08-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="83d08-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83d08-135">-SubscriptionId</span></span>
<span data-ttu-id="83d08-136">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="83d08-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d08-137">-Value</span><span class="sxs-lookup"><span data-stu-id="83d08-137">-Value</span></span>
<span data-ttu-id="83d08-138">Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="83d08-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="83d08-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83d08-139">-Confirm</span></span>
<span data-ttu-id="83d08-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83d08-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d08-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="83d08-141">-WhatIf</span></span>
<span data-ttu-id="83d08-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83d08-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d08-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83d08-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d08-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d08-144">CommonParameters</span></span>
<span data-ttu-id="83d08-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d08-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d08-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83d08-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d08-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83d08-147">INPUTS</span></span>

### <span data-ttu-id="83d08-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="83d08-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="83d08-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83d08-149">OUTPUTS</span></span>

### <span data-ttu-id="83d08-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="83d08-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="83d08-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="83d08-151">NOTES</span></span>

<span data-ttu-id="83d08-152">ALIASE</span><span class="sxs-lookup"><span data-stu-id="83d08-152">ALIASES</span></span>

<span data-ttu-id="83d08-153">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="83d08-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83d08-154">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="83d08-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83d08-155">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83d08-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83d08-156">INPUTOBJECT <IMySqlIdentity> : Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="83d08-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="83d08-157">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="83d08-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="83d08-158">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="83d08-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="83d08-159">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="83d08-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="83d08-160">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="83d08-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83d08-161">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="83d08-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="83d08-162">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="83d08-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="83d08-163">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="83d08-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="83d08-164">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="83d08-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="83d08-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="83d08-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="83d08-166">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="83d08-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="83d08-167">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="83d08-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="83d08-168">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="83d08-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="83d08-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="83d08-169">RELATED LINKS</span></span>

