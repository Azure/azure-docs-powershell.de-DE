---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/remove-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: b4d9553fe72c1179d82645606515165a3104abf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919456"
---
# <span data-ttu-id="3a8cf-101">Remove-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="3a8cf-101">Remove-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="3a8cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8cf-103">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-103">Deletes a server.</span></span>

## <span data-ttu-id="3a8cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a8cf-104">SYNTAX</span></span>

### <span data-ttu-id="3a8cf-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a8cf-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3a8cf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a8cf-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a8cf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a8cf-107">DESCRIPTION</span></span>
<span data-ttu-id="3a8cf-108">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-108">Deletes a server.</span></span>

## <span data-ttu-id="3a8cf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a8cf-109">EXAMPLES</span></span>

### <span data-ttu-id="3a8cf-110">Beispiel 1: Entfernen des PostgreSql-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="3a8cf-110">Example 1: Remove PostgreSql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

```

<span data-ttu-id="3a8cf-111">Dieses Cmdlet entfernt den PostgreSql-Server nach resourceGroup- und Servername.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-111">This cmdlet removes PostgreSql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="3a8cf-112">Beispiel 2: Entfernen des PostgreSql-Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="3a8cf-112">Example 2: Remove PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Remove-AzPostgreSqlFlexibleServer -InputObject $ID
 
```

<span data-ttu-id="3a8cf-113">Diese Cmdlets entfernen den PostgreSql-Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-113">These cmdlets remove PostgreSql server by identity.</span></span>

## <span data-ttu-id="3a8cf-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3a8cf-114">PARAMETERS</span></span>

### <span data-ttu-id="3a8cf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a8cf-115">-AsJob</span></span>
<span data-ttu-id="3a8cf-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3a8cf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3a8cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8cf-117">-DefaultProfile</span></span>
<span data-ttu-id="3a8cf-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a8cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a8cf-119">-InputObject</span></span>
<span data-ttu-id="3a8cf-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a8cf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3a8cf-121">-Name</span></span>
<span data-ttu-id="3a8cf-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8cf-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a8cf-123">-NoWait</span></span>
<span data-ttu-id="3a8cf-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3a8cf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a8cf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a8cf-125">-PassThru</span></span>
<span data-ttu-id="3a8cf-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3a8cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a8cf-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-128">The name of the resource group.</span></span>
<span data-ttu-id="3a8cf-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3a8cf-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a8cf-130">-SubscriptionId</span></span>
<span data-ttu-id="3a8cf-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3a8cf-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a8cf-132">-Confirm</span></span>
<span data-ttu-id="3a8cf-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8cf-134">-WhatIf</span></span>
<span data-ttu-id="3a8cf-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a8cf-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8cf-137">CommonParameters</span></span>
<span data-ttu-id="3a8cf-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8cf-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a8cf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8cf-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a8cf-140">INPUTS</span></span>

### <span data-ttu-id="3a8cf-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3a8cf-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="3a8cf-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a8cf-142">OUTPUTS</span></span>

### <span data-ttu-id="3a8cf-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a8cf-143">System.Boolean</span></span>

## <span data-ttu-id="3a8cf-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3a8cf-144">NOTES</span></span>

<span data-ttu-id="3a8cf-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3a8cf-145">ALIASES</span></span>

<span data-ttu-id="3a8cf-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3a8cf-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a8cf-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a8cf-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a8cf-149">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="3a8cf-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a8cf-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3a8cf-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3a8cf-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3a8cf-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="3a8cf-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a8cf-154">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3a8cf-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3a8cf-156">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="3a8cf-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3a8cf-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3a8cf-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3a8cf-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3a8cf-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3a8cf-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3a8cf-161">RELATED LINKS</span></span>

