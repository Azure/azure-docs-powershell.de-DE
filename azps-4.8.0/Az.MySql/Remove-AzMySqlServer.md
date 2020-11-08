---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: 86cc2a249479807adc14ad0faa4c682d1fef4725
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174617"
---
# <span data-ttu-id="456da-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="456da-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="456da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="456da-102">SYNOPSIS</span></span>
<span data-ttu-id="456da-103">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="456da-103">Deletes a server.</span></span>

## <span data-ttu-id="456da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="456da-104">SYNTAX</span></span>

### <span data-ttu-id="456da-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="456da-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="456da-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="456da-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="456da-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="456da-107">DESCRIPTION</span></span>
<span data-ttu-id="456da-108">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="456da-108">Deletes a server.</span></span>

## <span data-ttu-id="456da-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="456da-109">EXAMPLES</span></span>

### <span data-ttu-id="456da-110">Beispiel 1: Entfernen des MySQL-Servers nach ResourceGroup und Servername</span><span class="sxs-lookup"><span data-stu-id="456da-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="456da-111">Mit diesem Cmdlet wird der MySQL-Server nach ResourceGroup und Servername entfernt.</span><span class="sxs-lookup"><span data-stu-id="456da-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="456da-112">Beispiel 2: Entfernen von MySQL Server nach Identität</span><span class="sxs-lookup"><span data-stu-id="456da-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="456da-113">Diese Cmdlets entfernen den MySQL-Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="456da-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="456da-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="456da-114">PARAMETERS</span></span>

### <span data-ttu-id="456da-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="456da-115">-AsJob</span></span>
<span data-ttu-id="456da-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="456da-116">Run the command as a job</span></span>

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

### <span data-ttu-id="456da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456da-117">-DefaultProfile</span></span>
<span data-ttu-id="456da-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="456da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="456da-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="456da-119">-InputObject</span></span>
<span data-ttu-id="456da-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="456da-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="456da-121">-Name</span><span class="sxs-lookup"><span data-stu-id="456da-121">-Name</span></span>
<span data-ttu-id="456da-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="456da-122">The name of the server.</span></span>

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

### <span data-ttu-id="456da-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="456da-123">-NoWait</span></span>
<span data-ttu-id="456da-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="456da-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="456da-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="456da-125">-PassThru</span></span>
<span data-ttu-id="456da-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="456da-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="456da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456da-127">-ResourceGroupName</span></span>
<span data-ttu-id="456da-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="456da-128">The name of the resource group.</span></span>
<span data-ttu-id="456da-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="456da-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="456da-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="456da-130">-SubscriptionId</span></span>
<span data-ttu-id="456da-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="456da-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="456da-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="456da-132">-Confirm</span></span>
<span data-ttu-id="456da-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="456da-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456da-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456da-134">-WhatIf</span></span>
<span data-ttu-id="456da-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="456da-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="456da-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="456da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456da-137">CommonParameters</span></span>
<span data-ttu-id="456da-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456da-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="456da-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456da-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="456da-140">INPUTS</span></span>

### <span data-ttu-id="456da-141">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="456da-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="456da-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="456da-142">OUTPUTS</span></span>

### <span data-ttu-id="456da-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="456da-143">System.Boolean</span></span>

## <span data-ttu-id="456da-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="456da-144">NOTES</span></span>

<span data-ttu-id="456da-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="456da-145">ALIASES</span></span>

<span data-ttu-id="456da-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="456da-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="456da-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="456da-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="456da-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="456da-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="456da-149">Inputobject <IMySqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="456da-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="456da-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="456da-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="456da-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="456da-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="456da-152">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="456da-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="456da-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="456da-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="456da-154">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="456da-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="456da-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="456da-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="456da-156">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="456da-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="456da-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="456da-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="456da-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="456da-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="456da-159">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="456da-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="456da-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="456da-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="456da-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="456da-161">RELATED LINKS</span></span>

