---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: dc2a36a9ac8c2595ef2f60b8edc40582ad864ff8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945046"
---
# <span data-ttu-id="d53a2-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="d53a2-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="d53a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d53a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d53a2-103">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="d53a2-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="d53a2-104">Verwenden Update-AzMariaDbServer sie stattdessen, wenn Sie AdministratorLoginPassword, Sku usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d53a2-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="d53a2-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d53a2-105">SYNTAX</span></span>

### <span data-ttu-id="d53a2-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="d53a2-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d53a2-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d53a2-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d53a2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d53a2-108">DESCRIPTION</span></span>
<span data-ttu-id="d53a2-109">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="d53a2-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="d53a2-110">Verwenden Update-AzMariaDberver sie stattdessen, wenn Sie AdministratorLoginPassword, Sku usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d53a2-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="d53a2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d53a2-111">EXAMPLES</span></span>

### <span data-ttu-id="d53a2-112">Beispiel 1: Aktualisieren der MariaDB-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d53a2-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="d53a2-113">Mit diesem Befehl wird eine MariaDB-Konfiguration aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d53a2-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="d53a2-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d53a2-114">PARAMETERS</span></span>

### <span data-ttu-id="d53a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d53a2-115">-AsJob</span></span>
<span data-ttu-id="d53a2-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d53a2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d53a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53a2-117">-DefaultProfile</span></span>
<span data-ttu-id="d53a2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d53a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d53a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d53a2-119">-InputObject</span></span>
<span data-ttu-id="d53a2-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d53a2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d53a2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d53a2-121">-Name</span></span>
<span data-ttu-id="d53a2-122">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d53a2-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="d53a2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d53a2-123">-NoWait</span></span>
<span data-ttu-id="d53a2-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d53a2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d53a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d53a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="d53a2-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d53a2-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d53a2-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d53a2-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d53a2-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="d53a2-128">-ServerName</span></span>
<span data-ttu-id="d53a2-129">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="d53a2-129">The name of the server.</span></span>

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

### <span data-ttu-id="d53a2-130">-Source</span><span class="sxs-lookup"><span data-stu-id="d53a2-130">-Source</span></span>
<span data-ttu-id="d53a2-131">Quelle der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d53a2-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="d53a2-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d53a2-132">-SubscriptionId</span></span>
<span data-ttu-id="d53a2-133">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d53a2-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d53a2-134">-Wert</span><span class="sxs-lookup"><span data-stu-id="d53a2-134">-Value</span></span>
<span data-ttu-id="d53a2-135">Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d53a2-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="d53a2-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d53a2-136">-Confirm</span></span>
<span data-ttu-id="d53a2-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d53a2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d53a2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d53a2-138">-WhatIf</span></span>
<span data-ttu-id="d53a2-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d53a2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d53a2-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d53a2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d53a2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53a2-141">CommonParameters</span></span>
<span data-ttu-id="d53a2-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d53a2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53a2-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d53a2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53a2-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d53a2-144">INPUTS</span></span>

### <span data-ttu-id="d53a2-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d53a2-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d53a2-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d53a2-146">OUTPUTS</span></span>

### <span data-ttu-id="d53a2-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="d53a2-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="d53a2-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d53a2-148">NOTES</span></span>

<span data-ttu-id="d53a2-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d53a2-149">ALIASES</span></span>

<span data-ttu-id="d53a2-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d53a2-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d53a2-151">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="d53a2-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d53a2-152">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d53a2-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d53a2-153">INPUTOBJECT <IMariaDbIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="d53a2-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d53a2-154">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d53a2-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d53a2-155">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d53a2-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d53a2-156">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="d53a2-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d53a2-157">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d53a2-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d53a2-158">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="d53a2-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d53a2-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d53a2-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d53a2-160">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="d53a2-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d53a2-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d53a2-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d53a2-162">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="d53a2-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d53a2-163">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d53a2-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d53a2-164">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d53a2-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d53a2-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d53a2-165">RELATED LINKS</span></span>

