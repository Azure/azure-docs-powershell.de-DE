---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 630393d0c535a5f44f8a5e7dcf49cc491552f185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949280"
---
# <span data-ttu-id="434ff-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="434ff-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="434ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="434ff-102">SYNOPSIS</span></span>
<span data-ttu-id="434ff-103">Löscht eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="434ff-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="434ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="434ff-104">SYNTAX</span></span>

### <span data-ttu-id="434ff-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="434ff-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="434ff-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="434ff-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="434ff-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="434ff-107">DESCRIPTION</span></span>
<span data-ttu-id="434ff-108">Löscht eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="434ff-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="434ff-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="434ff-109">EXAMPLES</span></span>

### <span data-ttu-id="434ff-110">Beispiel 1: Entfernen der Instanz des SAP-Monitors nach Name</span><span class="sxs-lookup"><span data-stu-id="434ff-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="434ff-111">Mit diesem Befehl wird die Instanz des SAP-Monitors nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="434ff-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="434ff-112">Beispiel 2: Entfernen der Instanz des SAP-Monitors nach Objekt</span><span class="sxs-lookup"><span data-stu-id="434ff-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="434ff-113">Mit diesem Befehl wird die Instanz des SAP-Monitors nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="434ff-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="434ff-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="434ff-114">PARAMETERS</span></span>

### <span data-ttu-id="434ff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="434ff-115">-AsJob</span></span>
<span data-ttu-id="434ff-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="434ff-116">Run the command as a job</span></span>

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

### <span data-ttu-id="434ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434ff-117">-DefaultProfile</span></span>
<span data-ttu-id="434ff-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="434ff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434ff-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="434ff-119">-InputObject</span></span>
<span data-ttu-id="434ff-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="434ff-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="434ff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="434ff-121">-Name</span></span>
<span data-ttu-id="434ff-122">Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="434ff-122">Name of the provider instance.</span></span>

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

### <span data-ttu-id="434ff-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="434ff-123">-NoWait</span></span>
<span data-ttu-id="434ff-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="434ff-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="434ff-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="434ff-125">-PassThru</span></span>
<span data-ttu-id="434ff-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="434ff-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="434ff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434ff-127">-ResourceGroupName</span></span>
<span data-ttu-id="434ff-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="434ff-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="434ff-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="434ff-129">-SapMonitorName</span></span>
<span data-ttu-id="434ff-130">Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="434ff-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="434ff-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="434ff-131">-SubscriptionId</span></span>
<span data-ttu-id="434ff-132">Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="434ff-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="434ff-133">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="434ff-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="434ff-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="434ff-134">-Confirm</span></span>
<span data-ttu-id="434ff-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="434ff-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="434ff-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="434ff-136">-WhatIf</span></span>
<span data-ttu-id="434ff-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="434ff-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="434ff-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="434ff-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="434ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434ff-139">CommonParameters</span></span>
<span data-ttu-id="434ff-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="434ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434ff-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="434ff-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434ff-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="434ff-142">INPUTS</span></span>

### <span data-ttu-id="434ff-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="434ff-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="434ff-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="434ff-144">OUTPUTS</span></span>

### <span data-ttu-id="434ff-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="434ff-145">System.Boolean</span></span>

## <span data-ttu-id="434ff-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="434ff-146">NOTES</span></span>

<span data-ttu-id="434ff-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="434ff-147">ALIASES</span></span>

<span data-ttu-id="434ff-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="434ff-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="434ff-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="434ff-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="434ff-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="434ff-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="434ff-151">INPUTOBJECT <IHanaOnAzureIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="434ff-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="434ff-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="434ff-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="434ff-153">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="434ff-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="434ff-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="434ff-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="434ff-155">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="434ff-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="434ff-156">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="434ff-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="434ff-157">`[ResourceName <String>]`: Der Name der Identitätsressource.</span><span class="sxs-lookup"><span data-stu-id="434ff-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="434ff-158">`[SapMonitorName <String>]`: Name der SAP-Monitorressource.</span><span class="sxs-lookup"><span data-stu-id="434ff-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="434ff-159">`[Scope <String>]`: Der Ressourcenanbieterbereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="434ff-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="434ff-160">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="434ff-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="434ff-161">`[SubscriptionId <String>]`: Abonnement-ID, mit der Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="434ff-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="434ff-162">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="434ff-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="434ff-163">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="434ff-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="434ff-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="434ff-164">RELATED LINKS</span></span>

