---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 8ed57766ba36607503994d331cec5381d9f43bbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384458"
---
# <span data-ttu-id="97486-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="97486-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="97486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97486-102">SYNOPSIS</span></span>
<span data-ttu-id="97486-103">Ruft Details zu Azure Site Recovery-Ereignissen im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="97486-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="97486-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97486-104">SYNTAX</span></span>

### <span data-ttu-id="97486-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="97486-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97486-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="97486-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97486-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="97486-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97486-108">ByName</span><span class="sxs-lookup"><span data-stu-id="97486-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97486-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97486-109">DESCRIPTION</span></span>
<span data-ttu-id="97486-110">**"Get-AzRecoveryServicesAsrEvent"** ruft die Liste der Ereignisse im Tresor basierend auf den angegebenen Auswahlfiltern ab.</span><span class="sxs-lookup"><span data-stu-id="97486-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="97486-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97486-111">EXAMPLES</span></span>

### <span data-ttu-id="97486-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97486-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="97486-113">Liste aller Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="97486-113">List of all events.</span></span>

### <span data-ttu-id="97486-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="97486-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="97486-115">Ereignis nach Name erhalten.</span><span class="sxs-lookup"><span data-stu-id="97486-115">Get event by name.</span></span>

### <span data-ttu-id="97486-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="97486-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="97486-117">Liste des Ereignisses für das betroffene Objekt.</span><span class="sxs-lookup"><span data-stu-id="97486-117">List of event for affected Object.</span></span>

### <span data-ttu-id="97486-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="97486-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="97486-119">Liste des Ereignisses zwischen Start- und Endzeit, Schweregrad und Integritätstyp VmHealth.</span><span class="sxs-lookup"><span data-stu-id="97486-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="97486-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97486-120">PARAMETERS</span></span>

### <span data-ttu-id="97486-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="97486-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="97486-122">Gibt "AffectedObject FriendlyName" für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="97486-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97486-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97486-123">-DefaultProfile</span></span>
<span data-ttu-id="97486-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97486-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97486-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="97486-125">-EndTime</span></span>
<span data-ttu-id="97486-126">Gibt die Endzeit des Suchfensters an.</span><span class="sxs-lookup"><span data-stu-id="97486-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="97486-127">Verwenden Sie diesen Parameter, um nur die Ereignisse zu erhalten, die vor dem angegebenen Zeitpunkt aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="97486-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97486-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="97486-128">-EventType</span></span>
<span data-ttu-id="97486-129">Filtern Sie Ereignisse nach Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="97486-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97486-130">-Fabric</span><span class="sxs-lookup"><span data-stu-id="97486-130">-Fabric</span></span>
<span data-ttu-id="97486-131">Filterereignisse nach dem angegebenen Fabric.</span><span class="sxs-lookup"><span data-stu-id="97486-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97486-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="97486-132">-FabricId</span></span>
<span data-ttu-id="97486-133">Gibt die zu filternde fabricId an.</span><span class="sxs-lookup"><span data-stu-id="97486-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97486-134">-Name</span><span class="sxs-lookup"><span data-stu-id="97486-134">-Name</span></span>
<span data-ttu-id="97486-135">Gibt den Namen des Ereignisses für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="97486-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97486-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97486-136">-ResourceId</span></span>
<span data-ttu-id="97486-137">Gibt das Ereignis "ResourceId" des Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="97486-137">Specifies the event ResourceId of event.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97486-138">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="97486-138">-Severity</span></span>
<span data-ttu-id="97486-139">Der Schweregrad des Ereignisses, nach dem gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="97486-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97486-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="97486-140">-StartTime</span></span>
<span data-ttu-id="97486-141">Gibt die Startzeit des Suchfensters an.</span><span class="sxs-lookup"><span data-stu-id="97486-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="97486-142">Verwenden Sie diesen Parameter, um nur die Ereignisse zu erhalten, die nach der angegebenen Uhrzeit aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="97486-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97486-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97486-143">CommonParameters</span></span>
<span data-ttu-id="97486-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97486-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97486-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97486-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97486-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97486-146">INPUTS</span></span>

### <span data-ttu-id="97486-147">System.String</span><span class="sxs-lookup"><span data-stu-id="97486-147">System.String</span></span>

## <span data-ttu-id="97486-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97486-148">OUTPUTS</span></span>

### <span data-ttu-id="97486-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span><span class="sxs-lookup"><span data-stu-id="97486-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="97486-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="97486-150">NOTES</span></span>

## <span data-ttu-id="97486-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="97486-151">RELATED LINKS</span></span>
