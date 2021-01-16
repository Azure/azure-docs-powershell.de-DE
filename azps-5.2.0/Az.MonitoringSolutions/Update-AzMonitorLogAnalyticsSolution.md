---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306464"
---
# <span data-ttu-id="40de6-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="40de6-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="40de6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40de6-102">SYNOPSIS</span></span>
<span data-ttu-id="40de6-103">Aktualisieren Sie die Tags einer Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="40de6-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="40de6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40de6-104">SYNTAX</span></span>

### <span data-ttu-id="40de6-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="40de6-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40de6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="40de6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40de6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40de6-107">DESCRIPTION</span></span>
<span data-ttu-id="40de6-108">Aktualisieren Sie die Tags einer Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="40de6-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="40de6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40de6-109">EXAMPLES</span></span>

### <span data-ttu-id="40de6-110">Beispiel 1: Aktualisieren einer Lösung für die Überwachungsprotokollanalyse nach Name</span><span class="sxs-lookup"><span data-stu-id="40de6-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="40de6-111">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse nach Name aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="40de6-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="40de6-112">Beispiel 2: Aktualisieren einer Lösung für die Überwachungsprotokollanalyse nach Objekt</span><span class="sxs-lookup"><span data-stu-id="40de6-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="40de6-113">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse objekttyp aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="40de6-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="40de6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40de6-114">PARAMETERS</span></span>

### <span data-ttu-id="40de6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40de6-115">-DefaultProfile</span></span>
<span data-ttu-id="40de6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40de6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40de6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40de6-117">-InputObject</span></span>
<span data-ttu-id="40de6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="40de6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40de6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="40de6-119">-Name</span></span>
<span data-ttu-id="40de6-120">Benutzername der Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="40de6-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40de6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40de6-121">-ResourceGroupName</span></span>
<span data-ttu-id="40de6-122">Der Name der Ressourcengruppe, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="40de6-122">The name of the resource group to get.</span></span>
<span data-ttu-id="40de6-123">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="40de6-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="40de6-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40de6-124">-SubscriptionId</span></span>
<span data-ttu-id="40de6-125">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="40de6-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="40de6-126">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="40de6-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="40de6-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="40de6-127">-Tag</span></span>
<span data-ttu-id="40de6-128">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="40de6-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40de6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40de6-129">-Confirm</span></span>
<span data-ttu-id="40de6-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40de6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40de6-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="40de6-131">-WhatIf</span></span>
<span data-ttu-id="40de6-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40de6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40de6-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40de6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40de6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40de6-134">CommonParameters</span></span>
<span data-ttu-id="40de6-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40de6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40de6-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40de6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40de6-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40de6-137">INPUTS</span></span>

### <span data-ttu-id="40de6-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="40de6-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="40de6-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40de6-139">OUTPUTS</span></span>

### <span data-ttu-id="40de6-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="40de6-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="40de6-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40de6-141">NOTES</span></span>

<span data-ttu-id="40de6-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="40de6-142">ALIASES</span></span>

<span data-ttu-id="40de6-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="40de6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40de6-144">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="40de6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40de6-145">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40de6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40de6-146">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="40de6-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40de6-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="40de6-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40de6-148">`[ManagementAssociationName <String>]`: Name der Benutzerverwaltungsassoziation.</span><span class="sxs-lookup"><span data-stu-id="40de6-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="40de6-149">`[ManagementConfigurationName <String>]`: Konfigurationsname der Benutzerverwaltung.</span><span class="sxs-lookup"><span data-stu-id="40de6-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="40de6-150">`[ProviderName <String>]`: Anbietername für die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="40de6-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="40de6-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="40de6-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="40de6-152">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="40de6-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="40de6-153">`[ResourceName <String>]`: Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="40de6-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="40de6-154">`[ResourceType <String>]`: Ressourcentyp für die übergeordnete Ressource</span><span class="sxs-lookup"><span data-stu-id="40de6-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="40de6-155">`[SolutionName <String>]`: Name der Benutzerlösung.</span><span class="sxs-lookup"><span data-stu-id="40de6-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="40de6-156">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="40de6-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="40de6-157">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="40de6-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="40de6-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40de6-158">RELATED LINKS</span></span>

