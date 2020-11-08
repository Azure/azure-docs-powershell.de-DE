---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: c4eb244dd2d1a0d685bf18f39deedf9992b5597e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178605"
---
# <span data-ttu-id="6585b-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6585b-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="6585b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6585b-102">SYNOPSIS</span></span>
<span data-ttu-id="6585b-103">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="6585b-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="6585b-104">Verwenden Sie stattdessen Update-AzMySqlServer, wenn Sie AdministratorLoginPassword, SKU usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6585b-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6585b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6585b-105">SYNTAX</span></span>

### <span data-ttu-id="6585b-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="6585b-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6585b-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6585b-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6585b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6585b-108">DESCRIPTION</span></span>
<span data-ttu-id="6585b-109">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="6585b-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="6585b-110">Verwenden Sie stattdessen Update-AzMySqlServer, wenn Sie AdministratorLoginPassword, SKU usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6585b-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6585b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6585b-111">EXAMPLES</span></span>

### <span data-ttu-id="6585b-112">Beispiel 1: Aktualisieren der MySQL-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="6585b-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="6585b-113">Dieses Cmdlet aktualisiert die MySQL-Konfiguration mit dem Namen.</span><span class="sxs-lookup"><span data-stu-id="6585b-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="6585b-114">Beispiel 2: Aktualisieren der MySQL-Konfiguration nach Identität.</span><span class="sxs-lookup"><span data-stu-id="6585b-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="6585b-115">Diese Cmdlets aktualisieren die MySQL-Konfiguration nach Identität.</span><span class="sxs-lookup"><span data-stu-id="6585b-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="6585b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6585b-116">PARAMETERS</span></span>

### <span data-ttu-id="6585b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6585b-117">-AsJob</span></span>
<span data-ttu-id="6585b-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6585b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6585b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6585b-119">-DefaultProfile</span></span>
<span data-ttu-id="6585b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6585b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6585b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6585b-121">-InputObject</span></span>
<span data-ttu-id="6585b-122">Parameter Identity.</span><span class="sxs-lookup"><span data-stu-id="6585b-122">Identity Parameter.</span></span>
<span data-ttu-id="6585b-123">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6585b-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6585b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6585b-124">-Name</span></span>
<span data-ttu-id="6585b-125">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6585b-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="6585b-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6585b-126">-NoWait</span></span>
<span data-ttu-id="6585b-127">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6585b-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6585b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6585b-128">-ResourceGroupName</span></span>
<span data-ttu-id="6585b-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6585b-129">The name of the resource group.</span></span>
<span data-ttu-id="6585b-130">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6585b-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6585b-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="6585b-131">-ServerName</span></span>
<span data-ttu-id="6585b-132">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="6585b-132">The name of the server.</span></span>

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

### <span data-ttu-id="6585b-133">-Source</span><span class="sxs-lookup"><span data-stu-id="6585b-133">-Source</span></span>
<span data-ttu-id="6585b-134">Die Quelle der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6585b-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="6585b-135">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6585b-135">-SubscriptionId</span></span>
<span data-ttu-id="6585b-136">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6585b-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6585b-137">-Wert</span><span class="sxs-lookup"><span data-stu-id="6585b-137">-Value</span></span>
<span data-ttu-id="6585b-138">Der Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6585b-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="6585b-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6585b-139">-Confirm</span></span>
<span data-ttu-id="6585b-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6585b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6585b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6585b-141">-WhatIf</span></span>
<span data-ttu-id="6585b-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6585b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6585b-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6585b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6585b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6585b-144">CommonParameters</span></span>
<span data-ttu-id="6585b-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6585b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6585b-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6585b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6585b-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6585b-147">INPUTS</span></span>

### <span data-ttu-id="6585b-148">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6585b-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="6585b-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6585b-149">OUTPUTS</span></span>

### <span data-ttu-id="6585b-150">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="6585b-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="6585b-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="6585b-151">NOTES</span></span>

<span data-ttu-id="6585b-152">Aliase</span><span class="sxs-lookup"><span data-stu-id="6585b-152">ALIASES</span></span>

<span data-ttu-id="6585b-153">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6585b-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6585b-154">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6585b-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6585b-155">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="6585b-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6585b-156">Inputobject <IMySqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="6585b-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="6585b-157">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6585b-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6585b-158">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6585b-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6585b-159">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="6585b-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6585b-160">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="6585b-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6585b-161">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="6585b-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6585b-162">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6585b-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6585b-163">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6585b-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="6585b-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="6585b-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6585b-165">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="6585b-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6585b-166">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6585b-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6585b-167">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6585b-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6585b-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6585b-168">RELATED LINKS</span></span>

