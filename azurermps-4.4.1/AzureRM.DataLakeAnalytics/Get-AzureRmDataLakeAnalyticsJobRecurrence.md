---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: cfc5d0999ed9c77e38b83eee99eabbd19dd1e493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665070"
---
# <span data-ttu-id="e3e7a-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="e3e7a-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="e3e7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e7a-103">Ruft einen Daten See-Analyse Auftrags Serien-oder-Seriendruck ab.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3e7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3e7a-104">SYNTAX</span></span>

### <span data-ttu-id="e3e7a-105">Alle im Konto (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3e7a-105">All In Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3e7a-106">Spezifisches Auftrags Rezidiv</span><span class="sxs-lookup"><span data-stu-id="e3e7a-106">Specific Job Recurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3e7a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3e7a-107">DESCRIPTION</span></span>
<span data-ttu-id="e3e7a-108">Die **Get-AzureRmDataLakeAnalyticsJobRecurrence-** Funktion Ruft eine angegebene Azure Data Lake Analytics-auftragsserie oder eine Liste der Serie ab.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="e3e7a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3e7a-109">EXAMPLES</span></span>

### <span data-ttu-id="e3e7a-110">Beispiel 1: Abrufen einer angegebenen Serie</span><span class="sxs-lookup"><span data-stu-id="e3e7a-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="e3e7a-111">Dieser Befehl ruft die angegebene auftragsserie mit der ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' im Konto ' contosoadla ' ab.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="e3e7a-112">Beispiel 2: Abrufen einer Liste aller Serien im Konto</span><span class="sxs-lookup"><span data-stu-id="e3e7a-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="e3e7a-113">Dieser Befehl ruft eine Liste aller Wiederholungen im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="e3e7a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3e7a-114">PARAMETERS</span></span>

### <span data-ttu-id="e3e7a-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="e3e7a-115">-Account</span></span>
<span data-ttu-id="e3e7a-116">Name des Daten Lake Analytics-Kontonamens, unter dem die auftragsserie abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="e3e7a-117">-Serien-Nr</span><span class="sxs-lookup"><span data-stu-id="e3e7a-117">-RecurrenceId</span></span>
<span data-ttu-id="e3e7a-118">Die ID der jeweiligen auftragsserie, für die Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-118">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific Job Recurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e7a-119">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="e3e7a-119">-SubmittedAfter</span></span>
<span data-ttu-id="e3e7a-120">Ein optionaler Filter, der Auftrags Serien (n) zurückgibt, die nur nach der angegebenen Zeit übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-120">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e7a-121">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="e3e7a-121">-SubmittedBefore</span></span>
<span data-ttu-id="e3e7a-122">Ein optionaler Filter, der Auftrags Serien (n) zurückgibt, die nur vor der angegebenen Zeit übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-122">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e7a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e7a-123">-DefaultProfile</span></span>
<span data-ttu-id="e3e7a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3e7a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e7a-125">CommonParameters</span></span>
<span data-ttu-id="e3e7a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3e7a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e7a-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3e7a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e7a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3e7a-128">INPUTS</span></span>

### <span data-ttu-id="e3e7a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e3e7a-129">System.String</span></span>
<span data-ttu-id="e3e7a-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e3e7a-130">System.Guid</span></span>

## <span data-ttu-id="e3e7a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3e7a-131">OUTPUTS</span></span>

### <span data-ttu-id="e3e7a-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="e3e7a-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="e3e7a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3e7a-133">NOTES</span></span>

## <span data-ttu-id="e3e7a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3e7a-134">RELATED LINKS</span></span>

