---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: 67100c80a3a0ca822fc1f37f63968be282925b76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477981"
---
# <span data-ttu-id="be5fe-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="be5fe-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="be5fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="be5fe-103">Beendet einen Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="be5fe-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be5fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be5fe-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be5fe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be5fe-105">DESCRIPTION</span></span>
<span data-ttu-id="be5fe-106">Das Cmdlet **Stop-AzureRmAutomationJob** beendet einen Azure-Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="be5fe-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="be5fe-107">Geben Sie einen ausgeführten Automatisierungs Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="be5fe-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="be5fe-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be5fe-108">EXAMPLES</span></span>

### <span data-ttu-id="be5fe-109">Beispiel 1: Beenden eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="be5fe-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="be5fe-110">Mit diesem Befehl wird der Auftrag beendet, der die angegebene ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="be5fe-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="be5fe-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="be5fe-111">PARAMETERS</span></span>

### <span data-ttu-id="be5fe-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="be5fe-112">-AutomationAccountName</span></span>
<span data-ttu-id="be5fe-113">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen Auftrag stoppt.</span><span class="sxs-lookup"><span data-stu-id="be5fe-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="be5fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5fe-114">-DefaultProfile</span></span>
<span data-ttu-id="be5fe-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="be5fe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be5fe-116">-ID</span><span class="sxs-lookup"><span data-stu-id="be5fe-116">-Id</span></span>
<span data-ttu-id="be5fe-117">Gibt die ID eines Auftrags an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="be5fe-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="be5fe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be5fe-118">-ResourceGroupName</span></span>
<span data-ttu-id="be5fe-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="be5fe-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="be5fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5fe-120">CommonParameters</span></span>
<span data-ttu-id="be5fe-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be5fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5fe-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be5fe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5fe-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be5fe-123">INPUTS</span></span>

### <span data-ttu-id="be5fe-124">System. GUID</span><span class="sxs-lookup"><span data-stu-id="be5fe-124">System.Guid</span></span>

### <span data-ttu-id="be5fe-125">System. String</span><span class="sxs-lookup"><span data-stu-id="be5fe-125">System.String</span></span>

## <span data-ttu-id="be5fe-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be5fe-126">OUTPUTS</span></span>

### <span data-ttu-id="be5fe-127">System. void</span><span class="sxs-lookup"><span data-stu-id="be5fe-127">System.Void</span></span>

## <span data-ttu-id="be5fe-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="be5fe-128">NOTES</span></span>

## <span data-ttu-id="be5fe-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be5fe-129">RELATED LINKS</span></span>

[<span data-ttu-id="be5fe-130">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="be5fe-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="be5fe-131">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="be5fe-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="be5fe-132">Lebenslauf-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="be5fe-132">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="be5fe-133">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="be5fe-133">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


