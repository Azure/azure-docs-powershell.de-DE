---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150156"
---
# <span data-ttu-id="fbb5f-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="fbb5f-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="fbb5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb5f-103">Löscht eine Ausgabe aus einem Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="fbb5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbb5f-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb5f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbb5f-105">DESCRIPTION</span></span>
<span data-ttu-id="fbb5f-106">Das **Cmdlet "Remove-AzStreamAnalyticsOutput"** löscht asynchron eine Ausgabe aus einem Stream Analytics-Auftrag in Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="fbb5f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbb5f-107">EXAMPLES</span></span>

### <span data-ttu-id="fbb5f-108">BEISPIEL 1: Entfernen einer Ausgabe aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="fbb5f-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="fbb5f-109">Mit diesem Befehl wird die Ausgabe im Auftrag "StreamingJob" entfernt.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="fbb5f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbb5f-110">PARAMETERS</span></span>

### <span data-ttu-id="fbb5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb5f-111">-DefaultProfile</span></span>
<span data-ttu-id="fbb5f-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbb5f-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="fbb5f-113">-JobName</span></span>
<span data-ttu-id="fbb5f-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="fbb5f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fbb5f-115">-Name</span></span>
<span data-ttu-id="fbb5f-116">Gibt den Namen der Azure Stream Analytics-Ausgabe an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb5f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb5f-117">-ResourceGroupName</span></span>
<span data-ttu-id="fbb5f-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="fbb5f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbb5f-119">-Confirm</span></span>
<span data-ttu-id="fbb5f-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb5f-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fbb5f-121">-WhatIf</span></span>
<span data-ttu-id="fbb5f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb5f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb5f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb5f-124">CommonParameters</span></span>
<span data-ttu-id="fbb5f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb5f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb5f-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb5f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb5f-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbb5f-127">INPUTS</span></span>

### <span data-ttu-id="fbb5f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fbb5f-128">System.String</span></span>

## <span data-ttu-id="fbb5f-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbb5f-129">OUTPUTS</span></span>

### <span data-ttu-id="fbb5f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb5f-130">System.Boolean</span></span>

## <span data-ttu-id="fbb5f-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbb5f-131">NOTES</span></span>

## <span data-ttu-id="fbb5f-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbb5f-132">RELATED LINKS</span></span>

[<span data-ttu-id="fbb5f-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="fbb5f-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="fbb5f-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="fbb5f-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="fbb5f-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="fbb5f-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


