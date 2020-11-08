---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179606"
---
# <span data-ttu-id="b33d4-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="b33d4-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="b33d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b33d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b33d4-103">Aktualisieren Sie die Tags einer Lösung.</span><span class="sxs-lookup"><span data-stu-id="b33d4-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="b33d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b33d4-104">SYNTAX</span></span>

### <span data-ttu-id="b33d4-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="b33d4-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b33d4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b33d4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b33d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b33d4-107">DESCRIPTION</span></span>
<span data-ttu-id="b33d4-108">Aktualisieren Sie die Tags einer Lösung.</span><span class="sxs-lookup"><span data-stu-id="b33d4-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="b33d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b33d4-109">EXAMPLES</span></span>

### <span data-ttu-id="b33d4-110">Beispiel 1: Aktualisieren einer Monitor Protokollanalyse-Lösung nach Namen</span><span class="sxs-lookup"><span data-stu-id="b33d4-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="b33d4-111">Mit diesem Befehl wird eine Überwachungsprotokoll Analyse Lösung nach Namen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b33d4-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="b33d4-112">Beispiel 2: Aktualisieren einer Monitor Protokollanalyse-Lösung nach Objekt</span><span class="sxs-lookup"><span data-stu-id="b33d4-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="b33d4-113">Mit diesem Befehl wird eine Überwachungsprotokoll Analyse-Lösung nach Objekt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b33d4-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="b33d4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b33d4-114">PARAMETERS</span></span>

### <span data-ttu-id="b33d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33d4-115">-DefaultProfile</span></span>
<span data-ttu-id="b33d4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b33d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b33d4-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b33d4-117">-InputObject</span></span>
<span data-ttu-id="b33d4-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b33d4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b33d4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b33d4-119">-Name</span></span>
<span data-ttu-id="b33d4-120">Name der Benutzer Lösung</span><span class="sxs-lookup"><span data-stu-id="b33d4-120">User Solution Name.</span></span>

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

### <span data-ttu-id="b33d4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b33d4-121">-ResourceGroupName</span></span>
<span data-ttu-id="b33d4-122">Der Name der Ressourcengruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b33d4-122">The name of the resource group to get.</span></span>
<span data-ttu-id="b33d4-123">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b33d4-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b33d4-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b33d4-124">-SubscriptionId</span></span>
<span data-ttu-id="b33d4-125">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b33d4-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b33d4-126">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="b33d4-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b33d4-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b33d4-127">-Tag</span></span>
<span data-ttu-id="b33d4-128">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="b33d4-128">Resource tags</span></span>

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

### <span data-ttu-id="b33d4-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b33d4-129">-Confirm</span></span>
<span data-ttu-id="b33d4-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b33d4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b33d4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b33d4-131">-WhatIf</span></span>
<span data-ttu-id="b33d4-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b33d4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b33d4-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b33d4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b33d4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33d4-134">CommonParameters</span></span>
<span data-ttu-id="b33d4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b33d4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33d4-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b33d4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33d4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b33d4-137">INPUTS</span></span>

### <span data-ttu-id="b33d4-138">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="b33d4-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="b33d4-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b33d4-139">OUTPUTS</span></span>

### <span data-ttu-id="b33d4-140">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="b33d4-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="b33d4-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b33d4-141">NOTES</span></span>

<span data-ttu-id="b33d4-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="b33d4-142">ALIASES</span></span>

<span data-ttu-id="b33d4-143">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b33d4-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b33d4-144">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b33d4-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b33d4-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b33d4-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b33d4-146">Inputobject <IMonitoringSolutionsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="b33d4-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b33d4-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="b33d4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b33d4-148">`[ManagementAssociationName <String>]`: Benutzer ManagementAssociation-Name.</span><span class="sxs-lookup"><span data-stu-id="b33d4-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="b33d4-149">`[ManagementConfigurationName <String>]`: Name der Benutzer Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b33d4-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="b33d4-150">`[ProviderName <String>]`: Anbietername für die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="b33d4-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="b33d4-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b33d4-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="b33d4-152">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b33d4-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="b33d4-153">`[ResourceName <String>]`: Name der übergeordneten Ressource</span><span class="sxs-lookup"><span data-stu-id="b33d4-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="b33d4-154">`[ResourceType <String>]`: Ressourcentyp für die übergeordnete Ressource</span><span class="sxs-lookup"><span data-stu-id="b33d4-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="b33d4-155">`[SolutionName <String>]`: Name der Benutzer Lösung.</span><span class="sxs-lookup"><span data-stu-id="b33d4-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="b33d4-156">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b33d4-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b33d4-157">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="b33d4-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b33d4-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b33d4-158">RELATED LINKS</span></span>

