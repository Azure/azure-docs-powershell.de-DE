---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 6d23fe3728b569cbb1a2aee498d560672ee75877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497930"
---
# <span data-ttu-id="dc80e-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dc80e-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="dc80e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc80e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc80e-103">Setzt einen angehalten Automatisierungs Auftrag fort.</span><span class="sxs-lookup"><span data-stu-id="dc80e-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc80e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc80e-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc80e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc80e-105">DESCRIPTION</span></span>
<span data-ttu-id="dc80e-106">Das Cmdlet **Resume-AzureRmAutomationJob** setzt einen angehenden Azure-Automatisierungs Auftrag fort.</span><span class="sxs-lookup"><span data-stu-id="dc80e-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="dc80e-107">Geben Sie den angehenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="dc80e-107">Specify the suspended job.</span></span>

<span data-ttu-id="dc80e-108">Verwenden Sie das Suspend-AzureRmAutomationJob-Cmdlet, um einen Auftrag zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="dc80e-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="dc80e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc80e-109">EXAMPLES</span></span>

### <span data-ttu-id="dc80e-110">Beispiel 1: Fortsetzen eines angehenden Auftrags</span><span class="sxs-lookup"><span data-stu-id="dc80e-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dc80e-111">Mit diesem Befehl wird der Auftrag mit der angegebenen ID fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="dc80e-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="dc80e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc80e-112">PARAMETERS</span></span>

### <span data-ttu-id="dc80e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dc80e-113">-AutomationAccountName</span></span>
<span data-ttu-id="dc80e-114">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen Auftrag fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="dc80e-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="dc80e-115">-ID</span><span class="sxs-lookup"><span data-stu-id="dc80e-115">-Id</span></span>
<span data-ttu-id="dc80e-116">Gibt die ID eines Auftrags an, den dieses Cmdlet fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="dc80e-116">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="dc80e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc80e-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc80e-118">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Auftrag fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="dc80e-118">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="dc80e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc80e-119">-DefaultProfile</span></span>
<span data-ttu-id="dc80e-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc80e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc80e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc80e-121">CommonParameters</span></span>
<span data-ttu-id="dc80e-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc80e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc80e-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc80e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc80e-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc80e-124">INPUTS</span></span>

## <span data-ttu-id="dc80e-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc80e-125">OUTPUTS</span></span>

## <span data-ttu-id="dc80e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc80e-126">NOTES</span></span>

## <span data-ttu-id="dc80e-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc80e-127">RELATED LINKS</span></span>

[<span data-ttu-id="dc80e-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dc80e-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="dc80e-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="dc80e-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="dc80e-130">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dc80e-130">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="dc80e-131">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dc80e-131">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


