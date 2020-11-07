---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 9e228c2520402f1b8395c6ca4d90909905f6cb0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662341"
---
# <span data-ttu-id="273b6-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="273b6-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="273b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="273b6-102">SYNOPSIS</span></span>
<span data-ttu-id="273b6-103">Löscht eine Eingabe aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="273b6-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="273b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="273b6-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="273b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="273b6-105">DESCRIPTION</span></span>
<span data-ttu-id="273b6-106">Das Cmdlet **Remove-AzureRmStreamAnalyticsInput** löscht eine Eingabe aus einem Datenstrom Analyse Auftrag in Azure asynchron.</span><span class="sxs-lookup"><span data-stu-id="273b6-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="273b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="273b6-107">EXAMPLES</span></span>

### <span data-ttu-id="273b6-108">Beispiel 1: Entfernen eines Eingabedatenstroms aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="273b6-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="273b6-109">Dieser Befehl entfernt die Eingabe EventStream aus StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="273b6-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="273b6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="273b6-110">PARAMETERS</span></span>

### <span data-ttu-id="273b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273b6-111">-DefaultProfile</span></span>
<span data-ttu-id="273b6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="273b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273b6-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="273b6-113">-JobName</span></span>
<span data-ttu-id="273b6-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="273b6-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273b6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="273b6-115">-Name</span></span>
<span data-ttu-id="273b6-116">Gibt den Namen der zu entfernenden Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="273b6-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="273b6-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="273b6-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273b6-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="273b6-119">-Confirm</span></span>
<span data-ttu-id="273b6-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="273b6-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273b6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="273b6-121">-WhatIf</span></span>
<span data-ttu-id="273b6-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="273b6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="273b6-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="273b6-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273b6-124">CommonParameters</span></span>
<span data-ttu-id="273b6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="273b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273b6-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="273b6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273b6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="273b6-127">INPUTS</span></span>

### <span data-ttu-id="273b6-128">Keine</span><span class="sxs-lookup"><span data-stu-id="273b6-128">None</span></span>
<span data-ttu-id="273b6-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="273b6-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="273b6-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="273b6-130">OUTPUTS</span></span>

### <span data-ttu-id="273b6-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="273b6-131">System.Object</span></span>

## <span data-ttu-id="273b6-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="273b6-132">NOTES</span></span>

## <span data-ttu-id="273b6-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="273b6-133">RELATED LINKS</span></span>

[<span data-ttu-id="273b6-134">Neu – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="273b6-134">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="273b6-135">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="273b6-135">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="273b6-136">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="273b6-136">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


