---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: d38971c15c46cbeaba6e9dda87ad0f3b7febbfd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500954"
---
# <span data-ttu-id="e044b-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e044b-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="e044b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e044b-102">SYNOPSIS</span></span>
<span data-ttu-id="e044b-103">Ruft die Protokollierungsdaten Ströme eines Automatisierungs-DSC-Kompilierungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="e044b-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e044b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e044b-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e044b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e044b-105">DESCRIPTION</span></span>
<span data-ttu-id="e044b-106">Das Cmdlet " **Get-AzureRmAutomationDscCompilationJobOutput** " Ruft die Datenstrom Einträge eines APS-Kompilierungs Auftrags (Desired State Configuration, DSC) in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="e044b-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="e044b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e044b-107">EXAMPLES</span></span>

### <span data-ttu-id="e044b-108">Beispiel 1: Abrufen der Protokolle für einen DSC-Kompilierungs Auftrag</span><span class="sxs-lookup"><span data-stu-id="e044b-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="e044b-109">Der erste Befehl ruft die Kompilierungsaufträge im Automatisierungs Konto mit dem Namen Contoso17 mithilfe des Get-AzureRmAutomationDscCompilationJob-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="e044b-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="e044b-110">Der Befehl speichert diese Objekte in der $Jobs-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e044b-110">The command stores those objects in the $Jobs variable.</span></span>

<span data-ttu-id="e044b-111">Der zweite Befehl ruft die Ausgabe des Kompilierungs Auftrags für einen beliebigen Datenstrom für das erste Element des $Jobs-Arrays ab.</span><span class="sxs-lookup"><span data-stu-id="e044b-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="e044b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e044b-112">PARAMETERS</span></span>

### <span data-ttu-id="e044b-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e044b-113">-AutomationAccountName</span></span>
<span data-ttu-id="e044b-114">Gibt den Namen des Automatisierungs Kontos an, das den DSC-Kompilierungs Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="e044b-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="e044b-115">-ID</span><span class="sxs-lookup"><span data-stu-id="e044b-115">-Id</span></span>
<span data-ttu-id="e044b-116">Gibt die eindeutige ID des DSC-Kompilierungs Auftrags an, für den dieses Cmdlet Ausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="e044b-116">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e044b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e044b-117">-ResourceGroupName</span></span>
<span data-ttu-id="e044b-118">Gibt den Namen der Ressourcengruppe an, die den DSC-Kompilierungs Auftrag enthält, für den dieses Cmdlet Datenstrom Einträge erhält.</span><span class="sxs-lookup"><span data-stu-id="e044b-118">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="e044b-119">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="e044b-119">-StartTime</span></span>
<span data-ttu-id="e044b-120">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="e044b-120">Specifies a start time.</span></span>
<span data-ttu-id="e044b-121">Dieses Cmdlet ruft Datenstrom Einträge ab, die der DSC-Kompilierungs Auftrag nach dieser Zeit ausgibt.</span><span class="sxs-lookup"><span data-stu-id="e044b-121">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e044b-122">-Stream</span><span class="sxs-lookup"><span data-stu-id="e044b-122">-Stream</span></span>
<span data-ttu-id="e044b-123">Gibt den Typ des Datenstroms für die Ausgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e044b-123">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="e044b-124">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="e044b-124">Valid values are:</span></span> 

- <span data-ttu-id="e044b-125">Alle</span><span class="sxs-lookup"><span data-stu-id="e044b-125">Any</span></span> 
- <span data-ttu-id="e044b-126">Warnung</span><span class="sxs-lookup"><span data-stu-id="e044b-126">Warning</span></span> 
- <span data-ttu-id="e044b-127">Fehler</span><span class="sxs-lookup"><span data-stu-id="e044b-127">Error</span></span> 
- <span data-ttu-id="e044b-128">Ausführliche</span><span class="sxs-lookup"><span data-stu-id="e044b-128">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e044b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e044b-129">-DefaultProfile</span></span>
<span data-ttu-id="e044b-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e044b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e044b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e044b-131">CommonParameters</span></span>
<span data-ttu-id="e044b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e044b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e044b-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e044b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e044b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e044b-134">INPUTS</span></span>

## <span data-ttu-id="e044b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e044b-135">OUTPUTS</span></span>

### <span data-ttu-id="e044b-136">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="e044b-136">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="e044b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e044b-137">NOTES</span></span>

## <span data-ttu-id="e044b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e044b-138">RELATED LINKS</span></span>

[<span data-ttu-id="e044b-139">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e044b-139">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="e044b-140">Anfang-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e044b-140">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


