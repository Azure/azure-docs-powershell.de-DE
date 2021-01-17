---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384276"
---
# <span data-ttu-id="edf98-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="edf98-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="edf98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf98-102">SYNOPSIS</span></span>
<span data-ttu-id="edf98-103">Löscht eine Ausgabe aus einem Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="edf98-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="edf98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edf98-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edf98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edf98-105">DESCRIPTION</span></span>
<span data-ttu-id="edf98-106">Das **Cmdlet "Remove-AzStreamAnalyticsOutput"** löscht asynchron eine Ausgabe aus einem Stream Analytics-Auftrag in Azure.</span><span class="sxs-lookup"><span data-stu-id="edf98-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="edf98-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="edf98-107">EXAMPLES</span></span>

### <span data-ttu-id="edf98-108">BEISPIEL 1: Entfernen einer Ausgabe von einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="edf98-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="edf98-109">Mit diesem Befehl wird die Ausgabe des Auftrags "StreamingJob" entfernt.</span><span class="sxs-lookup"><span data-stu-id="edf98-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="edf98-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edf98-110">PARAMETERS</span></span>

### <span data-ttu-id="edf98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf98-111">-DefaultProfile</span></span>
<span data-ttu-id="edf98-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edf98-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edf98-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="edf98-113">-JobName</span></span>
<span data-ttu-id="edf98-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="edf98-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="edf98-115">-Name</span><span class="sxs-lookup"><span data-stu-id="edf98-115">-Name</span></span>
<span data-ttu-id="edf98-116">Gibt den Namen der Azure Stream Analytics-Ausgabe an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="edf98-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="edf98-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf98-117">-ResourceGroupName</span></span>
<span data-ttu-id="edf98-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="edf98-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="edf98-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edf98-119">-Confirm</span></span>
<span data-ttu-id="edf98-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="edf98-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edf98-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="edf98-121">-WhatIf</span></span>
<span data-ttu-id="edf98-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="edf98-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edf98-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="edf98-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edf98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf98-124">CommonParameters</span></span>
<span data-ttu-id="edf98-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf98-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edf98-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf98-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="edf98-127">INPUTS</span></span>

### <span data-ttu-id="edf98-128">System.String</span><span class="sxs-lookup"><span data-stu-id="edf98-128">System.String</span></span>

## <span data-ttu-id="edf98-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="edf98-129">OUTPUTS</span></span>

### <span data-ttu-id="edf98-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="edf98-130">System.Boolean</span></span>

## <span data-ttu-id="edf98-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="edf98-131">NOTES</span></span>

## <span data-ttu-id="edf98-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="edf98-132">RELATED LINKS</span></span>

[<span data-ttu-id="edf98-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="edf98-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="edf98-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="edf98-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="edf98-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="edf98-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


