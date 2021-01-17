---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 731a2df87ce6ad575e9aa3e10eb124e52ec1b60b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373175"
---
# <span data-ttu-id="1e867-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1e867-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="1e867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e867-102">SYNOPSIS</span></span>
<span data-ttu-id="1e867-103">Setzt einen angehaltenen Automatisierungsauftrag fort.</span><span class="sxs-lookup"><span data-stu-id="1e867-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="1e867-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e867-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e867-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e867-105">DESCRIPTION</span></span>
<span data-ttu-id="1e867-106">Das **Cmdlet "Resume-AzAutomationJob"** setzt einen angehaltenen Azure -Automatisierungsauftrag fort.</span><span class="sxs-lookup"><span data-stu-id="1e867-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="1e867-107">Geben Sie den angehaltenen Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="1e867-107">Specify the suspended job.</span></span>
<span data-ttu-id="1e867-108">Zum Anhalten eines Auftrags verwenden Sie das Suspend-AzAutomationJob Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e867-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="1e867-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e867-109">EXAMPLES</span></span>

### <span data-ttu-id="1e867-110">Beispiel 1: Fortsetzen eines angehaltenen Auftrags</span><span class="sxs-lookup"><span data-stu-id="1e867-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1e867-111">Mit diesem Befehl wird der Auftrag mit der angegebenen ID fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1e867-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="1e867-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e867-112">PARAMETERS</span></span>

### <span data-ttu-id="1e867-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1e867-113">-AutomationAccountName</span></span>
<span data-ttu-id="1e867-114">Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet einen Auftrag fortsetzen soll.</span><span class="sxs-lookup"><span data-stu-id="1e867-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="1e867-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e867-115">-DefaultProfile</span></span>
<span data-ttu-id="1e867-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1e867-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e867-117">-ID</span><span class="sxs-lookup"><span data-stu-id="1e867-117">-Id</span></span>
<span data-ttu-id="1e867-118">Gibt die ID eines Auftrags an, den dieses Cmdlet fortsetzen soll.</span><span class="sxs-lookup"><span data-stu-id="1e867-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="1e867-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e867-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e867-120">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Auftrag fort setzt.</span><span class="sxs-lookup"><span data-stu-id="1e867-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="1e867-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e867-121">CommonParameters</span></span>
<span data-ttu-id="1e867-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e867-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e867-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e867-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e867-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e867-124">INPUTS</span></span>

### <span data-ttu-id="1e867-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1e867-125">System.Guid</span></span>

### <span data-ttu-id="1e867-126">System.String</span><span class="sxs-lookup"><span data-stu-id="1e867-126">System.String</span></span>

## <span data-ttu-id="1e867-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e867-127">OUTPUTS</span></span>

### <span data-ttu-id="1e867-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="1e867-128">System.Void</span></span>

## <span data-ttu-id="1e867-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1e867-129">NOTES</span></span>

## <span data-ttu-id="1e867-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1e867-130">RELATED LINKS</span></span>

[<span data-ttu-id="1e867-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1e867-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="1e867-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1e867-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="1e867-133">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1e867-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="1e867-134">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1e867-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


