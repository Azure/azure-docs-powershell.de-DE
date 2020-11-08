---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178846"
---
# <span data-ttu-id="3ac62-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3ac62-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="3ac62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ac62-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac62-103">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="3ac62-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="3ac62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ac62-104">SYNTAX</span></span>

### <span data-ttu-id="3ac62-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ac62-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3ac62-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3ac62-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ac62-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ac62-107">DESCRIPTION</span></span>
<span data-ttu-id="3ac62-108">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="3ac62-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="3ac62-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ac62-109">EXAMPLES</span></span>

### <span data-ttu-id="3ac62-110">Beispiel 1: Entfernen einer virtuellen Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="3ac62-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="3ac62-111">Mit diesem Befehl wird eine virtuelle Netzwerkregel entfernt.</span><span class="sxs-lookup"><span data-stu-id="3ac62-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="3ac62-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ac62-112">PARAMETERS</span></span>

### <span data-ttu-id="3ac62-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ac62-113">-AsJob</span></span>
<span data-ttu-id="3ac62-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3ac62-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3ac62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac62-115">-DefaultProfile</span></span>
<span data-ttu-id="3ac62-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ac62-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac62-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3ac62-117">-InputObject</span></span>
<span data-ttu-id="3ac62-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3ac62-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac62-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3ac62-119">-Name</span></span>
<span data-ttu-id="3ac62-120">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3ac62-120">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="3ac62-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3ac62-121">-NoWait</span></span>
<span data-ttu-id="3ac62-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3ac62-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3ac62-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ac62-123">-PassThru</span></span>
<span data-ttu-id="3ac62-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="3ac62-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3ac62-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac62-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ac62-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="3ac62-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3ac62-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="3ac62-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3ac62-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="3ac62-128">-ServerName</span></span>
<span data-ttu-id="3ac62-129">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3ac62-129">The name of the server.</span></span>

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

### <span data-ttu-id="3ac62-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3ac62-130">-SubscriptionId</span></span>
<span data-ttu-id="3ac62-131">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3ac62-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3ac62-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ac62-132">-Confirm</span></span>
<span data-ttu-id="3ac62-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ac62-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ac62-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ac62-134">-WhatIf</span></span>
<span data-ttu-id="3ac62-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ac62-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ac62-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ac62-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ac62-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac62-137">CommonParameters</span></span>
<span data-ttu-id="3ac62-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ac62-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac62-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ac62-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac62-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ac62-140">INPUTS</span></span>

### <span data-ttu-id="3ac62-141">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="3ac62-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="3ac62-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ac62-142">OUTPUTS</span></span>

### <span data-ttu-id="3ac62-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ac62-143">System.Boolean</span></span>

## <span data-ttu-id="3ac62-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ac62-144">NOTES</span></span>

<span data-ttu-id="3ac62-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="3ac62-145">ALIASES</span></span>

<span data-ttu-id="3ac62-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3ac62-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ac62-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3ac62-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ac62-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="3ac62-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ac62-149">Inputobject <IMariaDbIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="3ac62-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ac62-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="3ac62-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3ac62-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3ac62-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3ac62-152">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="3ac62-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3ac62-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="3ac62-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ac62-154">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="3ac62-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3ac62-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="3ac62-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3ac62-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="3ac62-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3ac62-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="3ac62-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3ac62-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3ac62-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3ac62-159">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3ac62-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="3ac62-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3ac62-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3ac62-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ac62-161">RELATED LINKS</span></span>

