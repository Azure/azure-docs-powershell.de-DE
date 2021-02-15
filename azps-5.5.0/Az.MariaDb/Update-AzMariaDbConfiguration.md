---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159473"
---
# <span data-ttu-id="a9264-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9264-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="a9264-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9264-102">SYNOPSIS</span></span>
<span data-ttu-id="a9264-103">Aktualisiert die Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="a9264-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="a9264-104">Verwenden Update-AzMariaDbServer, wenn Sie "AdministratorLoginPassword", "SKU" usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a9264-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="a9264-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9264-105">SYNTAX</span></span>

### <span data-ttu-id="a9264-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9264-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9264-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a9264-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9264-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9264-108">DESCRIPTION</span></span>
<span data-ttu-id="a9264-109">Aktualisiert die Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="a9264-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="a9264-110">Verwenden Update-AzMariaDberver, wenn Sie "AdministratorLoginPassword", "SKU" usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a9264-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="a9264-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9264-111">EXAMPLES</span></span>

### <span data-ttu-id="a9264-112">Beispiel 1: Aktualisieren der Konfiguration von MariaDB</span><span class="sxs-lookup"><span data-stu-id="a9264-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="a9264-113">Mit diesem Befehl wird eine MariaDB-Konfiguration aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a9264-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="a9264-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9264-114">PARAMETERS</span></span>

### <span data-ttu-id="a9264-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9264-115">-AsJob</span></span>
<span data-ttu-id="a9264-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a9264-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a9264-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9264-117">-DefaultProfile</span></span>
<span data-ttu-id="a9264-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9264-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9264-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9264-119">-InputObject</span></span>
<span data-ttu-id="a9264-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a9264-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9264-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a9264-121">-Name</span></span>
<span data-ttu-id="a9264-122">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a9264-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="a9264-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a9264-123">-NoWait</span></span>
<span data-ttu-id="a9264-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a9264-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a9264-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9264-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9264-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a9264-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a9264-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a9264-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a9264-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9264-128">-ServerName</span></span>
<span data-ttu-id="a9264-129">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a9264-129">The name of the server.</span></span>

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

### <span data-ttu-id="a9264-130">-Source</span><span class="sxs-lookup"><span data-stu-id="a9264-130">-Source</span></span>
<span data-ttu-id="a9264-131">Quelle der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a9264-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="a9264-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9264-132">-SubscriptionId</span></span>
<span data-ttu-id="a9264-133">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a9264-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a9264-134">-Value</span><span class="sxs-lookup"><span data-stu-id="a9264-134">-Value</span></span>
<span data-ttu-id="a9264-135">Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a9264-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="a9264-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9264-136">-Confirm</span></span>
<span data-ttu-id="a9264-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9264-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9264-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a9264-138">-WhatIf</span></span>
<span data-ttu-id="a9264-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9264-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9264-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9264-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9264-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9264-141">CommonParameters</span></span>
<span data-ttu-id="a9264-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9264-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9264-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9264-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9264-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9264-144">INPUTS</span></span>

### <span data-ttu-id="a9264-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="a9264-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="a9264-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9264-146">OUTPUTS</span></span>

### <span data-ttu-id="a9264-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9264-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="a9264-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9264-148">NOTES</span></span>

<span data-ttu-id="a9264-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a9264-149">ALIASES</span></span>

<span data-ttu-id="a9264-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a9264-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9264-151">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9264-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9264-152">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9264-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9264-153">INPUTOBJECT <IMariaDbIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a9264-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9264-154">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a9264-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a9264-155">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a9264-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a9264-156">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="a9264-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a9264-157">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a9264-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9264-158">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="a9264-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a9264-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a9264-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a9264-160">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a9264-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a9264-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="a9264-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a9264-162">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a9264-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a9264-163">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a9264-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="a9264-164">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a9264-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a9264-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9264-165">RELATED LINKS</span></span>

