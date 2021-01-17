---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384277"
---
# <span data-ttu-id="03ca3-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="03ca3-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="03ca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="03ca3-103">Löscht eine Eingabe aus einem Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="03ca3-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="03ca3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03ca3-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03ca3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="03ca3-106">Das **Cmdlet "Remove-AzStreamAnalyticsInput"** löscht asynchron eine Eingabe aus einem Stream Analytics-Auftrag in Azure.</span><span class="sxs-lookup"><span data-stu-id="03ca3-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="03ca3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="03ca3-108">BEISPIEL 1: Entfernen eines Eingabedatenstroms aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="03ca3-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="03ca3-109">Mit diesem Befehl wird die Eingabe "EventStream" aus "StreamingJob" entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ca3-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="03ca3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="03ca3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ca3-111">-DefaultProfile</span></span>
<span data-ttu-id="03ca3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03ca3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03ca3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="03ca3-113">-JobName</span></span>
<span data-ttu-id="03ca3-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="03ca3-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="03ca3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="03ca3-115">-Name</span></span>
<span data-ttu-id="03ca3-116">Gibt den Namen der Azure Stream Analytics-Eingabe an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03ca3-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="03ca3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ca3-117">-ResourceGroupName</span></span>
<span data-ttu-id="03ca3-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="03ca3-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="03ca3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03ca3-119">-Confirm</span></span>
<span data-ttu-id="03ca3-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03ca3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03ca3-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="03ca3-121">-WhatIf</span></span>
<span data-ttu-id="03ca3-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03ca3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03ca3-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03ca3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03ca3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ca3-124">CommonParameters</span></span>
<span data-ttu-id="03ca3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ca3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ca3-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ca3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ca3-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03ca3-127">INPUTS</span></span>

### <span data-ttu-id="03ca3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="03ca3-128">System.String</span></span>

## <span data-ttu-id="03ca3-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03ca3-129">OUTPUTS</span></span>

### <span data-ttu-id="03ca3-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03ca3-130">System.Boolean</span></span>

## <span data-ttu-id="03ca3-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="03ca3-131">NOTES</span></span>

## <span data-ttu-id="03ca3-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="03ca3-132">RELATED LINKS</span></span>

[<span data-ttu-id="03ca3-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="03ca3-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="03ca3-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="03ca3-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="03ca3-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="03ca3-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


