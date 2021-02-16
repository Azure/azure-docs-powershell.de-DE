---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
ms.openlocfilehash: c495cb1372735c856224d45010728f264f73c252
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170351"
---
# <span data-ttu-id="56bab-101">Remove-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="56bab-101">Remove-AzMariaDbServer</span></span>

## <span data-ttu-id="56bab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56bab-102">SYNOPSIS</span></span>
<span data-ttu-id="56bab-103">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="56bab-103">Deletes a server.</span></span>

## <span data-ttu-id="56bab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56bab-104">SYNTAX</span></span>

### <span data-ttu-id="56bab-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="56bab-105">Delete (Default)</span></span>
```
Remove-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56bab-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56bab-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56bab-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56bab-107">DESCRIPTION</span></span>
<span data-ttu-id="56bab-108">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="56bab-108">Deletes a server.</span></span>

## <span data-ttu-id="56bab-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56bab-109">EXAMPLES</span></span>

### <span data-ttu-id="56bab-110">Beispiel 1: Entfernen einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="56bab-110">Example 1: Remove a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbServer -Name mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="56bab-111">Mit diesem Befehl wird eine MariaDB entfernt.</span><span class="sxs-lookup"><span data-stu-id="56bab-111">This command removes a MariaDB.</span></span>

### <span data-ttu-id="56bab-112">Beispiel 2: Entfernen einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="56bab-112">Example 2: Remove a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-bc-t01 -ResourceGroupName mariadb-test-qu5ov0 | Remove-AzMariaDbServer

```

<span data-ttu-id="56bab-113">Mit diesem Befehl wird eine MariaDB entfernt.</span><span class="sxs-lookup"><span data-stu-id="56bab-113">This command removes a MariaDB.</span></span>

## <span data-ttu-id="56bab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56bab-114">PARAMETERS</span></span>

### <span data-ttu-id="56bab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56bab-115">-AsJob</span></span>
<span data-ttu-id="56bab-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="56bab-116">Run the command as a job</span></span>

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

### <span data-ttu-id="56bab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bab-117">-DefaultProfile</span></span>
<span data-ttu-id="56bab-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56bab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56bab-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56bab-119">-InputObject</span></span>
<span data-ttu-id="56bab-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="56bab-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56bab-121">-Name</span><span class="sxs-lookup"><span data-stu-id="56bab-121">-Name</span></span>
<span data-ttu-id="56bab-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="56bab-122">The name of the server.</span></span>

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

### <span data-ttu-id="56bab-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="56bab-123">-NoWait</span></span>
<span data-ttu-id="56bab-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="56bab-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="56bab-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56bab-125">-PassThru</span></span>
<span data-ttu-id="56bab-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="56bab-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="56bab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56bab-127">-ResourceGroupName</span></span>
<span data-ttu-id="56bab-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="56bab-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="56bab-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="56bab-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="56bab-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56bab-130">-SubscriptionId</span></span>
<span data-ttu-id="56bab-131">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56bab-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="56bab-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56bab-132">-Confirm</span></span>
<span data-ttu-id="56bab-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56bab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56bab-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="56bab-134">-WhatIf</span></span>
<span data-ttu-id="56bab-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56bab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56bab-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56bab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56bab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bab-137">CommonParameters</span></span>
<span data-ttu-id="56bab-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56bab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bab-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56bab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bab-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56bab-140">INPUTS</span></span>

### <span data-ttu-id="56bab-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="56bab-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="56bab-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56bab-142">OUTPUTS</span></span>

### <span data-ttu-id="56bab-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="56bab-143">System.Boolean</span></span>

## <span data-ttu-id="56bab-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56bab-144">NOTES</span></span>

<span data-ttu-id="56bab-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="56bab-145">ALIASES</span></span>

<span data-ttu-id="56bab-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="56bab-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56bab-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="56bab-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56bab-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56bab-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56bab-149">INPUTOBJECT <IMariaDbIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="56bab-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56bab-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="56bab-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="56bab-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="56bab-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="56bab-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="56bab-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="56bab-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="56bab-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56bab-154">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="56bab-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="56bab-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="56bab-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="56bab-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="56bab-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="56bab-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="56bab-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="56bab-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="56bab-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="56bab-159">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="56bab-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="56bab-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="56bab-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="56bab-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56bab-161">RELATED LINKS</span></span>

