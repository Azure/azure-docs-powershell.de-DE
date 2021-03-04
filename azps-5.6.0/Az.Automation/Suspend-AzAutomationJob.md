---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 035cd77ab389b9c3cdce686620b3157b4b046c41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933251"
---
# <span data-ttu-id="d53ea-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d53ea-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="d53ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d53ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d53ea-103">Setzt einen Automatisierungsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="d53ea-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="d53ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d53ea-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d53ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d53ea-105">DESCRIPTION</span></span>
<span data-ttu-id="d53ea-106">Das **Cmdlet Suspend-AzAutomationJob** setzt einen Azure-Automatisierungsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="d53ea-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="d53ea-107">Geben Sie einen ausgeführten Automatisierungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="d53ea-107">Specify a running Automation job.</span></span>
<span data-ttu-id="d53ea-108">Zum Fortsetzen eines angehaltenen Auftrags verwenden Sie das cmdlet Resume-AzAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="d53ea-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="d53ea-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d53ea-109">EXAMPLES</span></span>

### <span data-ttu-id="d53ea-110">Beispiel 1: Anhalten eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="d53ea-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d53ea-111">Mit diesem Befehl wird der Auftrag angehalten, der die angegebene ID hat.</span><span class="sxs-lookup"><span data-stu-id="d53ea-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="d53ea-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d53ea-112">PARAMETERS</span></span>

### <span data-ttu-id="d53ea-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d53ea-113">-AutomationAccountName</span></span>
<span data-ttu-id="d53ea-114">Gibt den Namen eines Automatisierungskontos an, bei dem dieses Cmdlet einen Auftrag anhängt.</span><span class="sxs-lookup"><span data-stu-id="d53ea-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="d53ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53ea-115">-DefaultProfile</span></span>
<span data-ttu-id="d53ea-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d53ea-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d53ea-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d53ea-117">-Id</span></span>
<span data-ttu-id="d53ea-118">Gibt die ID eines Auftrags an, der von diesem Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d53ea-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="d53ea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d53ea-119">-ResourceGroupName</span></span>
<span data-ttu-id="d53ea-120">Gibt die ID eines Auftrags an, der von diesem Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d53ea-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="d53ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53ea-121">CommonParameters</span></span>
<span data-ttu-id="d53ea-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d53ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53ea-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d53ea-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53ea-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d53ea-124">INPUTS</span></span>

### <span data-ttu-id="d53ea-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d53ea-125">System.Guid</span></span>

### <span data-ttu-id="d53ea-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d53ea-126">System.String</span></span>

## <span data-ttu-id="d53ea-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d53ea-127">OUTPUTS</span></span>

### <span data-ttu-id="d53ea-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="d53ea-128">System.Void</span></span>

## <span data-ttu-id="d53ea-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d53ea-129">NOTES</span></span>

## <span data-ttu-id="d53ea-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d53ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="d53ea-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d53ea-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="d53ea-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d53ea-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="d53ea-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d53ea-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="d53ea-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d53ea-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


