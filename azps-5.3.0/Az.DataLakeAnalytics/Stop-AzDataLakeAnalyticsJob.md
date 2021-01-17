---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472541"
---
# <span data-ttu-id="7f07c-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7f07c-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="7f07c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f07c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f07c-103">Bricht einen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="7f07c-103">Cancels a job.</span></span>

## <span data-ttu-id="7f07c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f07c-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f07c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f07c-105">DESCRIPTION</span></span>
<span data-ttu-id="7f07c-106">Das **Cmdlet "Stop-AzDataLakeAnalyticsJob"** bricht einen Azure Data Lake Analytics-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="7f07c-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="7f07c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f07c-107">EXAMPLES</span></span>

### <span data-ttu-id="7f07c-108">Beispiel 1: Abbrechen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="7f07c-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="7f07c-109">Dieser Befehl bricht den Auftrag mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="7f07c-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="7f07c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f07c-110">PARAMETERS</span></span>

### <span data-ttu-id="7f07c-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="7f07c-111">-Account</span></span>
<span data-ttu-id="7f07c-112">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="7f07c-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="7f07c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f07c-113">-DefaultProfile</span></span>
<span data-ttu-id="7f07c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7f07c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f07c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7f07c-115">-Force</span></span>
<span data-ttu-id="7f07c-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="7f07c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f07c-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="7f07c-117">-JobId</span></span>
<span data-ttu-id="7f07c-118">Gibt die ID des zu abbrechenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="7f07c-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="7f07c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f07c-119">-PassThru</span></span>
<span data-ttu-id="7f07c-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7f07c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7f07c-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7f07c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7f07c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f07c-122">-Confirm</span></span>
<span data-ttu-id="7f07c-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f07c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f07c-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7f07c-124">-WhatIf</span></span>
<span data-ttu-id="7f07c-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f07c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f07c-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f07c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f07c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f07c-127">CommonParameters</span></span>
<span data-ttu-id="7f07c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f07c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f07c-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f07c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f07c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f07c-130">INPUTS</span></span>

### <span data-ttu-id="7f07c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7f07c-131">System.String</span></span>

### <span data-ttu-id="7f07c-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7f07c-132">System.Guid</span></span>

### <span data-ttu-id="7f07c-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f07c-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f07c-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f07c-134">OUTPUTS</span></span>

### <span data-ttu-id="7f07c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f07c-135">System.Boolean</span></span>

## <span data-ttu-id="7f07c-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f07c-136">NOTES</span></span>

## <span data-ttu-id="7f07c-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f07c-137">RELATED LINKS</span></span>

[<span data-ttu-id="7f07c-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7f07c-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="7f07c-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7f07c-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="7f07c-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7f07c-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


