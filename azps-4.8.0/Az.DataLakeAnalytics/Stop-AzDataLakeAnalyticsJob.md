---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165847"
---
# <span data-ttu-id="817d2-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="817d2-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="817d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="817d2-102">SYNOPSIS</span></span>
<span data-ttu-id="817d2-103">Bricht einen Job ab.</span><span class="sxs-lookup"><span data-stu-id="817d2-103">Cancels a job.</span></span>

## <span data-ttu-id="817d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="817d2-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="817d2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="817d2-105">DESCRIPTION</span></span>
<span data-ttu-id="817d2-106">Mit dem Cmdlet " **Stop-AzDataLakeAnalyticsJob** " wird ein Azure Data Lake-Analyse Auftrag abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="817d2-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="817d2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="817d2-107">EXAMPLES</span></span>

### <span data-ttu-id="817d2-108">Beispiel 1: Abbrechen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="817d2-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="817d2-109">Mit diesem Befehl wird der Auftrag mit der angegebenen ID abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="817d2-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="817d2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="817d2-110">PARAMETERS</span></span>

### <span data-ttu-id="817d2-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="817d2-111">-Account</span></span>
<span data-ttu-id="817d2-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="817d2-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="817d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817d2-113">-DefaultProfile</span></span>
<span data-ttu-id="817d2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="817d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="817d2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="817d2-115">-Force</span></span>
<span data-ttu-id="817d2-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="817d2-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817d2-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="817d2-117">-JobId</span></span>
<span data-ttu-id="817d2-118">Gibt die ID des Auftrags an, der abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="817d2-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="817d2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="817d2-119">-PassThru</span></span>
<span data-ttu-id="817d2-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="817d2-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="817d2-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="817d2-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817d2-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="817d2-122">-Confirm</span></span>
<span data-ttu-id="817d2-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="817d2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817d2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="817d2-124">-WhatIf</span></span>
<span data-ttu-id="817d2-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="817d2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="817d2-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="817d2-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817d2-127">CommonParameters</span></span>
<span data-ttu-id="817d2-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="817d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817d2-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="817d2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817d2-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="817d2-130">INPUTS</span></span>

### <span data-ttu-id="817d2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="817d2-131">System.String</span></span>

### <span data-ttu-id="817d2-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="817d2-132">System.Guid</span></span>

### <span data-ttu-id="817d2-133">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="817d2-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="817d2-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="817d2-134">OUTPUTS</span></span>

### <span data-ttu-id="817d2-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="817d2-135">System.Boolean</span></span>

## <span data-ttu-id="817d2-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="817d2-136">NOTES</span></span>

## <span data-ttu-id="817d2-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="817d2-137">RELATED LINKS</span></span>

[<span data-ttu-id="817d2-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="817d2-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="817d2-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="817d2-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="817d2-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="817d2-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


