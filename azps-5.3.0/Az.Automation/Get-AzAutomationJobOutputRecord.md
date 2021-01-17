---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471356"
---
# <span data-ttu-id="a7e5d-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="a7e5d-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="a7e5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e5d-103">Ruft die vollständige Ausgabe eines Ausgabedatensatzs für einen Automatisierungsauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="a7e5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7e5d-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7e5d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7e5d-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e5d-106">Das **Cmdlet "Get-AzAutomationJobOutputRecord"** ruft die vollständige Ausgabe eines Ausgabedatensatz für einen Automatisierungsauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="a7e5d-107">Obwohl das **Cmdlet "Get-AzAutomationJobOutput"** einen oder mehrere Auftragsausgabedatensätze auflistet, gibt es nur eine Zusammenfassung als Zeichenfolge des Werts eines ausgabedatensatz zurück.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="a7e5d-108">Es gibt nicht den vollständigen Wert des ausgegebenen Werts eines Ausgabedatensatzs im ursprünglichen Typ zurück.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="a7e5d-109">Darüber hinaus hat die Zusammenfassung eine maximale Länge, die den vollständigen Wert, den dieses Cmdlet ausausgabe, möglicherweise überschreitet.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="a7e5d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7e5d-110">EXAMPLES</span></span>

### <span data-ttu-id="a7e5d-111">Beispiel 1: Vollständige Ausgabe eines Automatisierungsauftrags</span><span class="sxs-lookup"><span data-stu-id="a7e5d-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="a7e5d-112">Dieser Befehl ruft die vollständige Ausgabe des Auftrags ab, der die angegebene Auftrags-ID hat.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="a7e5d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7e5d-113">PARAMETERS</span></span>

### <span data-ttu-id="a7e5d-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a7e5d-114">-AutomationAccountName</span></span>
<span data-ttu-id="a7e5d-115">Gibt den Namen eines Automatisierungskontos an, für das dieses Cmdlet einen Auftragsausgabedatensatz erhält.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="a7e5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e5d-116">-DefaultProfile</span></span>
<span data-ttu-id="a7e5d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a7e5d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7e5d-118">-ID</span><span class="sxs-lookup"><span data-stu-id="a7e5d-118">-Id</span></span>
<span data-ttu-id="a7e5d-119">Gibt die ID eines Auftragsausgabedatenblatts an, das von diesem Cmdlet abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e5d-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="a7e5d-120">-JobId</span></span>
<span data-ttu-id="a7e5d-121">Gibt die ID eines Auftrags an, für den dieses Cmdlet einen Ausgabedatensatz erhält.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e5d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e5d-122">-ResourceGroupName</span></span>
<span data-ttu-id="a7e5d-123">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Auftragsausgabedatensatz erhält.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="a7e5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e5d-124">CommonParameters</span></span>
<span data-ttu-id="a7e5d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e5d-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e5d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e5d-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7e5d-127">INPUTS</span></span>

### <span data-ttu-id="a7e5d-128">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a7e5d-128">System.Guid</span></span>

### <span data-ttu-id="a7e5d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a7e5d-129">System.String</span></span>

## <span data-ttu-id="a7e5d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7e5d-130">OUTPUTS</span></span>

### <span data-ttu-id="a7e5d-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="a7e5d-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="a7e5d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a7e5d-132">NOTES</span></span>

## <span data-ttu-id="a7e5d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a7e5d-133">RELATED LINKS</span></span>

[<span data-ttu-id="a7e5d-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a7e5d-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


