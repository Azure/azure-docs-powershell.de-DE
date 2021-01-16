---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: 6c7576023e4902caacd204edc97feba0a378f63b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360266"
---
# <span data-ttu-id="db3d4-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="db3d4-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="db3d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="db3d4-103">Aktualisiert die Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="db3d4-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="db3d4-104">Verwenden Update-AzMySqlServer, wenn Sie "AdministratorLoginPassword", "SKU" usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="db3d4-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="db3d4-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db3d4-105">SYNTAX</span></span>

### <span data-ttu-id="db3d4-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="db3d4-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db3d4-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="db3d4-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db3d4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db3d4-108">DESCRIPTION</span></span>
<span data-ttu-id="db3d4-109">Aktualisiert die Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="db3d4-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="db3d4-110">Verwenden Update-AzMySqlServer, wenn Sie "AdministratorLoginPassword", "SKU" usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="db3d4-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="db3d4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db3d4-111">EXAMPLES</span></span>

### <span data-ttu-id="db3d4-112">Beispiel 1: Aktualisieren der Konfiguration von MySql nach Name</span><span class="sxs-lookup"><span data-stu-id="db3d4-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="db3d4-113">Dieses Cmdlet aktualisiert die Konfiguration von MySql nach Name.</span><span class="sxs-lookup"><span data-stu-id="db3d4-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="db3d4-114">Beispiel 2: Aktualisieren der Konfiguration von MySql nach Identität.</span><span class="sxs-lookup"><span data-stu-id="db3d4-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="db3d4-115">Diese Cmdlets aktualisieren die Konfiguration von MySql nach Identität.</span><span class="sxs-lookup"><span data-stu-id="db3d4-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="db3d4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db3d4-116">PARAMETERS</span></span>

### <span data-ttu-id="db3d4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db3d4-117">-AsJob</span></span>
<span data-ttu-id="db3d4-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="db3d4-118">Run the command as a job</span></span>

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

### <span data-ttu-id="db3d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3d4-119">-DefaultProfile</span></span>
<span data-ttu-id="db3d4-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db3d4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db3d4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db3d4-121">-InputObject</span></span>
<span data-ttu-id="db3d4-122">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="db3d4-122">Identity Parameter.</span></span>
<span data-ttu-id="db3d4-123">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="db3d4-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="db3d4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="db3d4-124">-Name</span></span>
<span data-ttu-id="db3d4-125">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="db3d4-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="db3d4-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="db3d4-126">-NoWait</span></span>
<span data-ttu-id="db3d4-127">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="db3d4-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="db3d4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db3d4-128">-ResourceGroupName</span></span>
<span data-ttu-id="db3d4-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="db3d4-129">The name of the resource group.</span></span>
<span data-ttu-id="db3d4-130">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="db3d4-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="db3d4-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db3d4-131">-ServerName</span></span>
<span data-ttu-id="db3d4-132">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="db3d4-132">The name of the server.</span></span>

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

### <span data-ttu-id="db3d4-133">-Source</span><span class="sxs-lookup"><span data-stu-id="db3d4-133">-Source</span></span>
<span data-ttu-id="db3d4-134">Quelle der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="db3d4-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="db3d4-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db3d4-135">-SubscriptionId</span></span>
<span data-ttu-id="db3d4-136">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="db3d4-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="db3d4-137">-Value</span><span class="sxs-lookup"><span data-stu-id="db3d4-137">-Value</span></span>
<span data-ttu-id="db3d4-138">Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="db3d4-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="db3d4-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db3d4-139">-Confirm</span></span>
<span data-ttu-id="db3d4-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db3d4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db3d4-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="db3d4-141">-WhatIf</span></span>
<span data-ttu-id="db3d4-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db3d4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db3d4-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db3d4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db3d4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3d4-144">CommonParameters</span></span>
<span data-ttu-id="db3d4-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db3d4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3d4-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db3d4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3d4-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db3d4-147">INPUTS</span></span>

### <span data-ttu-id="db3d4-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="db3d4-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="db3d4-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db3d4-149">OUTPUTS</span></span>

### <span data-ttu-id="db3d4-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="db3d4-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="db3d4-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="db3d4-151">NOTES</span></span>

<span data-ttu-id="db3d4-152">ALIASE</span><span class="sxs-lookup"><span data-stu-id="db3d4-152">ALIASES</span></span>

<span data-ttu-id="db3d4-153">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="db3d4-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db3d4-154">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="db3d4-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db3d4-155">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db3d4-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db3d4-156">INPUTOBJECT <IMySqlIdentity> : Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="db3d4-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="db3d4-157">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="db3d4-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="db3d4-158">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="db3d4-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="db3d4-159">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="db3d4-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="db3d4-160">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="db3d4-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db3d4-161">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="db3d4-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="db3d4-162">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="db3d4-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="db3d4-163">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="db3d4-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="db3d4-164">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="db3d4-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="db3d4-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="db3d4-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="db3d4-166">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="db3d4-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="db3d4-167">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="db3d4-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="db3d4-168">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="db3d4-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="db3d4-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="db3d4-169">RELATED LINKS</span></span>

