---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300816"
---
# <span data-ttu-id="50514-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="50514-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="50514-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50514-102">SYNOPSIS</span></span>
<span data-ttu-id="50514-103">Löscht die Lösung im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50514-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="50514-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50514-104">SYNTAX</span></span>

### <span data-ttu-id="50514-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="50514-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="50514-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="50514-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50514-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50514-107">DESCRIPTION</span></span>
<span data-ttu-id="50514-108">Löscht die Lösung im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50514-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="50514-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50514-109">EXAMPLES</span></span>

### <span data-ttu-id="50514-110">Beispiel 1: Entfernen einer Lösung für die Überwachungsprotokollanalyse nach Name</span><span class="sxs-lookup"><span data-stu-id="50514-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="50514-111">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="50514-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="50514-112">Beispiel 2: Entfernen einer Lösung für die Überwachungsprotokollanalyse nach Objekt</span><span class="sxs-lookup"><span data-stu-id="50514-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="50514-113">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse Objekt für Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="50514-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="50514-114">Beispiel 3: Entfernen einer Lösung für die Überwachungsprotokollanalyse durch Pipeline</span><span class="sxs-lookup"><span data-stu-id="50514-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="50514-115">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse pipelineiert.</span><span class="sxs-lookup"><span data-stu-id="50514-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="50514-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50514-116">PARAMETERS</span></span>

### <span data-ttu-id="50514-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50514-117">-DefaultProfile</span></span>
<span data-ttu-id="50514-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50514-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50514-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50514-119">-InputObject</span></span>
<span data-ttu-id="50514-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="50514-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="50514-121">-Name</span><span class="sxs-lookup"><span data-stu-id="50514-121">-Name</span></span>
<span data-ttu-id="50514-122">Benutzername der Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="50514-122">User Solution Name.</span></span>

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

### <span data-ttu-id="50514-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50514-123">-PassThru</span></span>
<span data-ttu-id="50514-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="50514-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="50514-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50514-125">-ResourceGroupName</span></span>
<span data-ttu-id="50514-126">Der Name der Ressourcengruppe, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="50514-126">The name of the resource group to get.</span></span>
<span data-ttu-id="50514-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="50514-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="50514-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50514-128">-SubscriptionId</span></span>
<span data-ttu-id="50514-129">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="50514-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="50514-130">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="50514-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="50514-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50514-131">-Confirm</span></span>
<span data-ttu-id="50514-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50514-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50514-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="50514-133">-WhatIf</span></span>
<span data-ttu-id="50514-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50514-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50514-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50514-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50514-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50514-136">CommonParameters</span></span>
<span data-ttu-id="50514-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50514-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50514-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50514-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50514-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50514-139">INPUTS</span></span>

### <span data-ttu-id="50514-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="50514-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="50514-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50514-141">OUTPUTS</span></span>

### <span data-ttu-id="50514-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="50514-142">System.Boolean</span></span>

## <span data-ttu-id="50514-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="50514-143">NOTES</span></span>

<span data-ttu-id="50514-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="50514-144">ALIASES</span></span>

<span data-ttu-id="50514-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="50514-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50514-146">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="50514-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50514-147">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50514-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50514-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="50514-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="50514-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="50514-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="50514-150">`[ManagementAssociationName <String>]`: Name der Benutzerverwaltungsassoziation.</span><span class="sxs-lookup"><span data-stu-id="50514-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="50514-151">`[ManagementConfigurationName <String>]`: Konfigurationsname der Benutzerverwaltung.</span><span class="sxs-lookup"><span data-stu-id="50514-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="50514-152">`[ProviderName <String>]`: Anbietername für die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="50514-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="50514-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="50514-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="50514-154">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="50514-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="50514-155">`[ResourceName <String>]`: Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="50514-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="50514-156">`[ResourceType <String>]`: Ressourcentyp für die übergeordnete Ressource</span><span class="sxs-lookup"><span data-stu-id="50514-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="50514-157">`[SolutionName <String>]`: Name der Benutzerlösung.</span><span class="sxs-lookup"><span data-stu-id="50514-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="50514-158">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="50514-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="50514-159">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="50514-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="50514-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="50514-160">RELATED LINKS</span></span>

