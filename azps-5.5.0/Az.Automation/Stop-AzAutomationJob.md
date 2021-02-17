---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176116"
---
# <span data-ttu-id="78af8-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="78af8-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="78af8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78af8-102">SYNOPSIS</span></span>
<span data-ttu-id="78af8-103">Beendet einen Automatisierungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="78af8-103">Stops an Automation job.</span></span>

## <span data-ttu-id="78af8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78af8-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78af8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78af8-105">DESCRIPTION</span></span>
<span data-ttu-id="78af8-106">Das **Cmdlet "Stop-AzAutomationJob"** beendet einen Azure-Automatisierungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="78af8-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="78af8-107">Geben Sie einen ausgeführten Automatisierungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="78af8-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="78af8-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78af8-108">EXAMPLES</span></span>

### <span data-ttu-id="78af8-109">Beispiel 1: Beenden eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="78af8-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="78af8-110">Dieser Befehl beendet den Auftrag mit der angegebenen ID.</span><span class="sxs-lookup"><span data-stu-id="78af8-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="78af8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78af8-111">PARAMETERS</span></span>

### <span data-ttu-id="78af8-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78af8-112">-AutomationAccountName</span></span>
<span data-ttu-id="78af8-113">Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet einen Auftrag beendet.</span><span class="sxs-lookup"><span data-stu-id="78af8-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="78af8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78af8-114">-DefaultProfile</span></span>
<span data-ttu-id="78af8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="78af8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78af8-116">-ID</span><span class="sxs-lookup"><span data-stu-id="78af8-116">-Id</span></span>
<span data-ttu-id="78af8-117">Gibt die ID eines Auftrags an, der mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="78af8-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="78af8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78af8-118">-ResourceGroupName</span></span>
<span data-ttu-id="78af8-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="78af8-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="78af8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78af8-120">CommonParameters</span></span>
<span data-ttu-id="78af8-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78af8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78af8-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78af8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78af8-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78af8-123">INPUTS</span></span>

### <span data-ttu-id="78af8-124">System.Guid</span><span class="sxs-lookup"><span data-stu-id="78af8-124">System.Guid</span></span>

### <span data-ttu-id="78af8-125">System.String</span><span class="sxs-lookup"><span data-stu-id="78af8-125">System.String</span></span>

## <span data-ttu-id="78af8-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78af8-126">OUTPUTS</span></span>

### <span data-ttu-id="78af8-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="78af8-127">System.Void</span></span>

## <span data-ttu-id="78af8-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="78af8-128">NOTES</span></span>

## <span data-ttu-id="78af8-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="78af8-129">RELATED LINKS</span></span>

[<span data-ttu-id="78af8-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="78af8-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="78af8-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="78af8-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="78af8-132">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="78af8-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="78af8-133">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="78af8-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


