---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179104"
---
# <span data-ttu-id="af6a8-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="af6a8-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="af6a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="af6a8-103">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="af6a8-103">Restarts a server.</span></span>

## <span data-ttu-id="af6a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af6a8-104">SYNTAX</span></span>

### <span data-ttu-id="af6a8-105">Servername (Standard)</span><span class="sxs-lookup"><span data-stu-id="af6a8-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="af6a8-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="af6a8-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af6a8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af6a8-107">DESCRIPTION</span></span>
<span data-ttu-id="af6a8-108">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="af6a8-108">Restarts a server.</span></span>

## <span data-ttu-id="af6a8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af6a8-109">EXAMPLES</span></span>

### <span data-ttu-id="af6a8-110">Beispiel 1: Erneutes Starten eines MariaDB</span><span class="sxs-lookup"><span data-stu-id="af6a8-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="af6a8-111">Mit diesem Befehl wird ein MariaDB neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="af6a8-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="af6a8-112">Beispiel 2: Erneutes Starten eines MariaDB</span><span class="sxs-lookup"><span data-stu-id="af6a8-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="af6a8-113">Mit diesem Befehl wird ein MariaDB neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="af6a8-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="af6a8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="af6a8-114">PARAMETERS</span></span>

### <span data-ttu-id="af6a8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af6a8-115">-AsJob</span></span>
<span data-ttu-id="af6a8-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="af6a8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="af6a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af6a8-117">-DefaultProfile</span></span>
<span data-ttu-id="af6a8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af6a8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af6a8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="af6a8-119">-InputObject</span></span>
<span data-ttu-id="af6a8-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="af6a8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af6a8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="af6a8-121">-Name</span></span>
<span data-ttu-id="af6a8-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="af6a8-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6a8-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="af6a8-123">-NoWait</span></span>
<span data-ttu-id="af6a8-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="af6a8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="af6a8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af6a8-125">-PassThru</span></span>
<span data-ttu-id="af6a8-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="af6a8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="af6a8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af6a8-127">-ResourceGroupName</span></span>
<span data-ttu-id="af6a8-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="af6a8-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="af6a8-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="af6a8-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6a8-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="af6a8-130">-SubscriptionId</span></span>
<span data-ttu-id="af6a8-131">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="af6a8-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6a8-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="af6a8-132">-Confirm</span></span>
<span data-ttu-id="af6a8-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af6a8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af6a8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af6a8-134">-WhatIf</span></span>
<span data-ttu-id="af6a8-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af6a8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af6a8-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af6a8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af6a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af6a8-137">CommonParameters</span></span>
<span data-ttu-id="af6a8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af6a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af6a8-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af6a8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af6a8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af6a8-140">INPUTS</span></span>

### <span data-ttu-id="af6a8-141">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="af6a8-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="af6a8-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af6a8-142">OUTPUTS</span></span>

### <span data-ttu-id="af6a8-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af6a8-143">System.Boolean</span></span>

## <span data-ttu-id="af6a8-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="af6a8-144">NOTES</span></span>

<span data-ttu-id="af6a8-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="af6a8-145">ALIASES</span></span>

<span data-ttu-id="af6a8-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af6a8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af6a8-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="af6a8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af6a8-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="af6a8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af6a8-149">Inputobject <IMariaDbIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="af6a8-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="af6a8-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="af6a8-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="af6a8-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="af6a8-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="af6a8-152">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="af6a8-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="af6a8-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="af6a8-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="af6a8-154">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="af6a8-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="af6a8-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="af6a8-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="af6a8-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="af6a8-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="af6a8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="af6a8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="af6a8-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="af6a8-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="af6a8-159">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="af6a8-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="af6a8-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="af6a8-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="af6a8-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af6a8-161">RELATED LINKS</span></span>

