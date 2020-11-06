---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b6c703b1c3373e4e0f1347d9bb2a9819ac1e5de6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497205"
---
# <span data-ttu-id="65390-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65390-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="65390-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65390-102">SYNOPSIS</span></span>
<span data-ttu-id="65390-103">Entfernt einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="65390-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65390-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65390-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65390-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65390-105">DESCRIPTION</span></span>
<span data-ttu-id="65390-106">Das Cmdlet **Remove-AzureRmStreamAnalyticsJob** löscht einen bestimmten Datenstrom Analyse Auftrag in Azure asynchron.</span><span class="sxs-lookup"><span data-stu-id="65390-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="65390-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65390-107">EXAMPLES</span></span>

### <span data-ttu-id="65390-108">Beispiel 1: Entfernen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="65390-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="65390-109">Dieser Befehl entfernt den Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="65390-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="65390-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65390-110">PARAMETERS</span></span>

### <span data-ttu-id="65390-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65390-111">-DefaultProfile</span></span>
<span data-ttu-id="65390-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65390-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65390-113">-Name</span><span class="sxs-lookup"><span data-stu-id="65390-113">-Name</span></span>
<span data-ttu-id="65390-114">Gibt den Namen des zu entfernenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="65390-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65390-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65390-115">-ResourceGroupName</span></span>
<span data-ttu-id="65390-116">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="65390-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65390-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65390-117">-Confirm</span></span>
<span data-ttu-id="65390-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65390-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65390-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65390-119">-WhatIf</span></span>
<span data-ttu-id="65390-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65390-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65390-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65390-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65390-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65390-122">CommonParameters</span></span>
<span data-ttu-id="65390-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65390-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65390-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65390-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65390-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65390-125">INPUTS</span></span>

### <span data-ttu-id="65390-126">System. String</span><span class="sxs-lookup"><span data-stu-id="65390-126">System.String</span></span>

## <span data-ttu-id="65390-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65390-127">OUTPUTS</span></span>

### <span data-ttu-id="65390-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65390-128">System.Boolean</span></span>

## <span data-ttu-id="65390-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="65390-129">NOTES</span></span>

## <span data-ttu-id="65390-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65390-130">RELATED LINKS</span></span>

[<span data-ttu-id="65390-131">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65390-131">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="65390-132">Neu – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65390-132">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="65390-133">Anfang-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65390-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="65390-134">Stopp-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="65390-134">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


