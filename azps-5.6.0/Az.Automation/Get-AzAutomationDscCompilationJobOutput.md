---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 1da8d90ca336d2886f7633e646583bc61529fcee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939736"
---
# <span data-ttu-id="bd7bd-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="bd7bd-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="bd7bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd7bd-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7bd-103">Ruft die Protokollierungsströme eines Automatisierungs-DSC-Kompilierungsauftrags ab.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="bd7bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd7bd-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd7bd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd7bd-105">DESCRIPTION</span></span>
<span data-ttu-id="bd7bd-106">Das **Get-AzAutomationDscCompilationJobOutput-Cmdlet** ruft die Datenstromdatensätze eines APS Desired State Configuration (DSC)-Kompilierungsauftrags in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="bd7bd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd7bd-107">EXAMPLES</span></span>

### <span data-ttu-id="bd7bd-108">Beispiel 1: Erfassen der Protokolle für einen DSC-Kompilierungsauftrag</span><span class="sxs-lookup"><span data-stu-id="bd7bd-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="bd7bd-109">Der erste Befehl ruft die Kompilierungsaufträge im Automatisierungskonto namens Contoso17 mithilfe des cmdlets Get-AzAutomationDscCompilationJob ab.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="bd7bd-110">Der Befehl speichert diese Objekte in der $Jobs-Variable.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="bd7bd-111">Der zweite Befehl ruft die Ausgabe des Kompilierungsauftrags für einen beliebigen Datenstrom für das erste Element des $Jobs ab.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="bd7bd-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bd7bd-112">PARAMETERS</span></span>

### <span data-ttu-id="bd7bd-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bd7bd-113">-AutomationAccountName</span></span>
<span data-ttu-id="bd7bd-114">Gibt den Namen des Automatisierungskontos an, das den DSC-Kompilierungsauftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="bd7bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7bd-115">-DefaultProfile</span></span>
<span data-ttu-id="bd7bd-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bd7bd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd7bd-117">-ID</span><span class="sxs-lookup"><span data-stu-id="bd7bd-117">-Id</span></span>
<span data-ttu-id="bd7bd-118">Gibt die eindeutige ID des DSC-Kompilierungsauftrags an, für den dieses Cmdlet die Ausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="bd7bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="bd7bd-120">Gibt den Namen der Ressourcengruppe an, die den DSC-Kompilierungsauftrag enthält, für den dieses Cmdlet Datenstromeinträge erhält.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="bd7bd-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bd7bd-121">-StartTime</span></span>
<span data-ttu-id="bd7bd-122">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-122">Specifies a start time.</span></span>
<span data-ttu-id="bd7bd-123">Dieses Cmdlet ruft Datenstromdatensätze ab, die nach diesem Zeitpunkt vom AUFTRAG für die DSC-Kompilierung ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="bd7bd-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="bd7bd-124">-Stream</span></span>
<span data-ttu-id="bd7bd-125">Gibt den Typ des Datenstroms für die Ausgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="bd7bd-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="bd7bd-126">Valid values are:</span></span> 
- <span data-ttu-id="bd7bd-127">Any</span><span class="sxs-lookup"><span data-stu-id="bd7bd-127">Any</span></span> 
- <span data-ttu-id="bd7bd-128">Warnung</span><span class="sxs-lookup"><span data-stu-id="bd7bd-128">Warning</span></span> 
- <span data-ttu-id="bd7bd-129">Fehler</span><span class="sxs-lookup"><span data-stu-id="bd7bd-129">Error</span></span> 
- <span data-ttu-id="bd7bd-130">Verbose</span><span class="sxs-lookup"><span data-stu-id="bd7bd-130">Verbose</span></span>

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

### <span data-ttu-id="bd7bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7bd-131">CommonParameters</span></span>
<span data-ttu-id="bd7bd-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd7bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7bd-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd7bd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7bd-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd7bd-134">INPUTS</span></span>

### <span data-ttu-id="bd7bd-135">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bd7bd-135">System.Guid</span></span>

### <span data-ttu-id="bd7bd-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="bd7bd-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="bd7bd-137">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bd7bd-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bd7bd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bd7bd-138">System.String</span></span>

## <span data-ttu-id="bd7bd-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd7bd-139">OUTPUTS</span></span>

### <span data-ttu-id="bd7bd-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="bd7bd-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="bd7bd-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bd7bd-141">NOTES</span></span>

## <span data-ttu-id="bd7bd-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bd7bd-142">RELATED LINKS</span></span>

[<span data-ttu-id="bd7bd-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="bd7bd-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="bd7bd-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="bd7bd-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


