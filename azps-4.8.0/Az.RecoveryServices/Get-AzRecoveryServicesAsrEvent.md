---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 8ed57766ba36607503994d331cec5381d9f43bbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174228"
---
# <span data-ttu-id="31fb2-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="31fb2-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="31fb2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="31fb2-103">Ruft Details zu Azure Site Recovery-Ereignissen im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="31fb2-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="31fb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31fb2-104">SYNTAX</span></span>

### <span data-ttu-id="31fb2-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="31fb2-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31fb2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="31fb2-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31fb2-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="31fb2-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31fb2-108">ByName</span><span class="sxs-lookup"><span data-stu-id="31fb2-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31fb2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31fb2-109">DESCRIPTION</span></span>
<span data-ttu-id="31fb2-110">Der **Get-AzRecoveryServicesAsrEvent** Ruft die Liste der Ereignisse im Tresor basierend auf den angegebenen Auswahl Filtern ab.</span><span class="sxs-lookup"><span data-stu-id="31fb2-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="31fb2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31fb2-111">EXAMPLES</span></span>

### <span data-ttu-id="31fb2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="31fb2-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="31fb2-113">Liste aller Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="31fb2-113">List of all events.</span></span>

### <span data-ttu-id="31fb2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="31fb2-114">Example 2</span></span>
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

<span data-ttu-id="31fb2-115">Ereignis mit Namen abrufen.</span><span class="sxs-lookup"><span data-stu-id="31fb2-115">Get event by name.</span></span>

### <span data-ttu-id="31fb2-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="31fb2-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="31fb2-117">Liste des Ereignisses für das betroffene Objekt.</span><span class="sxs-lookup"><span data-stu-id="31fb2-117">List of event for affected Object.</span></span>

### <span data-ttu-id="31fb2-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="31fb2-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="31fb2-119">Liste der Ereignisse zwischen Startzeit und Endzeit, Schweregrad kritischer und Integritäts VmHealth.</span><span class="sxs-lookup"><span data-stu-id="31fb2-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="31fb2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="31fb2-120">PARAMETERS</span></span>

### <span data-ttu-id="31fb2-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="31fb2-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="31fb2-122">Gibt "affected FriendlyName" für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="31fb2-122">Specifies AffectedObject FriendlyName for the search.</span></span>

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

### <span data-ttu-id="31fb2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31fb2-123">-DefaultProfile</span></span>
<span data-ttu-id="31fb2-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31fb2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31fb2-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="31fb2-125">-EndTime</span></span>
<span data-ttu-id="31fb2-126">Gibt die Endzeit des Suchfensters an.</span><span class="sxs-lookup"><span data-stu-id="31fb2-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="31fb2-127">Verwenden Sie diesen Parameter, um nur die Ereignisse abzurufen, die vor der angegebenen Uhrzeit aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="31fb2-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

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

### <span data-ttu-id="31fb2-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="31fb2-128">-EventType</span></span>
<span data-ttu-id="31fb2-129">Filtern von Ereignissen nach dem Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="31fb2-129">Filter events by the event type.</span></span>

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

### <span data-ttu-id="31fb2-130">-Stoff</span><span class="sxs-lookup"><span data-stu-id="31fb2-130">-Fabric</span></span>
<span data-ttu-id="31fb2-131">Filtern von Ereignissen nach dem angegebenen Fabric</span><span class="sxs-lookup"><span data-stu-id="31fb2-131">Filter events by the specified fabric.</span></span>

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

### <span data-ttu-id="31fb2-132">-Fabric-Nr</span><span class="sxs-lookup"><span data-stu-id="31fb2-132">-FabricId</span></span>
<span data-ttu-id="31fb2-133">Gibt die zu filternde Fabric-Nr an.</span><span class="sxs-lookup"><span data-stu-id="31fb2-133">Specifies the fabricId to filter.</span></span>

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

### <span data-ttu-id="31fb2-134">-Name</span><span class="sxs-lookup"><span data-stu-id="31fb2-134">-Name</span></span>
<span data-ttu-id="31fb2-135">Gibt den Namen des Ereignisses für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="31fb2-135">Specifies name of the event for search.</span></span>

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

### <span data-ttu-id="31fb2-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="31fb2-136">-ResourceId</span></span>
<span data-ttu-id="31fb2-137">Gibt die Ereignis-Quell-Nr des Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="31fb2-137">Specifies the event ResourceId of event.</span></span>

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

### <span data-ttu-id="31fb2-138">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="31fb2-138">-Severity</span></span>
<span data-ttu-id="31fb2-139">Der Ereignisschweregrad, nach dem gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="31fb2-139">Event severity to filter on.</span></span>

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

### <span data-ttu-id="31fb2-140">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="31fb2-140">-StartTime</span></span>
<span data-ttu-id="31fb2-141">Gibt die Startzeit des Suchfensters an.</span><span class="sxs-lookup"><span data-stu-id="31fb2-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="31fb2-142">Verwenden Sie diesen Parameter, um nur die Ereignisse abzurufen, die nach der angegebenen Zeit aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="31fb2-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

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

### <span data-ttu-id="31fb2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31fb2-143">CommonParameters</span></span>
<span data-ttu-id="31fb2-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31fb2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31fb2-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31fb2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31fb2-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31fb2-146">INPUTS</span></span>

### <span data-ttu-id="31fb2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="31fb2-147">System.String</span></span>

## <span data-ttu-id="31fb2-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31fb2-148">OUTPUTS</span></span>

### <span data-ttu-id="31fb2-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASREvent</span><span class="sxs-lookup"><span data-stu-id="31fb2-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="31fb2-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="31fb2-150">NOTES</span></span>

## <span data-ttu-id="31fb2-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31fb2-151">RELATED LINKS</span></span>
