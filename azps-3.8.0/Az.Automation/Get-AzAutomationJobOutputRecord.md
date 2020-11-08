---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: e43cb76db410752aef0a0cffc72d3d5bb6f8e28f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997377"
---
# <span data-ttu-id="fbc85-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="fbc85-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="fbc85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fbc85-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc85-103">Ruft die vollständige Ausgabe eines Automatisierungs Auftrags-Ausgabe Eintrags ab.</span><span class="sxs-lookup"><span data-stu-id="fbc85-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="fbc85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbc85-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbc85-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbc85-105">DESCRIPTION</span></span>
<span data-ttu-id="fbc85-106">Das Cmdlet " **Get-AzAutomationJobOutputRecord** " Ruft die vollständige Ausgabe eines Automatisierungs Auftrags-Ausgabe Eintrags ab.</span><span class="sxs-lookup"><span data-stu-id="fbc85-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="fbc85-107">Obwohl das Cmdlet " **Get-AzAutomationJobOutput** " einen oder mehrere Auftragsausgabe Datensätze aufführt, gibt es nur eine Zusammenfassung als Zeichenfolge des Werts eines beliebigen Ausgabedatensatzes zurück.</span><span class="sxs-lookup"><span data-stu-id="fbc85-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="fbc85-108">Er gibt nicht den vollständigen Wert des ausgegebenen Werts eines Ausgabedatensatzes in seinem ursprünglichen Typ zurück.</span><span class="sxs-lookup"><span data-stu-id="fbc85-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="fbc85-109">Darüber hinaus hat die Zusammenfassung eine maximale Länge, wobei der vollständige Wert, den dieses Cmdlet ausgibt, möglicherweise überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="fbc85-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="fbc85-110">Im Gegensatz zu " **Get-AzAutomationJobOutput** " gibt dieses Cmdlet den vollständigen Wert in seinem ursprünglich ausgegebenen Typ für den ausgegebenen Wert eines Ausgabedatensatzes zurück.</span><span class="sxs-lookup"><span data-stu-id="fbc85-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="fbc85-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbc85-111">EXAMPLES</span></span>

### <span data-ttu-id="fbc85-112">Beispiel 1: Abrufen der vollständigen Ausgabe eines Automatisierungs Auftrags</span><span class="sxs-lookup"><span data-stu-id="fbc85-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="fbc85-113">Dieser Befehl ruft die vollständige Ausgabe des Auftrags ab, die die angegebene Auftrags-ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="fbc85-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="fbc85-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbc85-114">PARAMETERS</span></span>

### <span data-ttu-id="fbc85-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fbc85-115">-AutomationAccountName</span></span>
<span data-ttu-id="fbc85-116">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Auftragsausgabe Daten Satz erhält.</span><span class="sxs-lookup"><span data-stu-id="fbc85-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="fbc85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc85-117">-DefaultProfile</span></span>
<span data-ttu-id="fbc85-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fbc85-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbc85-119">-ID</span><span class="sxs-lookup"><span data-stu-id="fbc85-119">-Id</span></span>
<span data-ttu-id="fbc85-120">Gibt die ID eines Auftragsausgabe Datensatzes an, der für dieses Cmdlet abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbc85-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="fbc85-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="fbc85-121">-JobId</span></span>
<span data-ttu-id="fbc85-122">Gibt die ID eines Auftrags an, für den dieses Cmdlet einen Ausgabe Eintrag erhält.</span><span class="sxs-lookup"><span data-stu-id="fbc85-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="fbc85-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc85-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbc85-124">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Auftragsausgabe Daten Satz erhält.</span><span class="sxs-lookup"><span data-stu-id="fbc85-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="fbc85-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc85-125">CommonParameters</span></span>
<span data-ttu-id="fbc85-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbc85-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc85-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbc85-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc85-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fbc85-128">INPUTS</span></span>

### <span data-ttu-id="fbc85-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fbc85-129">System.Guid</span></span>

### <span data-ttu-id="fbc85-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fbc85-130">System.String</span></span>

## <span data-ttu-id="fbc85-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fbc85-131">OUTPUTS</span></span>

### <span data-ttu-id="fbc85-132">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="fbc85-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="fbc85-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbc85-133">NOTES</span></span>

## <span data-ttu-id="fbc85-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fbc85-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbc85-135">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="fbc85-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


