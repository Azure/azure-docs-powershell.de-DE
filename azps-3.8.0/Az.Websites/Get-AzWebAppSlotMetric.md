---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: 27800007756f8de91f23feab2f3cc1bd5206aa76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996549"
---
# <span data-ttu-id="9559c-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="9559c-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="9559c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9559c-102">SYNOPSIS</span></span>
<span data-ttu-id="9559c-103">Ruft Metriken für einen Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="9559c-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="9559c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9559c-104">SYNTAX</span></span>

### <span data-ttu-id="9559c-105">S1</span><span class="sxs-lookup"><span data-stu-id="9559c-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9559c-106">S2</span><span class="sxs-lookup"><span data-stu-id="9559c-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9559c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9559c-107">DESCRIPTION</span></span>
<span data-ttu-id="9559c-108">Der **Get-AzWebAppSlotMetric** ruft Web App-Metriken für den angegebenen Slot ab.</span><span class="sxs-lookup"><span data-stu-id="9559c-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="9559c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9559c-109">EXAMPLES</span></span>

### <span data-ttu-id="9559c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9559c-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="9559c-111">Mit diesem Befehl wird die Anforderung der angegebenen Web-App pro Minute (PT1M-Abruf Zeit 1 Minute) zwischen Startzeit und EndTime abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9559c-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="9559c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9559c-112">PARAMETERS</span></span>

### <span data-ttu-id="9559c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9559c-113">-DefaultProfile</span></span>
<span data-ttu-id="9559c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9559c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9559c-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9559c-115">-EndTime</span></span>
<span data-ttu-id="9559c-116">Endzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="9559c-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9559c-117">-Granularität</span><span class="sxs-lookup"><span data-stu-id="9559c-117">-Granularity</span></span>
<span data-ttu-id="9559c-118">Granularität</span><span class="sxs-lookup"><span data-stu-id="9559c-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9559c-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="9559c-119">-InstanceDetails</span></span>
<span data-ttu-id="9559c-120">Instanzen Details</span><span class="sxs-lookup"><span data-stu-id="9559c-120">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9559c-121">-Metriken</span><span class="sxs-lookup"><span data-stu-id="9559c-121">-Metrics</span></span>
<span data-ttu-id="9559c-122">Metriken</span><span class="sxs-lookup"><span data-stu-id="9559c-122">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9559c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9559c-123">-Name</span></span>
<span data-ttu-id="9559c-124">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9559c-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9559c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9559c-125">-ResourceGroupName</span></span>
<span data-ttu-id="9559c-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9559c-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9559c-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="9559c-127">-Slot</span></span>
<span data-ttu-id="9559c-128">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="9559c-128">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9559c-129">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="9559c-129">-StartTime</span></span>
<span data-ttu-id="9559c-130">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="9559c-130">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9559c-131">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9559c-131">-WebApp</span></span>
<span data-ttu-id="9559c-132">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="9559c-132">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9559c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9559c-133">CommonParameters</span></span>
<span data-ttu-id="9559c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9559c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9559c-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9559c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9559c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9559c-136">INPUTS</span></span>

### <span data-ttu-id="9559c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9559c-137">System.String</span></span>

### <span data-ttu-id="9559c-138">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9559c-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9559c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9559c-139">OUTPUTS</span></span>

### <span data-ttu-id="9559c-140">Microsoft. Azure. Management. Websites. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="9559c-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="9559c-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9559c-141">NOTES</span></span>

## <span data-ttu-id="9559c-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9559c-142">RELATED LINKS</span></span>

[<span data-ttu-id="9559c-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="9559c-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="9559c-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9559c-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="9559c-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9559c-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
