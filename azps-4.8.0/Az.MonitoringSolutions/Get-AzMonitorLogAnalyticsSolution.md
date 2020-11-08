---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166489"
---
# <span data-ttu-id="43700-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="43700-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="43700-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43700-102">SYNOPSIS</span></span>
<span data-ttu-id="43700-103">Ruft die Benutzer Lösung ab.</span><span class="sxs-lookup"><span data-stu-id="43700-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="43700-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43700-104">SYNTAX</span></span>

### <span data-ttu-id="43700-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="43700-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="43700-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="43700-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43700-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43700-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="43700-108">Liste</span><span class="sxs-lookup"><span data-stu-id="43700-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="43700-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43700-109">DESCRIPTION</span></span>
<span data-ttu-id="43700-110">Ruft die Benutzer Lösung ab.</span><span class="sxs-lookup"><span data-stu-id="43700-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="43700-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43700-111">EXAMPLES</span></span>

### <span data-ttu-id="43700-112">Beispiel 1: Abrufen einer Monitor Protokollanalyse-Lösung nach Namen</span><span class="sxs-lookup"><span data-stu-id="43700-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="43700-113">Mit diesem Befehl wird eine Überwachungsprotokoll Analyse Lösung nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="43700-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="43700-114">Beispiel 2: Abrufen einer Monitor Protokollanalyse-Lösung nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="43700-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="43700-115">Mit diesem Befehl wird eine Überwachungsprotokoll Analyse Lösung nach Ressourcen-ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="43700-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="43700-116">Beispiel 3: Abrufen einer Monitor Protokollanalyse-Lösung nach Objekt</span><span class="sxs-lookup"><span data-stu-id="43700-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="43700-117">Mit diesem Befehl wird eine Monitor Protokollanalyse-Lösung nach Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="43700-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="43700-118">Beispiel 4: Abrufen aller Lösungen für die Überwachungsprotokoll Analyse unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="43700-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="43700-119">Dieser Befehl ruft alle Überwachungsprotokoll Analyselösungen unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="43700-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="43700-120">Beispiel 5: Abrufen aller Überwachungsprotokoll Analyselösungen unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="43700-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="43700-121">Dieser Befehl ruft alle Überwachungsprotokoll Analyselösungen unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="43700-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="43700-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="43700-122">PARAMETERS</span></span>

### <span data-ttu-id="43700-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43700-123">-DefaultProfile</span></span>
<span data-ttu-id="43700-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43700-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43700-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43700-125">-InputObject</span></span>
<span data-ttu-id="43700-126">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="43700-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43700-127">-Name</span><span class="sxs-lookup"><span data-stu-id="43700-127">-Name</span></span>
<span data-ttu-id="43700-128">Name der Benutzer Lösung</span><span class="sxs-lookup"><span data-stu-id="43700-128">User Solution Name.</span></span>

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

### <span data-ttu-id="43700-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43700-129">-ResourceGroupName</span></span>
<span data-ttu-id="43700-130">Der Name der Ressourcengruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="43700-130">The name of the resource group to get.</span></span>
<span data-ttu-id="43700-131">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="43700-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="43700-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="43700-132">-SubscriptionId</span></span>
<span data-ttu-id="43700-133">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="43700-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="43700-134">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="43700-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="43700-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43700-135">CommonParameters</span></span>
<span data-ttu-id="43700-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43700-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43700-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43700-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43700-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43700-138">INPUTS</span></span>

### <span data-ttu-id="43700-139">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="43700-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="43700-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43700-140">OUTPUTS</span></span>

### <span data-ttu-id="43700-141">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="43700-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="43700-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="43700-142">NOTES</span></span>

<span data-ttu-id="43700-143">Aliase</span><span class="sxs-lookup"><span data-stu-id="43700-143">ALIASES</span></span>

<span data-ttu-id="43700-144">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43700-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43700-145">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="43700-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43700-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="43700-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43700-147">Inputobject <IMonitoringSolutionsIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="43700-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43700-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="43700-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43700-149">`[ManagementAssociationName <String>]`: Benutzer ManagementAssociation-Name.</span><span class="sxs-lookup"><span data-stu-id="43700-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="43700-150">`[ManagementConfigurationName <String>]`: Name der Benutzer Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="43700-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="43700-151">`[ProviderName <String>]`: Anbietername für die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="43700-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="43700-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="43700-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="43700-153">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="43700-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="43700-154">`[ResourceName <String>]`: Name der übergeordneten Ressource</span><span class="sxs-lookup"><span data-stu-id="43700-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="43700-155">`[ResourceType <String>]`: Ressourcentyp für die übergeordnete Ressource</span><span class="sxs-lookup"><span data-stu-id="43700-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="43700-156">`[SolutionName <String>]`: Name der Benutzer Lösung.</span><span class="sxs-lookup"><span data-stu-id="43700-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="43700-157">`[SubscriptionId <String>]`: Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="43700-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="43700-158">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="43700-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="43700-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43700-159">RELATED LINKS</span></span>

