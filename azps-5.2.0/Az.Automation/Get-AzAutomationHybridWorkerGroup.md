---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373860"
---
# <span data-ttu-id="4aa2e-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="4aa2e-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="4aa2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aa2e-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa2e-103">Ruft hybride Runbook-Workergruppen ab.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="4aa2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aa2e-104">SYNTAX</span></span>

### <span data-ttu-id="4aa2e-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="4aa2e-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa2e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4aa2e-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aa2e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aa2e-107">DESCRIPTION</span></span>
<span data-ttu-id="4aa2e-108">Das **Cmdlet "Get-AzAutomationHybridWorkerGroup"** ruft runbook-Hybrid-Workergruppen für die Azure-Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="4aa2e-109">Um eine bestimmte Gruppe zu erhalten, geben Sie deren Namen an.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="4aa2e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4aa2e-110">EXAMPLES</span></span>

### <span data-ttu-id="4aa2e-111">Beispiel 1: Alle Hybrid-Runbook-Workergruppen erhalten</span><span class="sxs-lookup"><span data-stu-id="4aa2e-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4aa2e-112">Dieser Befehl ruft alle Hybrid-Runbook-Workergruppen im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4aa2e-113">Beispiel 2: Erhalten einer einzelnen Hybrid-Runbook-Workergruppe</span><span class="sxs-lookup"><span data-stu-id="4aa2e-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="4aa2e-114">Dieser Befehl ruft die Hybrid-Runbook-Workergruppe mit dem Namen "HybridRunbookWorkerGroup01" im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4aa2e-115">Beispiel 3: Holen Sie sich die Worker in eine Hybrid-Runbook-Workergruppe.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="4aa2e-116">Dieser Befehl ruft die Hybrid-Runbook-Worker in der Hybrid-Runbook-Workergruppe mit dem Namen "HybridRunbookWorkerGroup01" im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4aa2e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aa2e-117">PARAMETERS</span></span>

### <span data-ttu-id="4aa2e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4aa2e-118">-AutomationAccountName</span></span>
<span data-ttu-id="4aa2e-119">Gibt den Namen eines Automatisierungskontos an.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="4aa2e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa2e-120">-DefaultProfile</span></span>
<span data-ttu-id="4aa2e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4aa2e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4aa2e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4aa2e-122">-Name</span></span>
<span data-ttu-id="4aa2e-123">Gibt den Gruppennamen der Hybrid-Runbook-Worker an.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aa2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="4aa2e-125">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4aa2e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa2e-126">CommonParameters</span></span>
<span data-ttu-id="4aa2e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aa2e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa2e-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa2e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa2e-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4aa2e-129">INPUTS</span></span>

### <span data-ttu-id="4aa2e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4aa2e-130">System.String</span></span>

## <span data-ttu-id="4aa2e-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4aa2e-131">OUTPUTS</span></span>

### <span data-ttu-id="4aa2e-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="4aa2e-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="4aa2e-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4aa2e-133">NOTES</span></span>

## <span data-ttu-id="4aa2e-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4aa2e-134">RELATED LINKS</span></span>
