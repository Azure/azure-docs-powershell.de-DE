---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 03cca81794e190a97ce21b7e9ed8c82392db3e36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662207"
---
# <span data-ttu-id="95919-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="95919-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="95919-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95919-102">SYNOPSIS</span></span>
<span data-ttu-id="95919-103">Löscht eine Ausgabe aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="95919-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95919-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95919-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95919-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95919-105">DESCRIPTION</span></span>
<span data-ttu-id="95919-106">Das Cmdlet **Remove-AzureRmStreamAnalyticsOutput** löscht eine Ausgabe aus einem Datenstrom Analyse Auftrag in Azure asynchron.</span><span class="sxs-lookup"><span data-stu-id="95919-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="95919-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95919-107">EXAMPLES</span></span>

### <span data-ttu-id="95919-108">Beispiel 1: Entfernen einer Ausgabe eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="95919-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="95919-109">Dieser Befehl entfernt die Ausgabe Ausgabe im Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="95919-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="95919-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95919-110">PARAMETERS</span></span>

### <span data-ttu-id="95919-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95919-111">-DefaultProfile</span></span>
<span data-ttu-id="95919-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95919-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95919-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="95919-113">-JobName</span></span>
<span data-ttu-id="95919-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="95919-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="95919-115">-Name</span><span class="sxs-lookup"><span data-stu-id="95919-115">-Name</span></span>
<span data-ttu-id="95919-116">Gibt den Namen der zu entfernenden Azure Stream Analytics-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="95919-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="95919-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95919-117">-ResourceGroupName</span></span>
<span data-ttu-id="95919-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="95919-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="95919-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95919-119">-Confirm</span></span>
<span data-ttu-id="95919-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95919-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95919-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95919-121">-WhatIf</span></span>
<span data-ttu-id="95919-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95919-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95919-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95919-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95919-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95919-124">CommonParameters</span></span>
<span data-ttu-id="95919-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95919-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95919-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95919-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95919-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95919-127">INPUTS</span></span>

### <span data-ttu-id="95919-128">Keine</span><span class="sxs-lookup"><span data-stu-id="95919-128">None</span></span>
<span data-ttu-id="95919-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="95919-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95919-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95919-130">OUTPUTS</span></span>

### <span data-ttu-id="95919-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="95919-131">System.Object</span></span>

## <span data-ttu-id="95919-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="95919-132">NOTES</span></span>

## <span data-ttu-id="95919-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95919-133">RELATED LINKS</span></span>

[<span data-ttu-id="95919-134">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="95919-134">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="95919-135">Neu – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="95919-135">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="95919-136">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="95919-136">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


