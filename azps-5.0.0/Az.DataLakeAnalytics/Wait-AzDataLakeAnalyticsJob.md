---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297957"
---
# <span data-ttu-id="1b6e1-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1b6e1-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="1b6e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6e1-103">Wartet, bis ein Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1b6e1-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="1b6e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b6e1-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b6e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b6e1-105">DESCRIPTION</span></span>
<span data-ttu-id="1b6e1-106">Das **Wait-AzDataLakeAnalyticsJob-** Cmdlet wartet darauf, dass ein Azure Data Lake-Analyse Auftrag abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="1b6e1-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="1b6e1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b6e1-107">EXAMPLES</span></span>

### <span data-ttu-id="1b6e1-108">Beispiel 1: warten Sie, bis ein Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1b6e1-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="1b6e1-109">Der folgende Befehl wartet auf den Auftrag mit der angegebenen ID, um ihn abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1b6e1-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="1b6e1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b6e1-110">PARAMETERS</span></span>

### <span data-ttu-id="1b6e1-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1b6e1-111">-Account</span></span>
<span data-ttu-id="1b6e1-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="1b6e1-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1b6e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6e1-113">-DefaultProfile</span></span>
<span data-ttu-id="1b6e1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1b6e1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b6e1-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="1b6e1-115">-JobId</span></span>
<span data-ttu-id="1b6e1-116">Gibt die ID des Auftrags an, für den gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b6e1-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="1b6e1-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="1b6e1-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="1b6e1-118">Gibt die Anzahl der Sekunden an, die gewartet werden muss, bevor der Wait-Vorgang beendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b6e1-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="1b6e1-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1b6e1-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="1b6e1-120">Geben Sie an, wie viele Sekunden zwischen jeder Prüfung des Auftragsstatus verstreichen soll.</span><span class="sxs-lookup"><span data-stu-id="1b6e1-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="1b6e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6e1-121">CommonParameters</span></span>
<span data-ttu-id="1b6e1-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6e1-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6e1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6e1-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b6e1-124">INPUTS</span></span>

### <span data-ttu-id="1b6e1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1b6e1-125">System.String</span></span>

### <span data-ttu-id="1b6e1-126">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1b6e1-126">System.Guid</span></span>

### <span data-ttu-id="1b6e1-127">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1b6e1-127">System.Int32</span></span>

## <span data-ttu-id="1b6e1-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b6e1-128">OUTPUTS</span></span>

### <span data-ttu-id="1b6e1-129">Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="1b6e1-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="1b6e1-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b6e1-130">NOTES</span></span>

## <span data-ttu-id="1b6e1-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b6e1-131">RELATED LINKS</span></span>

[<span data-ttu-id="1b6e1-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1b6e1-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="1b6e1-133">Stopp-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1b6e1-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="1b6e1-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1b6e1-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


