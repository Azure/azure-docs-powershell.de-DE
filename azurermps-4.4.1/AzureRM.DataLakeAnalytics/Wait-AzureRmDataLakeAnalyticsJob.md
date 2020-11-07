---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 672a992dd86fcbd95e17f0795147231b1b62cd5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663969"
---
# <span data-ttu-id="a957d-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a957d-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="a957d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a957d-102">SYNOPSIS</span></span>
<span data-ttu-id="a957d-103">Wartet, bis ein Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a957d-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a957d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a957d-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a957d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a957d-105">DESCRIPTION</span></span>
<span data-ttu-id="a957d-106">Das **Wait-AzureRmDataLakeAnalyticsJob-** Cmdlet wartet darauf, dass ein Azure Data Lake-Analyse Auftrag abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a957d-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="a957d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a957d-107">EXAMPLES</span></span>

### <span data-ttu-id="a957d-108">Beispiel 1: warten Sie, bis ein Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a957d-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="a957d-109">Der folgende Befehl wartet auf den Auftrag mit der angegebenen ID, um ihn abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a957d-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="a957d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a957d-110">PARAMETERS</span></span>

### <span data-ttu-id="a957d-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="a957d-111">-Account</span></span>
<span data-ttu-id="a957d-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a957d-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a957d-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="a957d-113">-JobId</span></span>
<span data-ttu-id="a957d-114">Gibt die ID des Auftrags an, für den gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a957d-114">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a957d-115">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="a957d-115">-TimeoutInSeconds</span></span>
<span data-ttu-id="a957d-116">Gibt die Anzahl der Sekunden an, die gewartet werden muss, bevor der Wait-Vorgang beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a957d-116">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a957d-117">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a957d-117">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="a957d-118">Geben Sie an, wie viele Sekunden zwischen jeder Prüfung des Auftragsstatus verstreichen soll.</span><span class="sxs-lookup"><span data-stu-id="a957d-118">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a957d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a957d-119">-DefaultProfile</span></span>
<span data-ttu-id="a957d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a957d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a957d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a957d-121">CommonParameters</span></span>
<span data-ttu-id="a957d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a957d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a957d-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a957d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a957d-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a957d-124">INPUTS</span></span>

### <span data-ttu-id="a957d-125">GUID</span><span class="sxs-lookup"><span data-stu-id="a957d-125">Guid</span></span>
<span data-ttu-id="a957d-126">Der Parameter "JobID" akzeptiert den Wert vom Typ "GUID" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a957d-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="a957d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a957d-127">OUTPUTS</span></span>

### <span data-ttu-id="a957d-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="a957d-128">JobInformation</span></span>
<span data-ttu-id="a957d-129">Die endgültigen Auftragsdetails für den abgeschlossenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="a957d-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="a957d-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a957d-130">NOTES</span></span>

## <span data-ttu-id="a957d-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a957d-131">RELATED LINKS</span></span>

[<span data-ttu-id="a957d-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a957d-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a957d-133">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a957d-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a957d-134">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a957d-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


