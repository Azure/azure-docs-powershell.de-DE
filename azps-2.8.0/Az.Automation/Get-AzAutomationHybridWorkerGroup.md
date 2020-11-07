---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 7481975d880d3d43508756ac2daec3e665878ee0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658052"
---
# <span data-ttu-id="95a1b-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="95a1b-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="95a1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="95a1b-103">Ruft Hybrid-runbooks-Arbeitsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="95a1b-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="95a1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95a1b-104">SYNTAX</span></span>

### <span data-ttu-id="95a1b-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="95a1b-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95a1b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="95a1b-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95a1b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95a1b-107">DESCRIPTION</span></span>
<span data-ttu-id="95a1b-108">Das Cmdlet " **Get-AzAutomationHybridWorkerGroup** " ruft Azure Automation Hybrid runbooks Worker Groups ab.</span><span class="sxs-lookup"><span data-stu-id="95a1b-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="95a1b-109">Um eine bestimmte Gruppe zu erhalten, geben Sie den Namen an.</span><span class="sxs-lookup"><span data-stu-id="95a1b-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="95a1b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95a1b-110">EXAMPLES</span></span>

### <span data-ttu-id="95a1b-111">Beispiel 1: Abrufen aller Hybrid runbooks Worker-Gruppen</span><span class="sxs-lookup"><span data-stu-id="95a1b-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="95a1b-112">Dieser Befehl ruft alle Hybriden runbooks-Arbeitsgruppen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="95a1b-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="95a1b-113">Beispiel 2: Abrufen einer einzelnen Hybriden runbooks Worker-Gruppe</span><span class="sxs-lookup"><span data-stu-id="95a1b-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="95a1b-114">Dieser Befehl ruft die Hybrid-runbooks-Arbeitsgruppe mit dem Namen HybridRunbookWorkerGroup01 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="95a1b-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="95a1b-115">Beispiel 3: Abrufen der Arbeitskräfte in einer hybriden runbooks Worker-Gruppe</span><span class="sxs-lookup"><span data-stu-id="95a1b-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="95a1b-116">Dieser Befehl ruft die Hybrid-runbooks-worker in der Hybrid-runbooks-Arbeitsgruppe mit dem Namen HybridRunbookWorkerGroup01 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="95a1b-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="95a1b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="95a1b-117">PARAMETERS</span></span>

### <span data-ttu-id="95a1b-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="95a1b-118">-AutomationAccountName</span></span>
<span data-ttu-id="95a1b-119">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="95a1b-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="95a1b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95a1b-120">-DefaultProfile</span></span>
<span data-ttu-id="95a1b-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="95a1b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95a1b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="95a1b-122">-Name</span></span>
<span data-ttu-id="95a1b-123">Gibt den Namen der Hybriden runbooks-Arbeitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="95a1b-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="95a1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="95a1b-125">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="95a1b-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="95a1b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a1b-126">CommonParameters</span></span>
<span data-ttu-id="95a1b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a1b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a1b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a1b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a1b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95a1b-129">INPUTS</span></span>

### <span data-ttu-id="95a1b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="95a1b-130">System.String</span></span>

## <span data-ttu-id="95a1b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95a1b-131">OUTPUTS</span></span>

### <span data-ttu-id="95a1b-132">Microsoft. Azure. Commands. Automation. Model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="95a1b-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="95a1b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="95a1b-133">NOTES</span></span>

## <span data-ttu-id="95a1b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95a1b-134">RELATED LINKS</span></span>
