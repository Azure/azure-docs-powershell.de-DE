---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471222"
---
# <span data-ttu-id="edace-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="edace-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="edace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edace-102">SYNOPSIS</span></span>
<span data-ttu-id="edace-103">Ein Automatisierungsauftrag wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="edace-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="edace-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edace-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edace-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edace-105">DESCRIPTION</span></span>
<span data-ttu-id="edace-106">Das **Cmdlet "Suspend-AzAutomationJob"** setzt einen Azure-Automatisierungsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="edace-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="edace-107">Geben Sie einen ausgeführten Automatisierungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="edace-107">Specify a running Automation job.</span></span>
<span data-ttu-id="edace-108">Wenn Sie einen angehaltenen Auftrag fortsetzen möchten, verwenden Sie das cmdlet Resume-AzAutomationJob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edace-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="edace-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="edace-109">EXAMPLES</span></span>

### <span data-ttu-id="edace-110">Beispiel 1: Aussetzen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="edace-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="edace-111">Mit diesem Befehl wird der Auftrag angehalten, der die angegebene ID hat.</span><span class="sxs-lookup"><span data-stu-id="edace-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="edace-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edace-112">PARAMETERS</span></span>

### <span data-ttu-id="edace-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="edace-113">-AutomationAccountName</span></span>
<span data-ttu-id="edace-114">Gibt den Namen eines Automatisierungskontos an, bei dem dieses Cmdlet einen Auftrag aussetzen soll.</span><span class="sxs-lookup"><span data-stu-id="edace-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="edace-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edace-115">-DefaultProfile</span></span>
<span data-ttu-id="edace-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="edace-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edace-117">-ID</span><span class="sxs-lookup"><span data-stu-id="edace-117">-Id</span></span>
<span data-ttu-id="edace-118">Gibt die ID eines Auftrags an, der von diesem Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="edace-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="edace-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edace-119">-ResourceGroupName</span></span>
<span data-ttu-id="edace-120">Gibt die ID eines Auftrags an, der von diesem Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="edace-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="edace-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edace-121">CommonParameters</span></span>
<span data-ttu-id="edace-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edace-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edace-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edace-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edace-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="edace-124">INPUTS</span></span>

### <span data-ttu-id="edace-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="edace-125">System.Guid</span></span>

### <span data-ttu-id="edace-126">System.String</span><span class="sxs-lookup"><span data-stu-id="edace-126">System.String</span></span>

## <span data-ttu-id="edace-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="edace-127">OUTPUTS</span></span>

### <span data-ttu-id="edace-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="edace-128">System.Void</span></span>

## <span data-ttu-id="edace-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="edace-129">NOTES</span></span>

## <span data-ttu-id="edace-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="edace-130">RELATED LINKS</span></span>

[<span data-ttu-id="edace-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="edace-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="edace-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="edace-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="edace-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="edace-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="edace-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="edace-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


