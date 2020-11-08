---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009185"
---
# <span data-ttu-id="35298-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="35298-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="35298-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35298-102">SYNOPSIS</span></span>
<span data-ttu-id="35298-103">Löscht die Lösung im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35298-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="35298-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35298-104">SYNTAX</span></span>

### <span data-ttu-id="35298-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="35298-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35298-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35298-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35298-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35298-107">DESCRIPTION</span></span>
<span data-ttu-id="35298-108">Löscht die Lösung im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35298-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="35298-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35298-109">EXAMPLES</span></span>

### <span data-ttu-id="35298-110">Beispiel 1: Entfernen einer Monitor Protokollanalyse-Lösung nach Namen</span><span class="sxs-lookup"><span data-stu-id="35298-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="35298-111">Mit diesem Befehl wird eine Lösung für die Monitor Protokollanalyse nach Namen entfernt.</span><span class="sxs-lookup"><span data-stu-id="35298-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="35298-112">Beispiel 2: Entfernen einer Monitor Protokollanalyse-Lösung nach Objekt</span><span class="sxs-lookup"><span data-stu-id="35298-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="35298-113">Mit diesem Befehl wird eine Überwachungsprotokoll-Analyse Lösung nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="35298-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="35298-114">Beispiel 3: Entfernen einer Monitor Protokollanalyse-Lösung nach Pipeline</span><span class="sxs-lookup"><span data-stu-id="35298-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="35298-115">Dieser Befehl entfernt eine Überwachungsprotokoll Analyse Lösung nach Pipeline.</span><span class="sxs-lookup"><span data-stu-id="35298-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="35298-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="35298-116">PARAMETERS</span></span>

### <span data-ttu-id="35298-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35298-117">-DefaultProfile</span></span>
<span data-ttu-id="35298-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35298-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35298-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35298-119">-InputObject</span></span>
<span data-ttu-id="35298-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="35298-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35298-121">-Name</span><span class="sxs-lookup"><span data-stu-id="35298-121">-Name</span></span>
<span data-ttu-id="35298-122">Name der Benutzer Lösung</span><span class="sxs-lookup"><span data-stu-id="35298-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35298-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35298-123">-PassThru</span></span>
<span data-ttu-id="35298-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="35298-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="35298-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35298-125">-ResourceGroupName</span></span>
<span data-ttu-id="35298-126">Der Name der Ressourcengruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="35298-126">The name of the resource group to get.</span></span>
<span data-ttu-id="35298-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="35298-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="35298-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="35298-128">-SubscriptionId</span></span>
<span data-ttu-id="35298-129">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="35298-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="35298-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="35298-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="35298-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35298-131">-Confirm</span></span>
<span data-ttu-id="35298-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35298-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35298-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35298-133">-WhatIf</span></span>
<span data-ttu-id="35298-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35298-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35298-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35298-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35298-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35298-136">CommonParameters</span></span>
<span data-ttu-id="35298-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35298-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35298-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35298-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35298-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35298-139">INPUTS</span></span>

### <span data-ttu-id="35298-140">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="35298-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="35298-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35298-141">OUTPUTS</span></span>

### <span data-ttu-id="35298-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35298-142">System.Boolean</span></span>

## <span data-ttu-id="35298-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="35298-143">NOTES</span></span>

<span data-ttu-id="35298-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="35298-144">ALIASES</span></span>

<span data-ttu-id="35298-145">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35298-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35298-146">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="35298-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35298-147">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="35298-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35298-148">Inputobject <IMonitoringSolutionsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="35298-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35298-149">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="35298-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35298-150">`[ManagementAssociationName <String>]`: Benutzer ManagementAssociation-Name.</span><span class="sxs-lookup"><span data-stu-id="35298-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="35298-151">`[ManagementConfigurationName <String>]`: Name der Benutzer Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="35298-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="35298-152">`[ProviderName <String>]`: Anbietername für die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="35298-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="35298-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="35298-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="35298-154">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="35298-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="35298-155">`[ResourceName <String>]`: Name der übergeordneten Ressource</span><span class="sxs-lookup"><span data-stu-id="35298-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="35298-156">`[ResourceType <String>]`: Ressourcentyp für die übergeordnete Ressource</span><span class="sxs-lookup"><span data-stu-id="35298-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="35298-157">`[SolutionName <String>]`: Name der Benutzer Lösung.</span><span class="sxs-lookup"><span data-stu-id="35298-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="35298-158">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="35298-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="35298-159">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="35298-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="35298-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35298-160">RELATED LINKS</span></span>

