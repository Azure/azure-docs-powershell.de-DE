---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177772"
---
# <span data-ttu-id="dc6ab-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dc6ab-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="dc6ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6ab-103">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="dc6ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc6ab-104">SYNTAX</span></span>

### <span data-ttu-id="dc6ab-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc6ab-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dc6ab-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc6ab-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dc6ab-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc6ab-107">DESCRIPTION</span></span>
<span data-ttu-id="dc6ab-108">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="dc6ab-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc6ab-109">EXAMPLES</span></span>

### <span data-ttu-id="dc6ab-110">Beispiel 1: Entfernen der virtuellen Netzwerkregel des PostgreSQL-Servers nach Namen</span><span class="sxs-lookup"><span data-stu-id="dc6ab-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="dc6ab-111">Dieses Cmdlet entfernt die virtuelle PostgreSQL-Server-Netzwerkregel nach Namen.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="dc6ab-112">Beispiel 2: Entfernen der virtuellen Netzwerkregel des PostgreSQL-Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="dc6ab-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="dc6ab-113">Mit diesen Cmdlets wird die virtuelle Netzwerkregel des PostgreSQL-Servers nach Identität entfernt.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="dc6ab-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc6ab-114">PARAMETERS</span></span>

### <span data-ttu-id="dc6ab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc6ab-115">-AsJob</span></span>
<span data-ttu-id="dc6ab-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="dc6ab-116">Run the command as a job</span></span>

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

### <span data-ttu-id="dc6ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6ab-117">-DefaultProfile</span></span>
<span data-ttu-id="dc6ab-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc6ab-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc6ab-119">-InputObject</span></span>
<span data-ttu-id="dc6ab-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ab-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dc6ab-121">-Name</span></span>
<span data-ttu-id="dc6ab-122">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ab-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="dc6ab-123">-NoWait</span></span>
<span data-ttu-id="dc6ab-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="dc6ab-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dc6ab-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc6ab-125">-PassThru</span></span>
<span data-ttu-id="dc6ab-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="dc6ab-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dc6ab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc6ab-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc6ab-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-128">The name of the resource group.</span></span>
<span data-ttu-id="dc6ab-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ab-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="dc6ab-130">-ServerName</span></span>
<span data-ttu-id="dc6ab-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ab-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="dc6ab-132">-SubscriptionId</span></span>
<span data-ttu-id="dc6ab-133">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ab-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc6ab-134">-Confirm</span></span>
<span data-ttu-id="dc6ab-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc6ab-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc6ab-136">-WhatIf</span></span>
<span data-ttu-id="dc6ab-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc6ab-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc6ab-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6ab-139">CommonParameters</span></span>
<span data-ttu-id="dc6ab-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6ab-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6ab-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc6ab-142">INPUTS</span></span>

### <span data-ttu-id="dc6ab-143">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="dc6ab-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="dc6ab-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc6ab-144">OUTPUTS</span></span>

### <span data-ttu-id="dc6ab-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc6ab-145">System.Boolean</span></span>

## <span data-ttu-id="dc6ab-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc6ab-146">NOTES</span></span>

<span data-ttu-id="dc6ab-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="dc6ab-147">ALIASES</span></span>

<span data-ttu-id="dc6ab-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc6ab-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc6ab-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc6ab-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc6ab-151">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="dc6ab-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc6ab-152">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dc6ab-153">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dc6ab-154">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dc6ab-155">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="dc6ab-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc6ab-156">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dc6ab-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dc6ab-158">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="dc6ab-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dc6ab-160">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dc6ab-161">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dc6ab-162">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dc6ab-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc6ab-163">RELATED LINKS</span></span>

