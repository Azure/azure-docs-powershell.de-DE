---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008172"
---
# <span data-ttu-id="94da6-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="94da6-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="94da6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94da6-102">SYNOPSIS</span></span>
<span data-ttu-id="94da6-103">Ruft die Protokollierungsdaten Ströme eines Automatisierungs-DSC-Kompilierungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="94da6-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="94da6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94da6-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94da6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94da6-105">DESCRIPTION</span></span>
<span data-ttu-id="94da6-106">Das Cmdlet " **Get-AzAutomationDscCompilationJobOutput** " Ruft die Datenstrom Einträge eines APS-Kompilierungs Auftrags (Desired State Configuration, DSC) in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="94da6-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="94da6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94da6-107">EXAMPLES</span></span>

### <span data-ttu-id="94da6-108">Beispiel 1: Abrufen der Protokolle für einen DSC-Kompilierungs Auftrag</span><span class="sxs-lookup"><span data-stu-id="94da6-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="94da6-109">Der erste Befehl ruft die Kompilierungsaufträge im Automatisierungs Konto mit dem Namen Contoso17 mithilfe des Get-AzAutomationDscCompilationJob-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="94da6-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="94da6-110">Der Befehl speichert diese Objekte in der $Jobs-Variablen.</span><span class="sxs-lookup"><span data-stu-id="94da6-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="94da6-111">Der zweite Befehl ruft die Ausgabe des Kompilierungs Auftrags für einen beliebigen Datenstrom für das erste Element des $Jobs-Arrays ab.</span><span class="sxs-lookup"><span data-stu-id="94da6-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="94da6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="94da6-112">PARAMETERS</span></span>

### <span data-ttu-id="94da6-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94da6-113">-AutomationAccountName</span></span>
<span data-ttu-id="94da6-114">Gibt den Namen des Automatisierungs Kontos an, das den DSC-Kompilierungs Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="94da6-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="94da6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94da6-115">-DefaultProfile</span></span>
<span data-ttu-id="94da6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="94da6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94da6-117">-ID</span><span class="sxs-lookup"><span data-stu-id="94da6-117">-Id</span></span>
<span data-ttu-id="94da6-118">Gibt die eindeutige ID des DSC-Kompilierungs Auftrags an, für den dieses Cmdlet Ausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="94da6-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="94da6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94da6-119">-ResourceGroupName</span></span>
<span data-ttu-id="94da6-120">Gibt den Namen der Ressourcengruppe an, die den DSC-Kompilierungs Auftrag enthält, für den dieses Cmdlet Datenstrom Einträge erhält.</span><span class="sxs-lookup"><span data-stu-id="94da6-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="94da6-121">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="94da6-121">-StartTime</span></span>
<span data-ttu-id="94da6-122">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="94da6-122">Specifies a start time.</span></span>
<span data-ttu-id="94da6-123">Dieses Cmdlet ruft Datenstrom Einträge ab, die der DSC-Kompilierungs Auftrag nach dieser Zeit ausgibt.</span><span class="sxs-lookup"><span data-stu-id="94da6-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="94da6-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="94da6-124">-Stream</span></span>
<span data-ttu-id="94da6-125">Gibt den Typ des Datenstroms für die Ausgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="94da6-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="94da6-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="94da6-126">Valid values are:</span></span> 
- <span data-ttu-id="94da6-127">Alle</span><span class="sxs-lookup"><span data-stu-id="94da6-127">Any</span></span> 
- <span data-ttu-id="94da6-128">Warnung</span><span class="sxs-lookup"><span data-stu-id="94da6-128">Warning</span></span> 
- <span data-ttu-id="94da6-129">Fehler</span><span class="sxs-lookup"><span data-stu-id="94da6-129">Error</span></span> 
- <span data-ttu-id="94da6-130">Ausführliche</span><span class="sxs-lookup"><span data-stu-id="94da6-130">Verbose</span></span>

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

### <span data-ttu-id="94da6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94da6-131">CommonParameters</span></span>
<span data-ttu-id="94da6-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94da6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94da6-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94da6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94da6-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94da6-134">INPUTS</span></span>

### <span data-ttu-id="94da6-135">System. GUID</span><span class="sxs-lookup"><span data-stu-id="94da6-135">System.Guid</span></span>

### <span data-ttu-id="94da6-136">Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="94da6-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="94da6-137">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="94da6-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="94da6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="94da6-138">System.String</span></span>

## <span data-ttu-id="94da6-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94da6-139">OUTPUTS</span></span>

### <span data-ttu-id="94da6-140">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="94da6-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="94da6-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="94da6-141">NOTES</span></span>

## <span data-ttu-id="94da6-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94da6-142">RELATED LINKS</span></span>

[<span data-ttu-id="94da6-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="94da6-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="94da6-144">Anfang-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="94da6-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


