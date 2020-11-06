---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 47fa876ff021dd920627ce4f08089c5fd04fb885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481917"
---
# <span data-ttu-id="81a48-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="81a48-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="81a48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81a48-102">SYNOPSIS</span></span>
<span data-ttu-id="81a48-103">Ruft Azure Web App-Metriken ab.</span><span class="sxs-lookup"><span data-stu-id="81a48-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81a48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81a48-104">SYNTAX</span></span>

### <span data-ttu-id="81a48-105">S1</span><span class="sxs-lookup"><span data-stu-id="81a48-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81a48-106">S2</span><span class="sxs-lookup"><span data-stu-id="81a48-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81a48-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81a48-107">DESCRIPTION</span></span>
<span data-ttu-id="81a48-108">Die **Get-AzureRmWebAppMetrics** ruft Web App-Metriken ab.</span><span class="sxs-lookup"><span data-stu-id="81a48-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="81a48-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81a48-109">EXAMPLES</span></span>

### <span data-ttu-id="81a48-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81a48-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="81a48-111">Dieser Befehl ruft Anforderungen der Web-App ContosoWebApp pro Minute ab (PT1M-Umfrage Zeit 1 Minute) zwischen Startzeit und EndTime</span><span class="sxs-lookup"><span data-stu-id="81a48-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="81a48-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="81a48-112">PARAMETERS</span></span>

### <span data-ttu-id="81a48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a48-113">-DefaultProfile</span></span>
<span data-ttu-id="81a48-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81a48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a48-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="81a48-115">-EndTime</span></span>
<span data-ttu-id="81a48-116">Endzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="81a48-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a48-117">-Granularität</span><span class="sxs-lookup"><span data-stu-id="81a48-117">-Granularity</span></span>
<span data-ttu-id="81a48-118">Granularität</span><span class="sxs-lookup"><span data-stu-id="81a48-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a48-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="81a48-119">-InstanceDetails</span></span>
<span data-ttu-id="81a48-120">Instanzen Details</span><span class="sxs-lookup"><span data-stu-id="81a48-120">Instance Details</span></span>

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

### <span data-ttu-id="81a48-121">-Metriken</span><span class="sxs-lookup"><span data-stu-id="81a48-121">-Metrics</span></span>
<span data-ttu-id="81a48-122">Metriken als Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="81a48-122">Metrics as a string array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a48-123">-Name</span><span class="sxs-lookup"><span data-stu-id="81a48-123">-Name</span></span>
<span data-ttu-id="81a48-124">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="81a48-124">WebApp Name</span></span>

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

### <span data-ttu-id="81a48-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a48-125">-ResourceGroupName</span></span>
<span data-ttu-id="81a48-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="81a48-126">Resource Group Name</span></span>

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

### <span data-ttu-id="81a48-127">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="81a48-127">-StartTime</span></span>
<span data-ttu-id="81a48-128">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="81a48-128">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a48-129">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="81a48-129">-WebApp</span></span>
<span data-ttu-id="81a48-130">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="81a48-130">WebApp object</span></span>

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

### <span data-ttu-id="81a48-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a48-131">CommonParameters</span></span>
<span data-ttu-id="81a48-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a48-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a48-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a48-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a48-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81a48-134">INPUTS</span></span>

### <span data-ttu-id="81a48-135">System. String</span><span class="sxs-lookup"><span data-stu-id="81a48-135">System.String</span></span>

### <span data-ttu-id="81a48-136">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="81a48-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="81a48-137">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="81a48-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="81a48-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81a48-138">OUTPUTS</span></span>

### <span data-ttu-id="81a48-139">Microsoft. Azure. Management. Websites. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="81a48-139">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="81a48-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="81a48-140">NOTES</span></span>

## <span data-ttu-id="81a48-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81a48-141">RELATED LINKS</span></span>

[<span data-ttu-id="81a48-142">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="81a48-142">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

