---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008164"
---
# <span data-ttu-id="c9d80-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="c9d80-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="c9d80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9d80-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d80-103">Ruft die vollständige Ausgabe eines Automatisierungs Auftrags-Ausgabe Eintrags ab.</span><span class="sxs-lookup"><span data-stu-id="c9d80-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="c9d80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9d80-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d80-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9d80-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d80-106">Das Cmdlet " **Get-AzAutomationJobOutputRecord** " Ruft die vollständige Ausgabe eines Automatisierungs Auftrags-Ausgabe Eintrags ab.</span><span class="sxs-lookup"><span data-stu-id="c9d80-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="c9d80-107">Obwohl das Cmdlet " **Get-AzAutomationJobOutput** " einen oder mehrere Auftragsausgabe Datensätze aufführt, gibt es nur eine Zusammenfassung als Zeichenfolge des Werts eines beliebigen Ausgabedatensatzes zurück.</span><span class="sxs-lookup"><span data-stu-id="c9d80-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="c9d80-108">Er gibt nicht den vollständigen Wert des ausgegebenen Werts eines Ausgabedatensatzes in seinem ursprünglichen Typ zurück.</span><span class="sxs-lookup"><span data-stu-id="c9d80-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="c9d80-109">Darüber hinaus hat die Zusammenfassung eine maximale Länge, wobei der vollständige Wert, den dieses Cmdlet ausgibt, möglicherweise überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="c9d80-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="c9d80-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9d80-110">EXAMPLES</span></span>

### <span data-ttu-id="c9d80-111">Beispiel 1: Abrufen der vollständigen Ausgabe eines Automatisierungs Auftrags</span><span class="sxs-lookup"><span data-stu-id="c9d80-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="c9d80-112">Dieser Befehl ruft die vollständige Ausgabe des Auftrags ab, die die angegebene Auftrags-ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="c9d80-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="c9d80-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9d80-113">PARAMETERS</span></span>

### <span data-ttu-id="c9d80-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c9d80-114">-AutomationAccountName</span></span>
<span data-ttu-id="c9d80-115">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Auftragsausgabe Daten Satz erhält.</span><span class="sxs-lookup"><span data-stu-id="c9d80-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="c9d80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d80-116">-DefaultProfile</span></span>
<span data-ttu-id="c9d80-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c9d80-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9d80-118">-ID</span><span class="sxs-lookup"><span data-stu-id="c9d80-118">-Id</span></span>
<span data-ttu-id="c9d80-119">Gibt die ID eines Auftragsausgabe Datensatzes an, der für dieses Cmdlet abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9d80-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="c9d80-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="c9d80-120">-JobId</span></span>
<span data-ttu-id="c9d80-121">Gibt die ID eines Auftrags an, für den dieses Cmdlet einen Ausgabe Eintrag erhält.</span><span class="sxs-lookup"><span data-stu-id="c9d80-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="c9d80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d80-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9d80-123">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Auftragsausgabe Daten Satz erhält.</span><span class="sxs-lookup"><span data-stu-id="c9d80-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="c9d80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d80-124">CommonParameters</span></span>
<span data-ttu-id="c9d80-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d80-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d80-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d80-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9d80-127">INPUTS</span></span>

### <span data-ttu-id="c9d80-128">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c9d80-128">System.Guid</span></span>

### <span data-ttu-id="c9d80-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c9d80-129">System.String</span></span>

## <span data-ttu-id="c9d80-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9d80-130">OUTPUTS</span></span>

### <span data-ttu-id="c9d80-131">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="c9d80-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="c9d80-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9d80-132">NOTES</span></span>

## <span data-ttu-id="c9d80-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9d80-133">RELATED LINKS</span></span>

[<span data-ttu-id="c9d80-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c9d80-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


