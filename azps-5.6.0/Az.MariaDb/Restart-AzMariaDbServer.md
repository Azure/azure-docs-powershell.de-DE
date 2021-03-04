---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: e8367638f2bcfcf54f0b3183180f2ab8d70b3ffc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945058"
---
# <span data-ttu-id="344bd-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="344bd-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="344bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="344bd-102">SYNOPSIS</span></span>
<span data-ttu-id="344bd-103">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="344bd-103">Restarts a server.</span></span>

## <span data-ttu-id="344bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="344bd-104">SYNTAX</span></span>

### <span data-ttu-id="344bd-105">Servername (Standard)</span><span class="sxs-lookup"><span data-stu-id="344bd-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="344bd-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="344bd-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="344bd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="344bd-107">DESCRIPTION</span></span>
<span data-ttu-id="344bd-108">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="344bd-108">Restarts a server.</span></span>

## <span data-ttu-id="344bd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="344bd-109">EXAMPLES</span></span>

### <span data-ttu-id="344bd-110">Beispiel 1: Neu starten einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="344bd-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="344bd-111">Mit diesem Befehl wird eine MariaDB neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="344bd-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="344bd-112">Beispiel 2: Neu starten einer MariaDB</span><span class="sxs-lookup"><span data-stu-id="344bd-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="344bd-113">Mit diesem Befehl wird eine MariaDB neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="344bd-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="344bd-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="344bd-114">PARAMETERS</span></span>

### <span data-ttu-id="344bd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="344bd-115">-AsJob</span></span>
<span data-ttu-id="344bd-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="344bd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="344bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="344bd-117">-DefaultProfile</span></span>
<span data-ttu-id="344bd-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="344bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="344bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="344bd-119">-InputObject</span></span>
<span data-ttu-id="344bd-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="344bd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="344bd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="344bd-121">-Name</span></span>
<span data-ttu-id="344bd-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="344bd-122">The name of the server.</span></span>

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

### <span data-ttu-id="344bd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="344bd-123">-NoWait</span></span>
<span data-ttu-id="344bd-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="344bd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="344bd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="344bd-125">-PassThru</span></span>
<span data-ttu-id="344bd-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="344bd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="344bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="344bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="344bd-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="344bd-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="344bd-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="344bd-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="344bd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="344bd-130">-SubscriptionId</span></span>
<span data-ttu-id="344bd-131">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="344bd-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="344bd-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="344bd-132">-Confirm</span></span>
<span data-ttu-id="344bd-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="344bd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="344bd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="344bd-134">-WhatIf</span></span>
<span data-ttu-id="344bd-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="344bd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="344bd-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="344bd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="344bd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344bd-137">CommonParameters</span></span>
<span data-ttu-id="344bd-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="344bd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344bd-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="344bd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344bd-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="344bd-140">INPUTS</span></span>

### <span data-ttu-id="344bd-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="344bd-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="344bd-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="344bd-142">OUTPUTS</span></span>

### <span data-ttu-id="344bd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="344bd-143">System.Boolean</span></span>

## <span data-ttu-id="344bd-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="344bd-144">NOTES</span></span>

<span data-ttu-id="344bd-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="344bd-145">ALIASES</span></span>

<span data-ttu-id="344bd-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="344bd-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="344bd-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="344bd-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="344bd-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="344bd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="344bd-149">INPUTOBJECT <IMariaDbIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="344bd-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="344bd-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="344bd-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="344bd-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="344bd-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="344bd-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="344bd-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="344bd-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="344bd-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="344bd-154">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="344bd-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="344bd-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="344bd-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="344bd-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="344bd-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="344bd-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="344bd-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="344bd-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="344bd-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="344bd-159">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="344bd-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="344bd-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="344bd-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="344bd-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="344bd-161">RELATED LINKS</span></span>

