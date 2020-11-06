---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c336c1bb2c2485c5bef691a5d5560a1b8795360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475861"
---
# <span data-ttu-id="0a76f-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="0a76f-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="0a76f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a76f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a76f-103">Ruft Metriken für einen Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="0a76f-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a76f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a76f-104">SYNTAX</span></span>

### <span data-ttu-id="0a76f-105">S1</span><span class="sxs-lookup"><span data-stu-id="0a76f-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a76f-106">S2</span><span class="sxs-lookup"><span data-stu-id="0a76f-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a76f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a76f-107">DESCRIPTION</span></span>
<span data-ttu-id="0a76f-108">Der **Get-AzureRmWebAppSlotMetrics** ruft Web App-Metriken für den angegebenen Slot ab.</span><span class="sxs-lookup"><span data-stu-id="0a76f-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="0a76f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a76f-109">EXAMPLES</span></span>

### <span data-ttu-id="0a76f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a76f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="0a76f-111">Mit diesem Befehl wird die Anforderung der angegebenen Web-App pro Minute (PT1M-Abruf Zeit 1 Minute) zwischen Startzeit und EndTime abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0a76f-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="0a76f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a76f-112">PARAMETERS</span></span>

### <span data-ttu-id="0a76f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a76f-113">-DefaultProfile</span></span>
<span data-ttu-id="0a76f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a76f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a76f-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0a76f-115">-EndTime</span></span>
<span data-ttu-id="0a76f-116">Endzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="0a76f-116">End Time in UTC</span></span>

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

### <span data-ttu-id="0a76f-117">-Granularität</span><span class="sxs-lookup"><span data-stu-id="0a76f-117">-Granularity</span></span>
<span data-ttu-id="0a76f-118">Granularität</span><span class="sxs-lookup"><span data-stu-id="0a76f-118">Granularity</span></span>

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

### <span data-ttu-id="0a76f-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="0a76f-119">-InstanceDetails</span></span>
<span data-ttu-id="0a76f-120">Instanzen Details</span><span class="sxs-lookup"><span data-stu-id="0a76f-120">Instance Details</span></span>

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

### <span data-ttu-id="0a76f-121">-Metriken</span><span class="sxs-lookup"><span data-stu-id="0a76f-121">-Metrics</span></span>
<span data-ttu-id="0a76f-122">Metriken</span><span class="sxs-lookup"><span data-stu-id="0a76f-122">Metrics</span></span>

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

### <span data-ttu-id="0a76f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0a76f-123">-Name</span></span>
<span data-ttu-id="0a76f-124">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="0a76f-124">WebApp Name</span></span>

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

### <span data-ttu-id="0a76f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a76f-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a76f-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0a76f-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0a76f-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="0a76f-127">-Slot</span></span>
<span data-ttu-id="0a76f-128">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="0a76f-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0a76f-129">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="0a76f-129">-StartTime</span></span>
<span data-ttu-id="0a76f-130">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="0a76f-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="0a76f-131">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="0a76f-131">-WebApp</span></span>
<span data-ttu-id="0a76f-132">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="0a76f-132">WebApp Object</span></span>

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

### <span data-ttu-id="0a76f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a76f-133">CommonParameters</span></span>
<span data-ttu-id="0a76f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a76f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a76f-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a76f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a76f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a76f-136">INPUTS</span></span>

### <span data-ttu-id="0a76f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0a76f-137">System.String</span></span>

### <span data-ttu-id="0a76f-138">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="0a76f-138">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="0a76f-139">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="0a76f-139">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="0a76f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a76f-140">OUTPUTS</span></span>

### <span data-ttu-id="0a76f-141">Microsoft. Azure. Management. Websites. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="0a76f-141">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="0a76f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a76f-142">NOTES</span></span>

## <span data-ttu-id="0a76f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a76f-143">RELATED LINKS</span></span>

[<span data-ttu-id="0a76f-144">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="0a76f-144">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="0a76f-145">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0a76f-145">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="0a76f-146">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a76f-146">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
