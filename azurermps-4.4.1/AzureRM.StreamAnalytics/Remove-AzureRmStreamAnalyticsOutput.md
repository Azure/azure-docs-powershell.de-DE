---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 9904699d95429e029f330e5c3ca3e5957eb4c35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662389"
---
# <span data-ttu-id="dda1a-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dda1a-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="dda1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dda1a-102">SYNOPSIS</span></span>
<span data-ttu-id="dda1a-103">Löscht eine Ausgabe aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="dda1a-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dda1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dda1a-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda1a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dda1a-105">DESCRIPTION</span></span>
<span data-ttu-id="dda1a-106">Das Cmdlet **Remove-AzureRmStreamAnalyticsOutput** löscht eine Ausgabe aus einem Datenstrom Analyse Auftrag in Azure asynchron.</span><span class="sxs-lookup"><span data-stu-id="dda1a-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="dda1a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dda1a-107">EXAMPLES</span></span>

### <span data-ttu-id="dda1a-108">Beispiel 1: Entfernen einer Ausgabe eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="dda1a-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="dda1a-109">Dieser Befehl entfernt die Ausgabe Ausgabe im Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="dda1a-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="dda1a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dda1a-110">PARAMETERS</span></span>

### <span data-ttu-id="dda1a-111">-Jobname</span><span class="sxs-lookup"><span data-stu-id="dda1a-111">-JobName</span></span>
<span data-ttu-id="dda1a-112">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="dda1a-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="dda1a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dda1a-113">-Name</span></span>
<span data-ttu-id="dda1a-114">Gibt den Namen der zu entfernenden Azure Stream Analytics-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="dda1a-114">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="dda1a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda1a-115">-ResourceGroupName</span></span>
<span data-ttu-id="dda1a-116">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="dda1a-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="dda1a-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dda1a-117">-Confirm</span></span>
<span data-ttu-id="dda1a-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dda1a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda1a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda1a-119">-WhatIf</span></span>
<span data-ttu-id="dda1a-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dda1a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda1a-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dda1a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda1a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda1a-122">-DefaultProfile</span></span>
<span data-ttu-id="dda1a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dda1a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dda1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda1a-124">CommonParameters</span></span>
<span data-ttu-id="dda1a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda1a-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda1a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda1a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dda1a-127">INPUTS</span></span>

## <span data-ttu-id="dda1a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dda1a-128">OUTPUTS</span></span>

### <span data-ttu-id="dda1a-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="dda1a-129">System.Object</span></span>

## <span data-ttu-id="dda1a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="dda1a-130">NOTES</span></span>

## <span data-ttu-id="dda1a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dda1a-131">RELATED LINKS</span></span>

[<span data-ttu-id="dda1a-132">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dda1a-132">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="dda1a-133">Neu – AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dda1a-133">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="dda1a-134">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dda1a-134">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


