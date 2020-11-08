---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176373"
---
# <span data-ttu-id="9c23e-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9c23e-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="9c23e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c23e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c23e-103">Entfernt einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="9c23e-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="9c23e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c23e-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c23e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c23e-105">DESCRIPTION</span></span>
<span data-ttu-id="9c23e-106">Das Cmdlet **Remove-AzStreamAnalyticsJob** löscht einen bestimmten Datenstrom Analyse Auftrag in Azure asynchron.</span><span class="sxs-lookup"><span data-stu-id="9c23e-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="9c23e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c23e-107">EXAMPLES</span></span>

### <span data-ttu-id="9c23e-108">Beispiel 1: Entfernen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="9c23e-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="9c23e-109">Dieser Befehl entfernt den Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="9c23e-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="9c23e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c23e-110">PARAMETERS</span></span>

### <span data-ttu-id="9c23e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c23e-111">-DefaultProfile</span></span>
<span data-ttu-id="9c23e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c23e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c23e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9c23e-113">-Name</span></span>
<span data-ttu-id="9c23e-114">Gibt den Namen des zu entfernenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="9c23e-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="9c23e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c23e-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c23e-116">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="9c23e-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="9c23e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c23e-117">-Confirm</span></span>
<span data-ttu-id="9c23e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c23e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c23e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c23e-119">-WhatIf</span></span>
<span data-ttu-id="9c23e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c23e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c23e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c23e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c23e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c23e-122">CommonParameters</span></span>
<span data-ttu-id="9c23e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c23e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c23e-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c23e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c23e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c23e-125">INPUTS</span></span>

### <span data-ttu-id="9c23e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9c23e-126">System.String</span></span>

## <span data-ttu-id="9c23e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c23e-127">OUTPUTS</span></span>

### <span data-ttu-id="9c23e-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c23e-128">System.Boolean</span></span>

## <span data-ttu-id="9c23e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c23e-129">NOTES</span></span>

## <span data-ttu-id="9c23e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c23e-130">RELATED LINKS</span></span>

[<span data-ttu-id="9c23e-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9c23e-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="9c23e-132">Neu – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9c23e-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="9c23e-133">Anfang-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9c23e-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="9c23e-134">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9c23e-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


