---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: f4be2a5da2dc8455b6e6674e7e74050ea506ae0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934875"
---
# <span data-ttu-id="2155b-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="2155b-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="2155b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2155b-102">SYNOPSIS</span></span>
<span data-ttu-id="2155b-103">Ruft die Benutzerlösung ab.</span><span class="sxs-lookup"><span data-stu-id="2155b-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="2155b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2155b-104">SYNTAX</span></span>

### <span data-ttu-id="2155b-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="2155b-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2155b-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2155b-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2155b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2155b-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2155b-108">Liste</span><span class="sxs-lookup"><span data-stu-id="2155b-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2155b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2155b-109">DESCRIPTION</span></span>
<span data-ttu-id="2155b-110">Ruft die Benutzerlösung ab.</span><span class="sxs-lookup"><span data-stu-id="2155b-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="2155b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2155b-111">EXAMPLES</span></span>

### <span data-ttu-id="2155b-112">Beispiel 1: Erhalten einer Lösung für die Überwachungsprotokollanalyse nach Name</span><span class="sxs-lookup"><span data-stu-id="2155b-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="2155b-113">Dieser Befehl ruft eine Lösung für die Überwachungsprotokollanalyse nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="2155b-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="2155b-114">Beispiel 2: Erhalten einer Lösung für die Überwachungsprotokollanalyse nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2155b-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="2155b-115">Dieser Befehl ruft eine Lösung für die Überwachungsprotokollanalyse nach Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="2155b-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="2155b-116">Beispiel 3: Erstellen einer Lösung für die Überwachungsprotokollanalyse nach Objekt</span><span class="sxs-lookup"><span data-stu-id="2155b-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="2155b-117">Dieser Befehl ruft eine Lösung für die Überwachungsprotokollanalyse nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="2155b-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="2155b-118">Beispiel 4: Alle Monitorprotokollanalyselösungen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2155b-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="2155b-119">Dieser Befehl ruft alle Monitorprotokollanalyselösungen unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2155b-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="2155b-120">Beispiel 5: Alle Monitorprotokollanalyselösungen unter einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="2155b-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="2155b-121">Dieser Befehl ruft alle Monitorprotokollanalyselösungen unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2155b-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="2155b-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2155b-122">PARAMETERS</span></span>

### <span data-ttu-id="2155b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2155b-123">-DefaultProfile</span></span>
<span data-ttu-id="2155b-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2155b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2155b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2155b-125">-InputObject</span></span>
<span data-ttu-id="2155b-126">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2155b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2155b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2155b-127">-Name</span></span>
<span data-ttu-id="2155b-128">Benutzername der Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="2155b-128">User Solution Name.</span></span>

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

### <span data-ttu-id="2155b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2155b-129">-ResourceGroupName</span></span>
<span data-ttu-id="2155b-130">Der Name der zu erhaltende Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2155b-130">The name of the resource group to get.</span></span>
<span data-ttu-id="2155b-131">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2155b-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2155b-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2155b-132">-SubscriptionId</span></span>
<span data-ttu-id="2155b-133">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2155b-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2155b-134">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="2155b-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2155b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2155b-135">CommonParameters</span></span>
<span data-ttu-id="2155b-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2155b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2155b-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2155b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2155b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2155b-138">INPUTS</span></span>

### <span data-ttu-id="2155b-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="2155b-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="2155b-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2155b-140">OUTPUTS</span></span>

### <span data-ttu-id="2155b-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="2155b-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="2155b-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2155b-142">NOTES</span></span>

<span data-ttu-id="2155b-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2155b-143">ALIASES</span></span>

<span data-ttu-id="2155b-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2155b-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2155b-145">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2155b-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2155b-146">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2155b-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2155b-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="2155b-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2155b-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2155b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2155b-149">`[ManagementAssociationName <String>]`: Name der Benutzerverwaltungsassoziation.</span><span class="sxs-lookup"><span data-stu-id="2155b-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="2155b-150">`[ManagementConfigurationName <String>]`: Name der Benutzerverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2155b-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="2155b-151">`[ProviderName <String>]`: Anbietername für die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="2155b-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="2155b-152">`[ResourceGroupName <String>]`: Der Name der zu erhaltende Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2155b-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="2155b-153">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2155b-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="2155b-154">`[ResourceName <String>]`: Übergeordneter Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2155b-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="2155b-155">`[ResourceType <String>]`: Ressourcentyp für die übergeordnete Ressource</span><span class="sxs-lookup"><span data-stu-id="2155b-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="2155b-156">`[SolutionName <String>]`: Name der Benutzerlösung.</span><span class="sxs-lookup"><span data-stu-id="2155b-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="2155b-157">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2155b-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2155b-158">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="2155b-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2155b-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2155b-159">RELATED LINKS</span></span>

