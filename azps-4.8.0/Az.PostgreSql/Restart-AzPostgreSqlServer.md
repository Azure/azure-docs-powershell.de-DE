---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165047"
---
# <span data-ttu-id="2d72c-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="2d72c-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="2d72c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d72c-102">SYNOPSIS</span></span>
<span data-ttu-id="2d72c-103">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="2d72c-103">Restarts a server.</span></span>

## <span data-ttu-id="2d72c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d72c-104">SYNTAX</span></span>

### <span data-ttu-id="2d72c-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d72c-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2d72c-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2d72c-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d72c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d72c-107">DESCRIPTION</span></span>
<span data-ttu-id="2d72c-108">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="2d72c-108">Restarts a server.</span></span>

## <span data-ttu-id="2d72c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d72c-109">EXAMPLES</span></span>

### <span data-ttu-id="2d72c-110">Beispiel 1: Neustart des PostgreSQL-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="2d72c-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="2d72c-111">Mit diesem Cmdlet wird der PostgreSQL-Server nach Ressourcengruppe und Servername neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="2d72c-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="2d72c-112">Beispiel 2: Neustarten des PostgreSQL-Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="2d72c-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="2d72c-113">Mit diesen Cmdlets wird der PostgreSQL-Server nach Identität neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="2d72c-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="2d72c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d72c-114">PARAMETERS</span></span>

### <span data-ttu-id="2d72c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d72c-115">-AsJob</span></span>
<span data-ttu-id="2d72c-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2d72c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2d72c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d72c-117">-DefaultProfile</span></span>
<span data-ttu-id="2d72c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d72c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d72c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2d72c-119">-InputObject</span></span>
<span data-ttu-id="2d72c-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2d72c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d72c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2d72c-121">-Name</span></span>
<span data-ttu-id="2d72c-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2d72c-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d72c-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2d72c-123">-NoWait</span></span>
<span data-ttu-id="2d72c-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2d72c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2d72c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d72c-125">-PassThru</span></span>
<span data-ttu-id="2d72c-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="2d72c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2d72c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d72c-127">-ResourceGroupName</span></span>
<span data-ttu-id="2d72c-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2d72c-128">The name of the resource group.</span></span>
<span data-ttu-id="2d72c-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="2d72c-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d72c-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2d72c-130">-SubscriptionId</span></span>
<span data-ttu-id="2d72c-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2d72c-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d72c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d72c-132">-Confirm</span></span>
<span data-ttu-id="2d72c-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d72c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d72c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d72c-134">-WhatIf</span></span>
<span data-ttu-id="2d72c-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d72c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d72c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d72c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d72c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d72c-137">CommonParameters</span></span>
<span data-ttu-id="2d72c-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d72c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d72c-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d72c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d72c-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d72c-140">INPUTS</span></span>

### <span data-ttu-id="2d72c-141">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2d72c-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="2d72c-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d72c-142">OUTPUTS</span></span>

### <span data-ttu-id="2d72c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d72c-143">System.Boolean</span></span>

## <span data-ttu-id="2d72c-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d72c-144">NOTES</span></span>

<span data-ttu-id="2d72c-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="2d72c-145">ALIASES</span></span>

<span data-ttu-id="2d72c-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2d72c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2d72c-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2d72c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2d72c-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2d72c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2d72c-149">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2d72c-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2d72c-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d72c-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2d72c-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2d72c-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2d72c-152">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="2d72c-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2d72c-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2d72c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2d72c-154">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="2d72c-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2d72c-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2d72c-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2d72c-156">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="2d72c-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="2d72c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="2d72c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2d72c-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2d72c-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2d72c-159">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2d72c-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2d72c-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2d72c-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2d72c-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d72c-161">RELATED LINKS</span></span>

