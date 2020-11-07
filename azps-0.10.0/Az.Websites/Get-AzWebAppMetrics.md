---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
ms.openlocfilehash: 9a3aeabc3eb38127b37ca4ab6a12975c51daea5b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842784"
---
# <span data-ttu-id="f8e85-101">Get-AzWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="f8e85-101">Get-AzWebAppMetrics</span></span>

## <span data-ttu-id="f8e85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8e85-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e85-103">Ruft Azure Web App-Metriken ab.</span><span class="sxs-lookup"><span data-stu-id="f8e85-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="f8e85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8e85-104">SYNTAX</span></span>

### <span data-ttu-id="f8e85-105">S1</span><span class="sxs-lookup"><span data-stu-id="f8e85-105">S1</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8e85-106">S2</span><span class="sxs-lookup"><span data-stu-id="f8e85-106">S2</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8e85-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8e85-107">DESCRIPTION</span></span>
<span data-ttu-id="f8e85-108">Die **Get-AzWebAppMetrics** ruft Web App-Metriken ab.</span><span class="sxs-lookup"><span data-stu-id="f8e85-108">The **Get-AzWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="f8e85-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8e85-109">EXAMPLES</span></span>

### <span data-ttu-id="f8e85-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8e85-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="f8e85-111">Dieser Befehl ruft Anforderungen der Web-App ContosoWebApp pro Minute ab (PT1M-Umfrage Zeit 1 Minute) zwischen Startzeit und EndTime</span><span class="sxs-lookup"><span data-stu-id="f8e85-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="f8e85-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8e85-112">PARAMETERS</span></span>

### <span data-ttu-id="f8e85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e85-113">-DefaultProfile</span></span>
<span data-ttu-id="f8e85-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8e85-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e85-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f8e85-115">-EndTime</span></span>
<span data-ttu-id="f8e85-116">Endzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="f8e85-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e85-117">-Granularität</span><span class="sxs-lookup"><span data-stu-id="f8e85-117">-Granularity</span></span>
<span data-ttu-id="f8e85-118">Granularität</span><span class="sxs-lookup"><span data-stu-id="f8e85-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e85-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="f8e85-119">-InstanceDetails</span></span>
<span data-ttu-id="f8e85-120">Instanzen Details</span><span class="sxs-lookup"><span data-stu-id="f8e85-120">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e85-121">-Metriken</span><span class="sxs-lookup"><span data-stu-id="f8e85-121">-Metrics</span></span>
<span data-ttu-id="f8e85-122">Metriken als Zeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="f8e85-122">Metrics as a string array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e85-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f8e85-123">-Name</span></span>
<span data-ttu-id="f8e85-124">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="f8e85-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8e85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e85-125">-ResourceGroupName</span></span>
<span data-ttu-id="f8e85-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f8e85-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e85-127">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="f8e85-127">-StartTime</span></span>
<span data-ttu-id="f8e85-128">Startzeit in UTC</span><span class="sxs-lookup"><span data-stu-id="f8e85-128">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e85-129">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="f8e85-129">-WebApp</span></span>
<span data-ttu-id="f8e85-130">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="f8e85-130">WebApp object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8e85-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e85-131">CommonParameters</span></span>
<span data-ttu-id="f8e85-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8e85-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e85-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e85-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e85-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8e85-134">INPUTS</span></span>

### <span data-ttu-id="f8e85-135">Website</span><span class="sxs-lookup"><span data-stu-id="f8e85-135">Site</span></span>
<span data-ttu-id="f8e85-136">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8e85-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f8e85-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8e85-137">OUTPUTS</span></span>

## <span data-ttu-id="f8e85-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8e85-138">NOTES</span></span>

## <span data-ttu-id="f8e85-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8e85-139">RELATED LINKS</span></span>

[<span data-ttu-id="f8e85-140">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="f8e85-140">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

