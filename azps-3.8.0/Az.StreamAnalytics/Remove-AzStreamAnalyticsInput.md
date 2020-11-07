---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846372"
---
# <span data-ttu-id="8af84-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8af84-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="8af84-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8af84-102">SYNOPSIS</span></span>
<span data-ttu-id="8af84-103">Löscht eine Eingabe aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="8af84-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="8af84-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8af84-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af84-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8af84-105">DESCRIPTION</span></span>
<span data-ttu-id="8af84-106">Das Cmdlet **Remove-AzStreamAnalyticsInput** löscht eine Eingabe aus einem Datenstrom Analyse Auftrag in Azure asynchron.</span><span class="sxs-lookup"><span data-stu-id="8af84-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="8af84-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8af84-107">EXAMPLES</span></span>

### <span data-ttu-id="8af84-108">Beispiel 1: Entfernen eines Eingabedatenstroms aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="8af84-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="8af84-109">Dieser Befehl entfernt die Eingabe EventStream aus StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="8af84-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="8af84-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8af84-110">PARAMETERS</span></span>

### <span data-ttu-id="8af84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af84-111">-DefaultProfile</span></span>
<span data-ttu-id="8af84-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8af84-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8af84-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="8af84-113">-JobName</span></span>
<span data-ttu-id="8af84-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="8af84-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="8af84-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8af84-115">-Name</span></span>
<span data-ttu-id="8af84-116">Gibt den Namen der zu entfernenden Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="8af84-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="8af84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af84-117">-ResourceGroupName</span></span>
<span data-ttu-id="8af84-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="8af84-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="8af84-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8af84-119">-Confirm</span></span>
<span data-ttu-id="8af84-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8af84-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af84-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af84-121">-WhatIf</span></span>
<span data-ttu-id="8af84-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8af84-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af84-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8af84-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af84-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af84-124">CommonParameters</span></span>
<span data-ttu-id="8af84-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8af84-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af84-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af84-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af84-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8af84-127">INPUTS</span></span>

### <span data-ttu-id="8af84-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8af84-128">System.String</span></span>

## <span data-ttu-id="8af84-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8af84-129">OUTPUTS</span></span>

### <span data-ttu-id="8af84-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8af84-130">System.Boolean</span></span>

## <span data-ttu-id="8af84-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="8af84-131">NOTES</span></span>

## <span data-ttu-id="8af84-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8af84-132">RELATED LINKS</span></span>

[<span data-ttu-id="8af84-133">Neu – AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8af84-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="8af84-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8af84-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="8af84-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8af84-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


