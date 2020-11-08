---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177596"
---
# <span data-ttu-id="04320-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="04320-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="04320-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04320-102">SYNOPSIS</span></span>
<span data-ttu-id="04320-103">Löscht eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="04320-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="04320-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04320-104">SYNTAX</span></span>

### <span data-ttu-id="04320-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="04320-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="04320-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="04320-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="04320-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04320-107">DESCRIPTION</span></span>
<span data-ttu-id="04320-108">Löscht eine Anbieterinstanz für das angegebene Abonnement, die Ressourcengruppe, den SapMonitor-Namen und den Ressourcennamen.</span><span class="sxs-lookup"><span data-stu-id="04320-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="04320-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04320-109">EXAMPLES</span></span>

### <span data-ttu-id="04320-110">Beispiel 1: Entfernen der Instanz des SAP-Monitors nach Name</span><span class="sxs-lookup"><span data-stu-id="04320-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="04320-111">Dieser Befehl entfernt die Instanz des SAP-Monitors nach Namen.</span><span class="sxs-lookup"><span data-stu-id="04320-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="04320-112">Beispiel 2: Entfernen der Instanz des SAP-Monitors nach Objekt</span><span class="sxs-lookup"><span data-stu-id="04320-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="04320-113">Dieser Befehl entfernt die Instanz des SAP-Monitors nach Objekt.</span><span class="sxs-lookup"><span data-stu-id="04320-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="04320-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="04320-114">PARAMETERS</span></span>

### <span data-ttu-id="04320-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04320-115">-AsJob</span></span>
<span data-ttu-id="04320-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="04320-116">Run the command as a job</span></span>

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

### <span data-ttu-id="04320-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04320-117">-DefaultProfile</span></span>
<span data-ttu-id="04320-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04320-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04320-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="04320-119">-InputObject</span></span>
<span data-ttu-id="04320-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="04320-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="04320-121">-Name</span><span class="sxs-lookup"><span data-stu-id="04320-121">-Name</span></span>
<span data-ttu-id="04320-122">Der Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="04320-122">Name of the provider instance.</span></span>

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

### <span data-ttu-id="04320-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="04320-123">-NoWait</span></span>
<span data-ttu-id="04320-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="04320-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="04320-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04320-125">-PassThru</span></span>
<span data-ttu-id="04320-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="04320-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="04320-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04320-127">-ResourceGroupName</span></span>
<span data-ttu-id="04320-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="04320-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="04320-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="04320-129">-SapMonitorName</span></span>
<span data-ttu-id="04320-130">Der Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="04320-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="04320-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="04320-131">-SubscriptionId</span></span>
<span data-ttu-id="04320-132">Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="04320-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="04320-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="04320-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="04320-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04320-134">-Confirm</span></span>
<span data-ttu-id="04320-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04320-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04320-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04320-136">-WhatIf</span></span>
<span data-ttu-id="04320-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04320-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04320-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04320-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04320-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04320-139">CommonParameters</span></span>
<span data-ttu-id="04320-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04320-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04320-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04320-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04320-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04320-142">INPUTS</span></span>

### <span data-ttu-id="04320-143">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="04320-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="04320-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04320-144">OUTPUTS</span></span>

### <span data-ttu-id="04320-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04320-145">System.Boolean</span></span>

## <span data-ttu-id="04320-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="04320-146">NOTES</span></span>

<span data-ttu-id="04320-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="04320-147">ALIASES</span></span>

<span data-ttu-id="04320-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04320-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04320-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="04320-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04320-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="04320-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04320-151">Inputobject <IHanaOnAzureIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="04320-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="04320-152">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="04320-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="04320-153">`[Location <String>]`: Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="04320-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="04320-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="04320-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="04320-155">`[ProviderInstanceName <String>]`: Name der Anbieterinstanz.</span><span class="sxs-lookup"><span data-stu-id="04320-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="04320-156">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="04320-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="04320-157">`[ResourceName <String>]`: Der Name der Identitäts Ressource.</span><span class="sxs-lookup"><span data-stu-id="04320-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="04320-158">`[SapMonitorName <String>]`: Name der SAP-Monitor Ressource.</span><span class="sxs-lookup"><span data-stu-id="04320-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="04320-159">`[Scope <String>]`: Der Ressourcenanbieter Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="04320-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="04320-160">Übergeordnete Ressource, die durch verwaltete Identitäten erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="04320-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="04320-161">`[SubscriptionId <String>]`: Abonnement-ID, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="04320-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="04320-162">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="04320-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="04320-163">`[VaultName <String>]`: Name des Tresors</span><span class="sxs-lookup"><span data-stu-id="04320-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="04320-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04320-164">RELATED LINKS</span></span>

