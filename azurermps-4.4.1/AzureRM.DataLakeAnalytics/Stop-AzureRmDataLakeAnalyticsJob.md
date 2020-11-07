---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: a0848ffc888b4812a28198749417d0b0894a5d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664771"
---
# <span data-ttu-id="4ed40-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4ed40-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="4ed40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ed40-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed40-103">Bricht einen Job ab.</span><span class="sxs-lookup"><span data-stu-id="4ed40-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ed40-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ed40-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed40-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ed40-105">DESCRIPTION</span></span>
<span data-ttu-id="4ed40-106">Mit dem Cmdlet " **Stop-AzureRmDataLakeAnalyticsJob** " wird ein Azure Data Lake-Analyse Auftrag abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4ed40-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="4ed40-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ed40-107">EXAMPLES</span></span>

### <span data-ttu-id="4ed40-108">Beispiel 1: Abbrechen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="4ed40-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="4ed40-109">Mit diesem Befehl wird der Auftrag mit der angegebenen ID abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4ed40-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="4ed40-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ed40-110">PARAMETERS</span></span>

### <span data-ttu-id="4ed40-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="4ed40-111">-Account</span></span>
<span data-ttu-id="4ed40-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4ed40-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4ed40-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4ed40-113">-Force</span></span>
<span data-ttu-id="4ed40-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4ed40-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ed40-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="4ed40-115">-JobId</span></span>
<span data-ttu-id="4ed40-116">Gibt die ID des Auftrags an, der abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ed40-116">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="4ed40-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ed40-117">-PassThru</span></span>
<span data-ttu-id="4ed40-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4ed40-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4ed40-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="4ed40-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4ed40-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ed40-120">-Confirm</span></span>
<span data-ttu-id="4ed40-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ed40-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed40-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed40-122">-WhatIf</span></span>
<span data-ttu-id="4ed40-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ed40-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed40-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ed40-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed40-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed40-125">-DefaultProfile</span></span>
<span data-ttu-id="4ed40-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ed40-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed40-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed40-127">CommonParameters</span></span>
<span data-ttu-id="4ed40-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed40-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed40-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed40-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed40-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ed40-130">INPUTS</span></span>

### <span data-ttu-id="4ed40-131">GUID</span><span class="sxs-lookup"><span data-stu-id="4ed40-131">Guid</span></span>
<span data-ttu-id="4ed40-132">Der Parameter "JobID" akzeptiert den Wert vom Typ "GUID" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ed40-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="4ed40-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ed40-133">OUTPUTS</span></span>

### <span data-ttu-id="4ed40-134">bool</span><span class="sxs-lookup"><span data-stu-id="4ed40-134">bool</span></span>
<span data-ttu-id="4ed40-135">Wenn passthru angegeben ist, gibt true nach Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="4ed40-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="4ed40-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ed40-136">NOTES</span></span>

## <span data-ttu-id="4ed40-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ed40-137">RELATED LINKS</span></span>

[<span data-ttu-id="4ed40-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4ed40-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4ed40-139">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4ed40-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4ed40-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4ed40-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


