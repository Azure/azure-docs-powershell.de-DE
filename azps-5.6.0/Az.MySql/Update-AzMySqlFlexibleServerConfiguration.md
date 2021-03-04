---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 98e476b2a1732d2c984d200265d817c3ff6d71a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927008"
---
# <span data-ttu-id="cd5e8-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd5e8-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="cd5e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5e8-103">Aktualisiert Informationen zu einer Konfiguration eines flexiblen MySQL-Servers.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="cd5e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd5e8-104">SYNTAX</span></span>

### <span data-ttu-id="cd5e8-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd5e8-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd5e8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cd5e8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd5e8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd5e8-107">DESCRIPTION</span></span>
<span data-ttu-id="cd5e8-108">Aktualisiert Informationen zu einer Konfiguration eines flexiblen MySQL-Servers.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="cd5e8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd5e8-109">EXAMPLES</span></span>

### <span data-ttu-id="cd5e8-110">Beispiel 1: Aktualisieren der MySql-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="cd5e8-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="cd5e8-111">Dieses Cmdlet aktualisiert die MySql-Konfiguration nach Name.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="cd5e8-112">Beispiel 2: Aktualisieren der MySql-Konfiguration nach Identität.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="cd5e8-113">Diese Cmdlets aktualisieren die MySql-Konfiguration nach Identität.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="cd5e8-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cd5e8-114">PARAMETERS</span></span>

### <span data-ttu-id="cd5e8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd5e8-115">-AsJob</span></span>
<span data-ttu-id="cd5e8-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="cd5e8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cd5e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5e8-117">-DefaultProfile</span></span>
<span data-ttu-id="cd5e8-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd5e8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd5e8-119">-InputObject</span></span>
<span data-ttu-id="cd5e8-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd5e8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cd5e8-121">-Name</span></span>
<span data-ttu-id="cd5e8-122">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="cd5e8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cd5e8-123">-NoWait</span></span>
<span data-ttu-id="cd5e8-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="cd5e8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd5e8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd5e8-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd5e8-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-126">The name of the resource group.</span></span>
<span data-ttu-id="cd5e8-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cd5e8-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="cd5e8-128">-ServerName</span></span>
<span data-ttu-id="cd5e8-129">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-129">The name of the server.</span></span>

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

### <span data-ttu-id="cd5e8-130">-Source</span><span class="sxs-lookup"><span data-stu-id="cd5e8-130">-Source</span></span>
<span data-ttu-id="cd5e8-131">Die Quelle des Aktualisierungswerts.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-131">The source of the updating value.</span></span>
<span data-ttu-id="cd5e8-132">Der Standardwert ist Benutzerüberschreibung</span><span class="sxs-lookup"><span data-stu-id="cd5e8-132">The default value is user-override</span></span>

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

### <span data-ttu-id="cd5e8-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd5e8-133">-SubscriptionId</span></span>
<span data-ttu-id="cd5e8-134">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cd5e8-135">-Wert</span><span class="sxs-lookup"><span data-stu-id="cd5e8-135">-Value</span></span>
<span data-ttu-id="cd5e8-136">Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="cd5e8-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd5e8-137">-Confirm</span></span>
<span data-ttu-id="cd5e8-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd5e8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd5e8-139">-WhatIf</span></span>
<span data-ttu-id="cd5e8-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd5e8-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd5e8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5e8-142">CommonParameters</span></span>
<span data-ttu-id="cd5e8-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5e8-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd5e8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5e8-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd5e8-145">INPUTS</span></span>

### <span data-ttu-id="cd5e8-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cd5e8-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="cd5e8-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd5e8-147">OUTPUTS</span></span>

### <span data-ttu-id="cd5e8-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="cd5e8-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="cd5e8-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cd5e8-149">NOTES</span></span>

<span data-ttu-id="cd5e8-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cd5e8-150">ALIASES</span></span>

<span data-ttu-id="cd5e8-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cd5e8-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd5e8-152">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd5e8-153">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd5e8-154">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="cd5e8-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd5e8-155">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cd5e8-156">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cd5e8-157">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cd5e8-158">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="cd5e8-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd5e8-159">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="cd5e8-160">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cd5e8-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cd5e8-162">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="cd5e8-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cd5e8-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cd5e8-165">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cd5e8-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cd5e8-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cd5e8-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cd5e8-167">RELATED LINKS</span></span>

