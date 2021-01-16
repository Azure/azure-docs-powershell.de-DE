---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297287"
---
# <span data-ttu-id="50905-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="50905-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="50905-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50905-102">SYNOPSIS</span></span>
<span data-ttu-id="50905-103">Löscht eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den Namen von SapMonitor und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="50905-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="50905-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50905-104">SYNTAX</span></span>

### <span data-ttu-id="50905-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="50905-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="50905-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="50905-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50905-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50905-107">DESCRIPTION</span></span>
<span data-ttu-id="50905-108">Löscht eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den Namen von SapMonitor und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="50905-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="50905-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50905-109">EXAMPLES</span></span>

### <span data-ttu-id="50905-110">Beispiel 1: Entfernen der Instanz des SAP Monitor nach Name</span><span class="sxs-lookup"><span data-stu-id="50905-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="50905-111">Mit diesem Befehl wird die Instanz des SAP Monitor nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="50905-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="50905-112">Beispiel 2: Entfernen der Instanz eines SAP Monitor nach Objekt</span><span class="sxs-lookup"><span data-stu-id="50905-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="50905-113">Mit diesem Befehl wird die Instanz des SAP Monitor nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="50905-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="50905-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50905-114">PARAMETERS</span></span>

### <span data-ttu-id="50905-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50905-115">-AsJob</span></span>
<span data-ttu-id="50905-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="50905-116">Run the command as a job</span></span>

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

### <span data-ttu-id="50905-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50905-117">-DefaultProfile</span></span>
<span data-ttu-id="50905-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50905-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50905-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50905-119">-InputObject</span></span>
<span data-ttu-id="50905-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="50905-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50905-121">-Name</span><span class="sxs-lookup"><span data-stu-id="50905-121">-Name</span></span>
<span data-ttu-id="50905-122">Der Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="50905-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50905-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="50905-123">-NoWait</span></span>
<span data-ttu-id="50905-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="50905-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="50905-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50905-125">-PassThru</span></span>
<span data-ttu-id="50905-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="50905-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="50905-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50905-127">-ResourceGroupName</span></span>
<span data-ttu-id="50905-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="50905-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="50905-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="50905-129">-SapMonitorName</span></span>
<span data-ttu-id="50905-130">Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="50905-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="50905-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50905-131">-SubscriptionId</span></span>
<span data-ttu-id="50905-132">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="50905-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="50905-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="50905-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="50905-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50905-134">-Confirm</span></span>
<span data-ttu-id="50905-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50905-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50905-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="50905-136">-WhatIf</span></span>
<span data-ttu-id="50905-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50905-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50905-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50905-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50905-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50905-139">CommonParameters</span></span>
<span data-ttu-id="50905-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50905-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50905-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50905-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50905-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50905-142">INPUTS</span></span>

### <span data-ttu-id="50905-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="50905-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="50905-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50905-144">OUTPUTS</span></span>

### <span data-ttu-id="50905-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="50905-145">System.Boolean</span></span>

## <span data-ttu-id="50905-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="50905-146">NOTES</span></span>

<span data-ttu-id="50905-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="50905-147">ALIASES</span></span>

<span data-ttu-id="50905-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="50905-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50905-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="50905-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50905-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50905-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50905-151">INPUTOBJECT <IHanaOnAzureIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="50905-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="50905-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="50905-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="50905-153">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="50905-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="50905-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="50905-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="50905-155">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="50905-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="50905-156">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="50905-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="50905-157">`[ResourceName <String>]`: Der Name der Identitätsressource.</span><span class="sxs-lookup"><span data-stu-id="50905-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="50905-158">`[SapMonitorName <String>]`: Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="50905-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="50905-159">`[Scope <String>]`: Der Umfang des Ressourcenanbieters der Ressource.</span><span class="sxs-lookup"><span data-stu-id="50905-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="50905-160">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="50905-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="50905-161">`[SubscriptionId <String>]`: Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="50905-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="50905-162">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="50905-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="50905-163">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="50905-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="50905-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="50905-164">RELATED LINKS</span></span>

