---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 3858c2ad6ca90716d5c9140949a683b9c409a105
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950291"
---
# <span data-ttu-id="0c96a-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0c96a-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="0c96a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c96a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c96a-103">Bricht einen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="0c96a-103">Cancels a job.</span></span>

## <span data-ttu-id="0c96a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c96a-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c96a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c96a-105">DESCRIPTION</span></span>
<span data-ttu-id="0c96a-106">Das **Cmdlet Stop-AzDataLakeAnalyticsJob** bricht einen Azure Data Lake Analytics-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="0c96a-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="0c96a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c96a-107">EXAMPLES</span></span>

### <span data-ttu-id="0c96a-108">Beispiel 1: Abbrechen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="0c96a-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="0c96a-109">Mit diesem Befehl wird der Auftrag mit der angegebenen ID abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="0c96a-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="0c96a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0c96a-110">PARAMETERS</span></span>

### <span data-ttu-id="0c96a-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="0c96a-111">-Account</span></span>
<span data-ttu-id="0c96a-112">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="0c96a-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0c96a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c96a-113">-DefaultProfile</span></span>
<span data-ttu-id="0c96a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0c96a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c96a-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="0c96a-115">-Force</span></span>
<span data-ttu-id="0c96a-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="0c96a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c96a-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="0c96a-117">-JobId</span></span>
<span data-ttu-id="0c96a-118">Gibt die ID des zu stornierenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="0c96a-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="0c96a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c96a-119">-PassThru</span></span>
<span data-ttu-id="0c96a-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0c96a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0c96a-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0c96a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0c96a-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0c96a-122">-Confirm</span></span>
<span data-ttu-id="0c96a-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c96a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c96a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c96a-124">-WhatIf</span></span>
<span data-ttu-id="0c96a-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c96a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c96a-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c96a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c96a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c96a-127">CommonParameters</span></span>
<span data-ttu-id="0c96a-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c96a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c96a-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c96a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c96a-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c96a-130">INPUTS</span></span>

### <span data-ttu-id="0c96a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0c96a-131">System.String</span></span>

### <span data-ttu-id="0c96a-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0c96a-132">System.Guid</span></span>

### <span data-ttu-id="0c96a-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0c96a-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0c96a-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c96a-134">OUTPUTS</span></span>

### <span data-ttu-id="0c96a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c96a-135">System.Boolean</span></span>

## <span data-ttu-id="0c96a-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0c96a-136">NOTES</span></span>

## <span data-ttu-id="0c96a-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0c96a-137">RELATED LINKS</span></span>

[<span data-ttu-id="0c96a-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0c96a-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="0c96a-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0c96a-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="0c96a-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0c96a-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


