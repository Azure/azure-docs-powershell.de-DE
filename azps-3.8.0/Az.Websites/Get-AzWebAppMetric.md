---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 91b5de48805e458b771227ca9c92e9891be170e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845744"
---
# <span data-ttu-id="65024-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="65024-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="65024-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65024-102">SYNOPSIS</span></span>
<span data-ttu-id="65024-103">Ruft Azure Web App-Metriken ab.</span><span class="sxs-lookup"><span data-stu-id="65024-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="65024-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65024-104">SYNTAX</span></span>

### <span data-ttu-id="65024-105">S1</span><span class="sxs-lookup"><span data-stu-id="65024-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65024-106">S2</span><span class="sxs-lookup"><span data-stu-id="65024-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65024-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65024-107">DESCRIPTION</span></span>
<span data-ttu-id="65024-108">Die **Get-AzWebAppMetric** ruft Web App-Metriken ab.</span><span class="sxs-lookup"><span data-stu-id="65024-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="65024-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65024-109">EXAMPLES</span></span>

### <span data-ttu-id="65024-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65024-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="65024-111">Dieser Befehl ruft Anforderungen der Web-App ContosoWebApp pro Minute ab (PT1M-Umfrage Zeit 1 Minute) zwischen Startzeit und EndTime</span><span class="sxs-lookup"><span data-stu-id="65024-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="65024-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="65024-112">PARAMETERS</span></span>

### <span data-ttu-id="65024-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65024-113">-DefaultProfile</span></span>
<span data-ttu-id="65024-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65024-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65024-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="65024-115">-EndTime</span></span>
<span data-ttu-id="65024-116">Endzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="65024-116">End Time in UTC</span></span>

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

### <span data-ttu-id="65024-117">-Granularität</span><span class="sxs-lookup"><span data-stu-id="65024-117">-Granularity</span></span>
<span data-ttu-id="65024-118">Granularität</span><span class="sxs-lookup"><span data-stu-id="65024-118">Granularity</span></span>

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

### <span data-ttu-id="65024-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="65024-119">-InstanceDetails</span></span>
<span data-ttu-id="65024-120">Instanzen Details</span><span class="sxs-lookup"><span data-stu-id="65024-120">Instance Details</span></span>

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

### <span data-ttu-id="65024-121">-Metriken</span><span class="sxs-lookup"><span data-stu-id="65024-121">-Metrics</span></span>
<span data-ttu-id="65024-122">Metriken als Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="65024-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="65024-123">-Name</span><span class="sxs-lookup"><span data-stu-id="65024-123">-Name</span></span>
<span data-ttu-id="65024-124">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="65024-124">WebApp Name</span></span>

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

### <span data-ttu-id="65024-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65024-125">-ResourceGroupName</span></span>
<span data-ttu-id="65024-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="65024-126">Resource Group Name</span></span>

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

### <span data-ttu-id="65024-127">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="65024-127">-StartTime</span></span>
<span data-ttu-id="65024-128">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="65024-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="65024-129">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="65024-129">-WebApp</span></span>
<span data-ttu-id="65024-130">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="65024-130">WebApp object</span></span>

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

### <span data-ttu-id="65024-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65024-131">CommonParameters</span></span>
<span data-ttu-id="65024-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65024-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65024-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65024-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65024-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65024-134">INPUTS</span></span>

### <span data-ttu-id="65024-135">System. String</span><span class="sxs-lookup"><span data-stu-id="65024-135">System.String</span></span>

### <span data-ttu-id="65024-136">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="65024-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="65024-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65024-137">OUTPUTS</span></span>

### <span data-ttu-id="65024-138">Microsoft. Azure. Management. Websites. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="65024-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="65024-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="65024-139">NOTES</span></span>

## <span data-ttu-id="65024-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65024-140">RELATED LINKS</span></span>

[<span data-ttu-id="65024-141">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="65024-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

