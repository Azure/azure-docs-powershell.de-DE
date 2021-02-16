---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168436"
---
# <span data-ttu-id="31103-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="31103-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="31103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31103-102">SYNOPSIS</span></span>
<span data-ttu-id="31103-103">Ruft die Protokolldatenströme eines Automatisierungs-DSC-Kompilierungsauftrags ab.</span><span class="sxs-lookup"><span data-stu-id="31103-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="31103-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31103-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31103-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31103-105">DESCRIPTION</span></span>
<span data-ttu-id="31103-106">Das **Cmdlet "Get-AzAutomationDscCompilationJobOutput"** ruft die Datenstromeinträge eines Kompilierungsauftrags (Desired State Configuration, DSC) für APS in der Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="31103-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="31103-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="31103-107">EXAMPLES</span></span>

### <span data-ttu-id="31103-108">Beispiel 1: Erhalten der Protokolle für einen Auftrag zur DSC-Kompilierung</span><span class="sxs-lookup"><span data-stu-id="31103-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="31103-109">Der erste Befehl ruft die Kompilierungsaufträge im Automatisierungskonto namens "Contoso17" mithilfe des cmdlets Get-AzAutomationDscCompilationJob ab.</span><span class="sxs-lookup"><span data-stu-id="31103-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="31103-110">Der Befehl speichert diese Objekte in der $Jobs Variable.</span><span class="sxs-lookup"><span data-stu-id="31103-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="31103-111">Der zweite Befehl ruft die Ausgabe des Kompilierungsauftrags für jeden Datenstrom für das erste Element des $Jobs ab.</span><span class="sxs-lookup"><span data-stu-id="31103-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="31103-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31103-112">PARAMETERS</span></span>

### <span data-ttu-id="31103-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="31103-113">-AutomationAccountName</span></span>
<span data-ttu-id="31103-114">Gibt den Namen des Automatisierungskontos an, das den DSC-Kompilierungsauftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="31103-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="31103-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31103-115">-DefaultProfile</span></span>
<span data-ttu-id="31103-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="31103-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31103-117">-ID</span><span class="sxs-lookup"><span data-stu-id="31103-117">-Id</span></span>
<span data-ttu-id="31103-118">Gibt die eindeutige ID des DSC-Kompilierungsauftrags an, für den dieses Cmdlet die Ausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="31103-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="31103-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31103-119">-ResourceGroupName</span></span>
<span data-ttu-id="31103-120">Gibt den Namen der Ressourcengruppe an, die den DSC-Kompilierungsauftrag enthält, für den dieses Cmdlet Datenstromdatensätze erhält.</span><span class="sxs-lookup"><span data-stu-id="31103-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="31103-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="31103-121">-StartTime</span></span>
<span data-ttu-id="31103-122">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="31103-122">Specifies a start time.</span></span>
<span data-ttu-id="31103-123">Dieses Cmdlet ruft Streamdatensätze ab, die nach diesem Zeitpunkt vom Auftrag für die DSC-Kompilierung ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="31103-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="31103-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="31103-124">-Stream</span></span>
<span data-ttu-id="31103-125">Gibt den Typ des Datenstroms für die Ausgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="31103-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="31103-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="31103-126">Valid values are:</span></span> 
- <span data-ttu-id="31103-127">Any</span><span class="sxs-lookup"><span data-stu-id="31103-127">Any</span></span> 
- <span data-ttu-id="31103-128">Warnung</span><span class="sxs-lookup"><span data-stu-id="31103-128">Warning</span></span> 
- <span data-ttu-id="31103-129">Fehler</span><span class="sxs-lookup"><span data-stu-id="31103-129">Error</span></span> 
- <span data-ttu-id="31103-130">Verbose</span><span class="sxs-lookup"><span data-stu-id="31103-130">Verbose</span></span>

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

### <span data-ttu-id="31103-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31103-131">CommonParameters</span></span>
<span data-ttu-id="31103-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31103-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31103-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31103-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31103-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="31103-134">INPUTS</span></span>

### <span data-ttu-id="31103-135">System.Guid</span><span class="sxs-lookup"><span data-stu-id="31103-135">System.Guid</span></span>

### <span data-ttu-id="31103-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="31103-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="31103-137">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="31103-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="31103-138">System.String</span><span class="sxs-lookup"><span data-stu-id="31103-138">System.String</span></span>

## <span data-ttu-id="31103-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="31103-139">OUTPUTS</span></span>

### <span data-ttu-id="31103-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="31103-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="31103-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="31103-141">NOTES</span></span>

## <span data-ttu-id="31103-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="31103-142">RELATED LINKS</span></span>

[<span data-ttu-id="31103-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="31103-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="31103-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="31103-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


