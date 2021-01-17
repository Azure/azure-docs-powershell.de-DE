---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d571eb887069aa5c28029dfa98ab022c1d82fc88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306595"
---
# <span data-ttu-id="d297f-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="d297f-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="d297f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d297f-102">SYNOPSIS</span></span>
<span data-ttu-id="d297f-103">Ruft eine Data Lake Analytics Job-Serie oder -Serie ab.</span><span class="sxs-lookup"><span data-stu-id="d297f-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="d297f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d297f-104">SYNTAX</span></span>

### <span data-ttu-id="d297f-105">GetAllInAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="d297f-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d297f-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="d297f-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d297f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d297f-107">DESCRIPTION</span></span>
<span data-ttu-id="d297f-108">Die **Get-AzDataLakeAnalyticsJobRecurrence** ruft eine bestimmte Serie von Azure Data Lake Analytics Job oder eine Liste von Serien ab.</span><span class="sxs-lookup"><span data-stu-id="d297f-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="d297f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d297f-109">EXAMPLES</span></span>

### <span data-ttu-id="d297f-110">Beispiel 1: Erhalten einer angegebenen Serie</span><span class="sxs-lookup"><span data-stu-id="d297f-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="d297f-111">Dieser Befehl ruft die angegebene Aufgabenserie mit der ID '83cb7ad2-3523-4b82-b909-d478b0d8aea3' im Konto 'contosoadla' ab.</span><span class="sxs-lookup"><span data-stu-id="d297f-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="d297f-112">Beispiel 2: Erhalten einer Liste aller Serien im Konto</span><span class="sxs-lookup"><span data-stu-id="d297f-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="d297f-113">Dieser Befehl ruft eine Liste aller Serien im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="d297f-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="d297f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d297f-114">PARAMETERS</span></span>

### <span data-ttu-id="d297f-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="d297f-115">-Account</span></span>
<span data-ttu-id="d297f-116">Der Name des Data Lake Analytics-Kontonamens, unter dem die Aufgabenserie abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d297f-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="d297f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d297f-117">-DefaultProfile</span></span>
<span data-ttu-id="d297f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d297f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d297f-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="d297f-119">-RecurrenceId</span></span>
<span data-ttu-id="d297f-120">DIE ID der bestimmten Auftragsserie, für die Informationen zurücksenend werden.</span><span class="sxs-lookup"><span data-stu-id="d297f-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d297f-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="d297f-121">-SubmittedAfter</span></span>
<span data-ttu-id="d297f-122">Ein optionaler Filter, der Eine/n-Serie(n) zurückgibt, die nur nach der angegebenen Zeit übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="d297f-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="d297f-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="d297f-123">-SubmittedBefore</span></span>
<span data-ttu-id="d297f-124">Ein optionaler Filter, der Eine/n-Serie(n) zurückgibt, die nur vor dem angegebenen Zeitpunkt übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="d297f-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="d297f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d297f-125">CommonParameters</span></span>
<span data-ttu-id="d297f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d297f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d297f-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d297f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d297f-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d297f-128">INPUTS</span></span>

### <span data-ttu-id="d297f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d297f-129">System.String</span></span>

### <span data-ttu-id="d297f-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d297f-130">System.Guid</span></span>

### <span data-ttu-id="d297f-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d297f-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d297f-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d297f-132">OUTPUTS</span></span>

### <span data-ttu-id="d297f-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="d297f-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="d297f-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d297f-134">NOTES</span></span>

## <span data-ttu-id="d297f-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d297f-135">RELATED LINKS</span></span>
