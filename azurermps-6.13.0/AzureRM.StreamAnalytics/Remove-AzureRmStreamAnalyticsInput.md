---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8e80162d5efa6aa274617941df218812ae6901a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497209"
---
# <span data-ttu-id="55d9e-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="55d9e-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="55d9e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="55d9e-103">Löscht eine Eingabe aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="55d9e-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55d9e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55d9e-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55d9e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="55d9e-106">Das Cmdlet **Remove-AzureRmStreamAnalyticsInput** löscht eine Eingabe aus einem Datenstrom Analyse Auftrag in Azure asynchron.</span><span class="sxs-lookup"><span data-stu-id="55d9e-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="55d9e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55d9e-107">EXAMPLES</span></span>

### <span data-ttu-id="55d9e-108">Beispiel 1: Entfernen eines Eingabedatenstroms aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="55d9e-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="55d9e-109">Dieser Befehl entfernt die Eingabe EventStream aus StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="55d9e-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="55d9e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="55d9e-110">PARAMETERS</span></span>

### <span data-ttu-id="55d9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d9e-111">-DefaultProfile</span></span>
<span data-ttu-id="55d9e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55d9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55d9e-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="55d9e-113">-JobName</span></span>
<span data-ttu-id="55d9e-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="55d9e-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="55d9e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="55d9e-115">-Name</span></span>
<span data-ttu-id="55d9e-116">Gibt den Namen der zu entfernenden Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="55d9e-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="55d9e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55d9e-117">-ResourceGroupName</span></span>
<span data-ttu-id="55d9e-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="55d9e-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="55d9e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55d9e-119">-Confirm</span></span>
<span data-ttu-id="55d9e-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55d9e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55d9e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55d9e-121">-WhatIf</span></span>
<span data-ttu-id="55d9e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55d9e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55d9e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55d9e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55d9e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d9e-124">CommonParameters</span></span>
<span data-ttu-id="55d9e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55d9e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d9e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55d9e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d9e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55d9e-127">INPUTS</span></span>

### <span data-ttu-id="55d9e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="55d9e-128">System.String</span></span>

## <span data-ttu-id="55d9e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55d9e-129">OUTPUTS</span></span>

### <span data-ttu-id="55d9e-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55d9e-130">System.Boolean</span></span>

## <span data-ttu-id="55d9e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="55d9e-131">NOTES</span></span>

## <span data-ttu-id="55d9e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55d9e-132">RELATED LINKS</span></span>

[<span data-ttu-id="55d9e-133">Neu – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="55d9e-133">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="55d9e-134">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="55d9e-134">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="55d9e-135">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="55d9e-135">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


