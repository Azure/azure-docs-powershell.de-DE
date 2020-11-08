---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restart-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
ms.openlocfilehash: ac222556eb39d0bf8535921265721f54e84f4eae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008377"
---
# <span data-ttu-id="91f45-101">Restart-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="91f45-101">Restart-AzMySqlServer</span></span>

## <span data-ttu-id="91f45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91f45-102">SYNOPSIS</span></span>
<span data-ttu-id="91f45-103">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="91f45-103">Restarts a server.</span></span>

## <span data-ttu-id="91f45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91f45-104">SYNTAX</span></span>

### <span data-ttu-id="91f45-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="91f45-105">Restart (Default)</span></span>
```
Restart-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="91f45-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="91f45-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="91f45-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91f45-107">DESCRIPTION</span></span>
<span data-ttu-id="91f45-108">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="91f45-108">Restarts a server.</span></span>

## <span data-ttu-id="91f45-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91f45-109">EXAMPLES</span></span>

### <span data-ttu-id="91f45-110">Beispiel 1: Neustarten von MySQL Server nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="91f45-110">Example 1: Restart MySql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="91f45-111">Mit diesem Cmdlet wird der MySQL-Server nach Ressourcengruppe und Servername neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="91f45-111">This cmdlet restarts MySql server by resource group and server name.</span></span>

### <span data-ttu-id="91f45-112">Beispiel 2: Neustarten von MySQL Server nach Identität</span><span class="sxs-lookup"><span data-stu-id="91f45-112">Example 2: Restart MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/restart"
PS C:\> Restart-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="91f45-113">Mit diesen Cmdlets wird der MySQL-Server nach Identität neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="91f45-113">These cmdlets restart MySql server by identity.</span></span>

## <span data-ttu-id="91f45-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="91f45-114">PARAMETERS</span></span>

### <span data-ttu-id="91f45-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91f45-115">-AsJob</span></span>
<span data-ttu-id="91f45-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="91f45-116">Run the command as a job</span></span>

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

### <span data-ttu-id="91f45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f45-117">-DefaultProfile</span></span>
<span data-ttu-id="91f45-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91f45-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91f45-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91f45-119">-InputObject</span></span>
<span data-ttu-id="91f45-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="91f45-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91f45-121">-Name</span><span class="sxs-lookup"><span data-stu-id="91f45-121">-Name</span></span>
<span data-ttu-id="91f45-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="91f45-122">The name of the server.</span></span>

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

### <span data-ttu-id="91f45-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="91f45-123">-NoWait</span></span>
<span data-ttu-id="91f45-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="91f45-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="91f45-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91f45-125">-PassThru</span></span>
<span data-ttu-id="91f45-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="91f45-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="91f45-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f45-127">-ResourceGroupName</span></span>
<span data-ttu-id="91f45-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91f45-128">The name of the resource group.</span></span>
<span data-ttu-id="91f45-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="91f45-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="91f45-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="91f45-130">-SubscriptionId</span></span>
<span data-ttu-id="91f45-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="91f45-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="91f45-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91f45-132">-Confirm</span></span>
<span data-ttu-id="91f45-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91f45-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f45-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f45-134">-WhatIf</span></span>
<span data-ttu-id="91f45-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91f45-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f45-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91f45-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f45-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f45-137">CommonParameters</span></span>
<span data-ttu-id="91f45-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f45-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f45-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91f45-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f45-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91f45-140">INPUTS</span></span>

### <span data-ttu-id="91f45-141">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="91f45-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="91f45-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91f45-142">OUTPUTS</span></span>

### <span data-ttu-id="91f45-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91f45-143">System.Boolean</span></span>

## <span data-ttu-id="91f45-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="91f45-144">NOTES</span></span>

<span data-ttu-id="91f45-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="91f45-145">ALIASES</span></span>

<span data-ttu-id="91f45-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91f45-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91f45-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91f45-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91f45-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="91f45-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91f45-149">Inputobject <IMySqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="91f45-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91f45-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="91f45-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="91f45-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="91f45-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="91f45-152">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="91f45-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="91f45-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="91f45-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91f45-154">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="91f45-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="91f45-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91f45-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="91f45-156">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="91f45-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="91f45-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="91f45-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="91f45-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="91f45-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="91f45-159">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="91f45-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="91f45-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="91f45-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="91f45-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91f45-161">RELATED LINKS</span></span>

