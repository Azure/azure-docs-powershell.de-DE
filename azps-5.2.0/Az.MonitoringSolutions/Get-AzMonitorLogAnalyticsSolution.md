---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306459"
---
# <span data-ttu-id="54d5e-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="54d5e-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="54d5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="54d5e-103">Ruft die Benutzerlösung ab.</span><span class="sxs-lookup"><span data-stu-id="54d5e-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="54d5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54d5e-104">SYNTAX</span></span>

### <span data-ttu-id="54d5e-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="54d5e-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="54d5e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="54d5e-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54d5e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="54d5e-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="54d5e-108">Liste</span><span class="sxs-lookup"><span data-stu-id="54d5e-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="54d5e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54d5e-109">DESCRIPTION</span></span>
<span data-ttu-id="54d5e-110">Ruft die Benutzerlösung ab.</span><span class="sxs-lookup"><span data-stu-id="54d5e-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="54d5e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54d5e-111">EXAMPLES</span></span>

### <span data-ttu-id="54d5e-112">Beispiel 1: Erstellen einer Lösung für die Überwachungsprotokollanalyse nach Name</span><span class="sxs-lookup"><span data-stu-id="54d5e-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="54d5e-113">Dieser Befehl ruft eine Lösung für die Überwachungsprotokollanalyse nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="54d5e-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="54d5e-114">Beispiel 2: Erhalten einer Lösung für die Überwachungsprotokollanalyse nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="54d5e-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="54d5e-115">Dieser Befehl ruft eine Lösung für die Überwachungsprotokollanalyse nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="54d5e-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="54d5e-116">Beispiel 3: Erhalten einer Lösung für die Überwachungsprotokollanalyse nach Objekt</span><span class="sxs-lookup"><span data-stu-id="54d5e-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="54d5e-117">Dieser Befehl ruft eine Objektlösung für die Überwachungsprotokollanalyse ab.</span><span class="sxs-lookup"><span data-stu-id="54d5e-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="54d5e-118">Beispiel 4: Alle Lösungen für die Überwachungsprotokollanalyse unter einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="54d5e-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="54d5e-119">Dieser Befehl ruft alle Lösungen für die Überwachungsprotokollanalyse unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="54d5e-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="54d5e-120">Beispiel 5: Alle Lösungen für die Überwachungsprotokollanalyse im Rahmen eines Abonnements erhalten</span><span class="sxs-lookup"><span data-stu-id="54d5e-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="54d5e-121">Dieser Befehl ruft alle Lösungen für die Überwachungsprotokollanalyse unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="54d5e-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="54d5e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54d5e-122">PARAMETERS</span></span>

### <span data-ttu-id="54d5e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d5e-123">-DefaultProfile</span></span>
<span data-ttu-id="54d5e-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54d5e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54d5e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54d5e-125">-InputObject</span></span>
<span data-ttu-id="54d5e-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="54d5e-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54d5e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="54d5e-127">-Name</span></span>
<span data-ttu-id="54d5e-128">Benutzername der Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="54d5e-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d5e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d5e-129">-ResourceGroupName</span></span>
<span data-ttu-id="54d5e-130">Der Name der Ressourcengruppe, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="54d5e-130">The name of the resource group to get.</span></span>
<span data-ttu-id="54d5e-131">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="54d5e-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d5e-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54d5e-132">-SubscriptionId</span></span>
<span data-ttu-id="54d5e-133">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="54d5e-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="54d5e-134">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="54d5e-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d5e-135">CommonParameters</span></span>
<span data-ttu-id="54d5e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d5e-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54d5e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d5e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54d5e-138">INPUTS</span></span>

### <span data-ttu-id="54d5e-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="54d5e-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="54d5e-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54d5e-140">OUTPUTS</span></span>

### <span data-ttu-id="54d5e-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="54d5e-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="54d5e-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54d5e-142">NOTES</span></span>

<span data-ttu-id="54d5e-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="54d5e-143">ALIASES</span></span>

<span data-ttu-id="54d5e-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="54d5e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54d5e-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="54d5e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54d5e-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54d5e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54d5e-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="54d5e-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54d5e-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="54d5e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54d5e-149">`[ManagementAssociationName <String>]`: Name der Benutzerverwaltungsassoziation.</span><span class="sxs-lookup"><span data-stu-id="54d5e-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="54d5e-150">`[ManagementConfigurationName <String>]`: Konfigurationsname der Benutzerverwaltung.</span><span class="sxs-lookup"><span data-stu-id="54d5e-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="54d5e-151">`[ProviderName <String>]`: Anbietername für die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="54d5e-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="54d5e-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="54d5e-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="54d5e-153">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="54d5e-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="54d5e-154">`[ResourceName <String>]`: Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="54d5e-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="54d5e-155">`[ResourceType <String>]`: Ressourcentyp für die übergeordnete Ressource</span><span class="sxs-lookup"><span data-stu-id="54d5e-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="54d5e-156">`[SolutionName <String>]`: Name der Benutzerlösung.</span><span class="sxs-lookup"><span data-stu-id="54d5e-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="54d5e-157">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="54d5e-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="54d5e-158">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="54d5e-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="54d5e-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54d5e-159">RELATED LINKS</span></span>

