---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500453"
---
# <span data-ttu-id="830c2-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="830c2-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="830c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="830c2-102">SYNOPSIS</span></span>
<span data-ttu-id="830c2-103">Ruft Details zu Azure Site Recovery-Ereignissen im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="830c2-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="830c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="830c2-104">SYNTAX</span></span>

### <span data-ttu-id="830c2-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="830c2-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="830c2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="830c2-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="830c2-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="830c2-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="830c2-108">ByName</span><span class="sxs-lookup"><span data-stu-id="830c2-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="830c2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="830c2-109">DESCRIPTION</span></span>
<span data-ttu-id="830c2-110">Der **Get-AzureRmRecoveryServicesAsrEvent** Ruft die Liste der Ereignisse im Tresor basierend auf den angegebenen Auswahl Filtern ab.</span><span class="sxs-lookup"><span data-stu-id="830c2-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="830c2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="830c2-111">EXAMPLES</span></span>

### <span data-ttu-id="830c2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="830c2-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="830c2-113">Liste aller Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="830c2-113">List of all events.</span></span>

### <span data-ttu-id="830c2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="830c2-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


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

<span data-ttu-id="830c2-115">Ereignis mit Namen abrufen.</span><span class="sxs-lookup"><span data-stu-id="830c2-115">Get event by name.</span></span>

### <span data-ttu-id="830c2-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="830c2-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="830c2-117">Liste des Ereignisses für das betroffene Objekt.</span><span class="sxs-lookup"><span data-stu-id="830c2-117">List of event for affected Object.</span></span>

### <span data-ttu-id="830c2-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="830c2-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="830c2-119">Liste der Ereignisse zwischen Startzeit und Endzeit, Schweregrad kritischer und Integritäts VmHealth.</span><span class="sxs-lookup"><span data-stu-id="830c2-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="830c2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="830c2-120">PARAMETERS</span></span>

### <span data-ttu-id="830c2-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="830c2-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="830c2-122">Gibt "affected FriendlyName" für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="830c2-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830c2-123">-DefaultProfile</span></span>
<span data-ttu-id="830c2-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="830c2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="830c2-125">-EndTime</span></span>
<span data-ttu-id="830c2-126">Gibt die Endzeit des Suchfensters an.</span><span class="sxs-lookup"><span data-stu-id="830c2-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="830c2-127">Verwenden Sie diesen Parameter, um nur die Ereignisse abzurufen, die vor der angegebenen Uhrzeit aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="830c2-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="830c2-128">-EventType</span></span>
<span data-ttu-id="830c2-129">Filtern von Ereignissen nach dem Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="830c2-129">Filter events by the event type.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-130">-Stoff</span><span class="sxs-lookup"><span data-stu-id="830c2-130">-Fabric</span></span>
<span data-ttu-id="830c2-131">Filtern von Ereignissen nach dem angegebenen Fabric</span><span class="sxs-lookup"><span data-stu-id="830c2-131">Filter events by the specified fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-132">-Fabric-Nr</span><span class="sxs-lookup"><span data-stu-id="830c2-132">-FabricId</span></span>
<span data-ttu-id="830c2-133">Gibt die zu filternde Fabric-Nr an.</span><span class="sxs-lookup"><span data-stu-id="830c2-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-134">-Name</span><span class="sxs-lookup"><span data-stu-id="830c2-134">-Name</span></span>
<span data-ttu-id="830c2-135">Gibt den Namen des Ereignisses für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="830c2-135">Specifies name of the event for search.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="830c2-136">-ResourceId</span></span>
<span data-ttu-id="830c2-137">Gibt an Ereignis ReourceId.</span><span class="sxs-lookup"><span data-stu-id="830c2-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-138">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="830c2-138">-Severity</span></span>
<span data-ttu-id="830c2-139">Der Ereignisschweregrad, nach dem gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="830c2-139">Event severity to filter on.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-140">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="830c2-140">-StartTime</span></span>
<span data-ttu-id="830c2-141">Gibt die Startzeit des Suchfensters an.</span><span class="sxs-lookup"><span data-stu-id="830c2-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="830c2-142">Verwenden Sie diesen Parameter, um nur die Ereignisse abzurufen, die nach der angegebenen Zeit aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="830c2-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830c2-143">CommonParameters</span></span>
<span data-ttu-id="830c2-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830c2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830c2-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="830c2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830c2-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="830c2-146">INPUTS</span></span>

### <span data-ttu-id="830c2-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="830c2-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="830c2-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="830c2-148">OUTPUTS</span></span>

### <span data-ttu-id="830c2-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASREvent, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="830c2-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="830c2-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="830c2-150">NOTES</span></span>

## <span data-ttu-id="830c2-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="830c2-151">RELATED LINKS</span></span>
