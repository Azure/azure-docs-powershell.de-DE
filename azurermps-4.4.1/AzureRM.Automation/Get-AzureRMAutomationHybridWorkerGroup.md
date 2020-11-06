---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 1f2c82bc51cb5faba9f5b1dd0524e7aced2f0b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500969"
---
# <span data-ttu-id="9f81b-101">Get-AzureRMAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="9f81b-101">Get-AzureRMAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="9f81b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f81b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f81b-103">Ruft Hybrid-runbooks-Arbeitsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="9f81b-103">Gets hybrid runbook worker groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f81b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f81b-104">SYNTAX</span></span>

### <span data-ttu-id="9f81b-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f81b-105">ByAll (Default)</span></span>
```
Get-AzureRMAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f81b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9f81b-106">ByName</span></span>
```
Get-AzureRMAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f81b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f81b-107">DESCRIPTION</span></span>
<span data-ttu-id="9f81b-108">Das Cmdlet " **Get-AzureRmAutomationHybridWorkerGroup** " ruft Azure Automation Hybrid runbooks Worker Groups ab.</span><span class="sxs-lookup"><span data-stu-id="9f81b-108">The **Get-AzureRmAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="9f81b-109">Um eine bestimmte Gruppe zu erhalten, geben Sie den Namen an.</span><span class="sxs-lookup"><span data-stu-id="9f81b-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="9f81b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f81b-110">EXAMPLES</span></span>

### <span data-ttu-id="9f81b-111">Beispiel 1: Abrufen aller Hybrid runbooks Worker-Gruppen</span><span class="sxs-lookup"><span data-stu-id="9f81b-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="9f81b-112">Dieser Befehl ruft alle Hybriden runbooks-Arbeitsgruppen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="9f81b-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9f81b-113">Beispiel 2: Abrufen einer einzelnen Hybriden runbooks Worker-Gruppe</span><span class="sxs-lookup"><span data-stu-id="9f81b-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="9f81b-114">Dieser Befehl ruft die Hybrid-runbooks-Arbeitsgruppe mit dem Namen HybridRunbookWorkerGroup01 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="9f81b-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9f81b-115">Beispiel 3: Abrufen der Arbeitskräfte in einer hybriden runbooks Worker-Gruppe</span><span class="sxs-lookup"><span data-stu-id="9f81b-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="9f81b-116">Dieser Befehl ruft die Hybrid-runbooks-worker in der Hybrid-runbooks-Arbeitsgruppe mit dem Namen HybridRunbookWorkerGroup01 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="9f81b-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9f81b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f81b-117">PARAMETERS</span></span>

### <span data-ttu-id="9f81b-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f81b-118">-AutomationAccountName</span></span>
<span data-ttu-id="9f81b-119">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9f81b-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="9f81b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9f81b-120">-Name</span></span>
<span data-ttu-id="9f81b-121">Gibt den Namen der Hybriden runbooks-Arbeitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="9f81b-121">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="9f81b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f81b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f81b-123">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9f81b-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9f81b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f81b-124">-DefaultProfile</span></span>
<span data-ttu-id="9f81b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f81b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f81b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f81b-126">CommonParameters</span></span>
<span data-ttu-id="9f81b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f81b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f81b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f81b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f81b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f81b-129">INPUTS</span></span>

### <span data-ttu-id="9f81b-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9f81b-130">String</span></span>
<span data-ttu-id="9f81b-131">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f81b-131">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9f81b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f81b-132">OUTPUTS</span></span>

### <span data-ttu-id="9f81b-133">Microsoft. Azure. Commands. Automation. Model. HybridRunbookWorker</span><span class="sxs-lookup"><span data-stu-id="9f81b-133">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorker</span></span>

## <span data-ttu-id="9f81b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f81b-134">NOTES</span></span>

## <span data-ttu-id="9f81b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f81b-135">RELATED LINKS</span></span>

