---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 9559a599a6d0a50078dbec176ad937947facce7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661688"
---
# <span data-ttu-id="06e05-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="06e05-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="06e05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06e05-102">SYNOPSIS</span></span>
<span data-ttu-id="06e05-103">Beendet einen Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="06e05-103">Stops an Automation job.</span></span>

## <span data-ttu-id="06e05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06e05-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06e05-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06e05-105">DESCRIPTION</span></span>
<span data-ttu-id="06e05-106">Das Cmdlet **Stop-AzAutomationJob** beendet einen Azure-Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="06e05-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="06e05-107">Geben Sie einen ausgeführten Automatisierungs Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="06e05-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="06e05-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06e05-108">EXAMPLES</span></span>

### <span data-ttu-id="06e05-109">Beispiel 1: Beenden eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="06e05-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="06e05-110">Mit diesem Befehl wird der Auftrag beendet, der die angegebene ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="06e05-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="06e05-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="06e05-111">PARAMETERS</span></span>

### <span data-ttu-id="06e05-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="06e05-112">-AutomationAccountName</span></span>
<span data-ttu-id="06e05-113">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen Auftrag stoppt.</span><span class="sxs-lookup"><span data-stu-id="06e05-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="06e05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e05-114">-DefaultProfile</span></span>
<span data-ttu-id="06e05-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="06e05-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06e05-116">-ID</span><span class="sxs-lookup"><span data-stu-id="06e05-116">-Id</span></span>
<span data-ttu-id="06e05-117">Gibt die ID eines Auftrags an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="06e05-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="06e05-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e05-118">-ResourceGroupName</span></span>
<span data-ttu-id="06e05-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="06e05-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="06e05-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e05-120">CommonParameters</span></span>
<span data-ttu-id="06e05-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e05-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e05-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e05-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e05-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06e05-123">INPUTS</span></span>

### <span data-ttu-id="06e05-124">System. GUID</span><span class="sxs-lookup"><span data-stu-id="06e05-124">System.Guid</span></span>

### <span data-ttu-id="06e05-125">System. String</span><span class="sxs-lookup"><span data-stu-id="06e05-125">System.String</span></span>

## <span data-ttu-id="06e05-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06e05-126">OUTPUTS</span></span>

### <span data-ttu-id="06e05-127">System. void</span><span class="sxs-lookup"><span data-stu-id="06e05-127">System.Void</span></span>

## <span data-ttu-id="06e05-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="06e05-128">NOTES</span></span>

## <span data-ttu-id="06e05-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06e05-129">RELATED LINKS</span></span>

[<span data-ttu-id="06e05-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="06e05-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="06e05-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="06e05-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="06e05-132">Lebenslauf-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="06e05-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="06e05-133">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="06e05-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


