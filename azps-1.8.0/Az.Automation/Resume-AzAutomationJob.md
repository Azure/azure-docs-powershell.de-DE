---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 6315ba9079729779a7db872a87237e1b664837c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661719"
---
# <span data-ttu-id="ff200-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ff200-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="ff200-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff200-102">SYNOPSIS</span></span>
<span data-ttu-id="ff200-103">Setzt einen angehalten Automatisierungs Auftrag fort.</span><span class="sxs-lookup"><span data-stu-id="ff200-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="ff200-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff200-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff200-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff200-105">DESCRIPTION</span></span>
<span data-ttu-id="ff200-106">Das Cmdlet **Resume-AzAutomationJob** setzt einen angehenden Azure-Automatisierungs Auftrag fort.</span><span class="sxs-lookup"><span data-stu-id="ff200-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="ff200-107">Geben Sie den angehenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="ff200-107">Specify the suspended job.</span></span>
<span data-ttu-id="ff200-108">Verwenden Sie das Suspend-AzAutomationJob-Cmdlet, um einen Auftrag zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="ff200-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="ff200-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff200-109">EXAMPLES</span></span>

### <span data-ttu-id="ff200-110">Beispiel 1: Fortsetzen eines angehenden Auftrags</span><span class="sxs-lookup"><span data-stu-id="ff200-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ff200-111">Mit diesem Befehl wird der Auftrag mit der angegebenen ID fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="ff200-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="ff200-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff200-112">PARAMETERS</span></span>

### <span data-ttu-id="ff200-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ff200-113">-AutomationAccountName</span></span>
<span data-ttu-id="ff200-114">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen Auftrag fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="ff200-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="ff200-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff200-115">-DefaultProfile</span></span>
<span data-ttu-id="ff200-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ff200-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff200-117">-ID</span><span class="sxs-lookup"><span data-stu-id="ff200-117">-Id</span></span>
<span data-ttu-id="ff200-118">Gibt die ID eines Auftrags an, den dieses Cmdlet fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="ff200-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="ff200-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff200-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff200-120">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Auftrag fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="ff200-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="ff200-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff200-121">CommonParameters</span></span>
<span data-ttu-id="ff200-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff200-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff200-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff200-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff200-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff200-124">INPUTS</span></span>

### <span data-ttu-id="ff200-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ff200-125">System.Guid</span></span>

### <span data-ttu-id="ff200-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ff200-126">System.String</span></span>

## <span data-ttu-id="ff200-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff200-127">OUTPUTS</span></span>

### <span data-ttu-id="ff200-128">System. void</span><span class="sxs-lookup"><span data-stu-id="ff200-128">System.Void</span></span>

## <span data-ttu-id="ff200-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff200-129">NOTES</span></span>

## <span data-ttu-id="ff200-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff200-130">RELATED LINKS</span></span>

[<span data-ttu-id="ff200-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ff200-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="ff200-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="ff200-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="ff200-133">Stopp-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ff200-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="ff200-134">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ff200-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


