---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: f801a7c8dd83927e8aceebdc98138aa6ad39d31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503146"
---
# <span data-ttu-id="36dbc-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="36dbc-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="36dbc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="36dbc-103">Löscht eine Eingabe aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="36dbc-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36dbc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36dbc-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36dbc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36dbc-105">DESCRIPTION</span></span>
<span data-ttu-id="36dbc-106">Das Cmdlet **Remove-AzureRmStreamAnalyticsInput** löscht eine Eingabe aus einem Datenstrom Analyse Auftrag in Azure asynchron.</span><span class="sxs-lookup"><span data-stu-id="36dbc-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="36dbc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36dbc-107">EXAMPLES</span></span>

### <span data-ttu-id="36dbc-108">Beispiel 1: Entfernen eines Eingabedatenstroms aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="36dbc-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="36dbc-109">Dieser Befehl entfernt die Eingabe EventStream aus StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="36dbc-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="36dbc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="36dbc-110">PARAMETERS</span></span>

### <span data-ttu-id="36dbc-111">-Jobname</span><span class="sxs-lookup"><span data-stu-id="36dbc-111">-JobName</span></span>
<span data-ttu-id="36dbc-112">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="36dbc-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="36dbc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="36dbc-113">-Name</span></span>
<span data-ttu-id="36dbc-114">Gibt den Namen der zu entfernenden Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="36dbc-114">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="36dbc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36dbc-115">-ResourceGroupName</span></span>
<span data-ttu-id="36dbc-116">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Eingabe gehört.</span><span class="sxs-lookup"><span data-stu-id="36dbc-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="36dbc-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36dbc-117">-Confirm</span></span>
<span data-ttu-id="36dbc-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36dbc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36dbc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36dbc-119">-WhatIf</span></span>
<span data-ttu-id="36dbc-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36dbc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36dbc-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36dbc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36dbc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36dbc-122">-DefaultProfile</span></span>
<span data-ttu-id="36dbc-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36dbc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36dbc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36dbc-124">CommonParameters</span></span>
<span data-ttu-id="36dbc-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36dbc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36dbc-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36dbc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36dbc-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36dbc-127">INPUTS</span></span>

## <span data-ttu-id="36dbc-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36dbc-128">OUTPUTS</span></span>

### <span data-ttu-id="36dbc-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="36dbc-129">System.Object</span></span>

## <span data-ttu-id="36dbc-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="36dbc-130">NOTES</span></span>

## <span data-ttu-id="36dbc-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36dbc-131">RELATED LINKS</span></span>

[<span data-ttu-id="36dbc-132">Neu – AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="36dbc-132">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="36dbc-133">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="36dbc-133">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="36dbc-134">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="36dbc-134">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


