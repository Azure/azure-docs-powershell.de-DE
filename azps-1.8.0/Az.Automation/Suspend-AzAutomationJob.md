---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 850ff932bdae35bd21ab83c745b5da8c056d778d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661689"
---
# <span data-ttu-id="00f83-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="00f83-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="00f83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00f83-102">SYNOPSIS</span></span>
<span data-ttu-id="00f83-103">Unterbricht einen Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="00f83-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="00f83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00f83-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00f83-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00f83-105">DESCRIPTION</span></span>
<span data-ttu-id="00f83-106">Mit dem Cmdlet **Suspend-AzAutomationJob** wird ein Azure-Automatisierungs Auftrag angehalten.</span><span class="sxs-lookup"><span data-stu-id="00f83-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="00f83-107">Geben Sie einen ausgeführten Automatisierungs Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="00f83-107">Specify a running Automation job.</span></span>
<span data-ttu-id="00f83-108">Verwenden Sie das Resume-AzAutomationJob-Cmdlet, um einen angehalten Job fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="00f83-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="00f83-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00f83-109">EXAMPLES</span></span>

### <span data-ttu-id="00f83-110">Beispiel 1: Anhalten eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="00f83-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="00f83-111">Mit diesem Befehl wird der Auftrag mit der angegebenen ID angehalten.</span><span class="sxs-lookup"><span data-stu-id="00f83-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="00f83-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="00f83-112">PARAMETERS</span></span>

### <span data-ttu-id="00f83-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00f83-113">-AutomationAccountName</span></span>
<span data-ttu-id="00f83-114">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen Auftrag unterbricht.</span><span class="sxs-lookup"><span data-stu-id="00f83-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="00f83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f83-115">-DefaultProfile</span></span>
<span data-ttu-id="00f83-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="00f83-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00f83-117">-ID</span><span class="sxs-lookup"><span data-stu-id="00f83-117">-Id</span></span>
<span data-ttu-id="00f83-118">Gibt die ID eines Auftrags an, der vom Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="00f83-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="00f83-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f83-119">-ResourceGroupName</span></span>
<span data-ttu-id="00f83-120">Gibt die ID eines Auftrags an, der vom Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="00f83-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="00f83-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f83-121">CommonParameters</span></span>
<span data-ttu-id="00f83-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f83-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f83-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f83-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f83-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00f83-124">INPUTS</span></span>

### <span data-ttu-id="00f83-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="00f83-125">System.Guid</span></span>

### <span data-ttu-id="00f83-126">System. String</span><span class="sxs-lookup"><span data-stu-id="00f83-126">System.String</span></span>

## <span data-ttu-id="00f83-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00f83-127">OUTPUTS</span></span>

### <span data-ttu-id="00f83-128">System. void</span><span class="sxs-lookup"><span data-stu-id="00f83-128">System.Void</span></span>

## <span data-ttu-id="00f83-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="00f83-129">NOTES</span></span>

## <span data-ttu-id="00f83-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00f83-130">RELATED LINKS</span></span>

[<span data-ttu-id="00f83-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="00f83-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="00f83-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="00f83-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="00f83-133">Lebenslauf-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="00f83-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="00f83-134">Stopp-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="00f83-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


