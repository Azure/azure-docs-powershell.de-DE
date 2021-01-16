---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293848"
---
# <span data-ttu-id="6dc49-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="6dc49-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="6dc49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dc49-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc49-103">Löscht einen SAP-Monitor mit dem angegebenen Abonnement, der angegebenen Ressourcengruppe und dem Monitornamen.</span><span class="sxs-lookup"><span data-stu-id="6dc49-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="6dc49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6dc49-104">SYNTAX</span></span>

### <span data-ttu-id="6dc49-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="6dc49-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6dc49-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6dc49-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6dc49-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6dc49-107">DESCRIPTION</span></span>
<span data-ttu-id="6dc49-108">Löscht einen SAP-Monitor mit dem angegebenen Abonnement, der angegebenen Ressourcengruppe und dem Monitornamen.</span><span class="sxs-lookup"><span data-stu-id="6dc49-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="6dc49-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6dc49-109">EXAMPLES</span></span>

### <span data-ttu-id="6dc49-110">Beispiel 1: Entfernen eines SAP-Monitors nach Name</span><span class="sxs-lookup"><span data-stu-id="6dc49-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="6dc49-111">Mit diesem Befehl wird ein SAP Monitor nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="6dc49-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="6dc49-112">Beispiel 2: Entfernen eines SAP Monitor nach Objekt</span><span class="sxs-lookup"><span data-stu-id="6dc49-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="6dc49-113">Mit diesem Befehl wird ein SAP Monitor nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="6dc49-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="6dc49-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dc49-114">PARAMETERS</span></span>

### <span data-ttu-id="6dc49-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dc49-115">-AsJob</span></span>
<span data-ttu-id="6dc49-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6dc49-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6dc49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc49-117">-DefaultProfile</span></span>
<span data-ttu-id="6dc49-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6dc49-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dc49-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dc49-119">-InputObject</span></span>
<span data-ttu-id="6dc49-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6dc49-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6dc49-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6dc49-121">-Name</span></span>
<span data-ttu-id="6dc49-122">Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="6dc49-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc49-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6dc49-123">-NoWait</span></span>
<span data-ttu-id="6dc49-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6dc49-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6dc49-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dc49-125">-PassThru</span></span>
<span data-ttu-id="6dc49-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="6dc49-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6dc49-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc49-127">-ResourceGroupName</span></span>
<span data-ttu-id="6dc49-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6dc49-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="6dc49-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6dc49-129">-SubscriptionId</span></span>
<span data-ttu-id="6dc49-130">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6dc49-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6dc49-131">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="6dc49-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6dc49-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dc49-132">-Confirm</span></span>
<span data-ttu-id="6dc49-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6dc49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dc49-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6dc49-134">-WhatIf</span></span>
<span data-ttu-id="6dc49-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6dc49-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dc49-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6dc49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dc49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc49-137">CommonParameters</span></span>
<span data-ttu-id="6dc49-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc49-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dc49-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc49-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6dc49-140">INPUTS</span></span>

### <span data-ttu-id="6dc49-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="6dc49-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="6dc49-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6dc49-142">OUTPUTS</span></span>

### <span data-ttu-id="6dc49-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6dc49-143">System.Boolean</span></span>

## <span data-ttu-id="6dc49-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6dc49-144">NOTES</span></span>

<span data-ttu-id="6dc49-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6dc49-145">ALIASES</span></span>

<span data-ttu-id="6dc49-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6dc49-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6dc49-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6dc49-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6dc49-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6dc49-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6dc49-149">INPUTOBJECT <IHanaOnAzureIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6dc49-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6dc49-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6dc49-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6dc49-151">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="6dc49-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="6dc49-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="6dc49-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="6dc49-153">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="6dc49-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="6dc49-154">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6dc49-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="6dc49-155">`[ResourceName <String>]`: Der Name der Identitätsressource.</span><span class="sxs-lookup"><span data-stu-id="6dc49-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="6dc49-156">`[SapMonitorName <String>]`: Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="6dc49-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="6dc49-157">`[Scope <String>]`: Der Umfang des Ressourcenanbieters der Ressource.</span><span class="sxs-lookup"><span data-stu-id="6dc49-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="6dc49-158">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="6dc49-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="6dc49-159">`[SubscriptionId <String>]`: Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6dc49-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6dc49-160">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="6dc49-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6dc49-161">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="6dc49-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="6dc49-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6dc49-162">RELATED LINKS</span></span>

