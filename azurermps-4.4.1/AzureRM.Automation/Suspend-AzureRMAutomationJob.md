---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: cc9f402400b0290d8cf36dc38d59a45e29ce770c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664479"
---
# <span data-ttu-id="0a647-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0a647-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="0a647-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a647-102">SYNOPSIS</span></span>
<span data-ttu-id="0a647-103">Unterbricht einen Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="0a647-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a647-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a647-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a647-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a647-105">DESCRIPTION</span></span>
<span data-ttu-id="0a647-106">Mit dem Cmdlet **Suspend-AzureRmAutomationJob** wird ein Azure-Automatisierungs Auftrag angehalten.</span><span class="sxs-lookup"><span data-stu-id="0a647-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="0a647-107">Geben Sie einen ausgeführten Automatisierungs Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="0a647-107">Specify a running Automation job.</span></span>

<span data-ttu-id="0a647-108">Verwenden Sie das Resume-AzureRmAutomationJob-Cmdlet, um einen angehalten Job fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="0a647-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="0a647-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a647-109">EXAMPLES</span></span>

### <span data-ttu-id="0a647-110">Beispiel 1: Anhalten eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="0a647-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0a647-111">Mit diesem Befehl wird der Auftrag mit der angegebenen ID angehalten.</span><span class="sxs-lookup"><span data-stu-id="0a647-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="0a647-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a647-112">PARAMETERS</span></span>

### <span data-ttu-id="0a647-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0a647-113">-AutomationAccountName</span></span>
<span data-ttu-id="0a647-114">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen Auftrag unterbricht.</span><span class="sxs-lookup"><span data-stu-id="0a647-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="0a647-115">-ID</span><span class="sxs-lookup"><span data-stu-id="0a647-115">-Id</span></span>
<span data-ttu-id="0a647-116">Gibt die ID eines Auftrags an, der vom Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="0a647-116">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="0a647-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a647-117">-ResourceGroupName</span></span>
<span data-ttu-id="0a647-118">Gibt die ID eines Auftrags an, der vom Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="0a647-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="0a647-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a647-119">-DefaultProfile</span></span>
<span data-ttu-id="0a647-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a647-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a647-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a647-121">CommonParameters</span></span>
<span data-ttu-id="0a647-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a647-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a647-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a647-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a647-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a647-124">INPUTS</span></span>

## <span data-ttu-id="0a647-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a647-125">OUTPUTS</span></span>

## <span data-ttu-id="0a647-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a647-126">NOTES</span></span>

## <span data-ttu-id="0a647-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a647-127">RELATED LINKS</span></span>

[<span data-ttu-id="0a647-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0a647-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="0a647-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="0a647-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="0a647-130">Lebenslauf-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0a647-130">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="0a647-131">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0a647-131">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


