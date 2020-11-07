---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 53bd361d67829fdf30741540f1435032067508e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824627"
---
# <span data-ttu-id="29cf9-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="29cf9-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="29cf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="29cf9-103">Löscht eine Ausgabe aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="29cf9-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="29cf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29cf9-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29cf9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="29cf9-106">Das Cmdlet **Remove-AzStreamAnalyticsOutput** löscht eine Ausgabe aus einem Datenstrom Analyse Auftrag in Azure asynchron.</span><span class="sxs-lookup"><span data-stu-id="29cf9-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="29cf9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="29cf9-108">Beispiel 1: Entfernen einer Ausgabe eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="29cf9-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="29cf9-109">Dieser Befehl entfernt die Ausgabe Ausgabe im Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="29cf9-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="29cf9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="29cf9-110">PARAMETERS</span></span>

### <span data-ttu-id="29cf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29cf9-111">-DefaultProfile</span></span>
<span data-ttu-id="29cf9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29cf9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29cf9-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="29cf9-113">-JobName</span></span>
<span data-ttu-id="29cf9-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="29cf9-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="29cf9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="29cf9-115">-Name</span></span>
<span data-ttu-id="29cf9-116">Gibt den Namen der zu entfernenden Azure Stream Analytics-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="29cf9-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="29cf9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29cf9-117">-ResourceGroupName</span></span>
<span data-ttu-id="29cf9-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="29cf9-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="29cf9-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29cf9-119">-Confirm</span></span>
<span data-ttu-id="29cf9-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29cf9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29cf9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29cf9-121">-WhatIf</span></span>
<span data-ttu-id="29cf9-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29cf9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29cf9-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29cf9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29cf9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29cf9-124">CommonParameters</span></span>
<span data-ttu-id="29cf9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29cf9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29cf9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29cf9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29cf9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29cf9-127">INPUTS</span></span>

### <span data-ttu-id="29cf9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="29cf9-128">System.String</span></span>

## <span data-ttu-id="29cf9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29cf9-129">OUTPUTS</span></span>

### <span data-ttu-id="29cf9-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29cf9-130">System.Boolean</span></span>

## <span data-ttu-id="29cf9-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="29cf9-131">NOTES</span></span>

## <span data-ttu-id="29cf9-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29cf9-132">RELATED LINKS</span></span>

[<span data-ttu-id="29cf9-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="29cf9-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="29cf9-134">Neu – AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="29cf9-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="29cf9-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="29cf9-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


