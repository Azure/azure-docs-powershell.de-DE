---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: 0eedf88ed078c3532eb60a00b87733937344bafa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481354"
---
# <span data-ttu-id="6b091-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6b091-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="6b091-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b091-102">SYNOPSIS</span></span>
<span data-ttu-id="6b091-103">Beendet einen Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="6b091-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b091-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b091-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b091-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b091-105">DESCRIPTION</span></span>
<span data-ttu-id="6b091-106">Das Cmdlet **Stop-AzureRmAutomationJob** beendet einen Azure-Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="6b091-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="6b091-107">Geben Sie einen ausgeführten Automatisierungs Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="6b091-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="6b091-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b091-108">EXAMPLES</span></span>

### <span data-ttu-id="6b091-109">Beispiel 1: Beenden eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="6b091-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6b091-110">Mit diesem Befehl wird der Auftrag beendet, der die angegebene ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="6b091-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="6b091-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b091-111">PARAMETERS</span></span>

### <span data-ttu-id="6b091-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6b091-112">-AutomationAccountName</span></span>
<span data-ttu-id="6b091-113">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen Auftrag stoppt.</span><span class="sxs-lookup"><span data-stu-id="6b091-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b091-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b091-114">-DefaultProfile</span></span>
<span data-ttu-id="6b091-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6b091-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b091-116">-ID</span><span class="sxs-lookup"><span data-stu-id="6b091-116">-Id</span></span>
<span data-ttu-id="6b091-117">Gibt die ID eines Auftrags an, der vom Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b091-117">Specifies the ID of a job that this cmdlet stops.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b091-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b091-118">-ResourceGroupName</span></span>
<span data-ttu-id="6b091-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6b091-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b091-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b091-120">CommonParameters</span></span>
<span data-ttu-id="6b091-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b091-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b091-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b091-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b091-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b091-123">INPUTS</span></span>

### <span data-ttu-id="6b091-124">Keine</span><span class="sxs-lookup"><span data-stu-id="6b091-124">None</span></span>
<span data-ttu-id="6b091-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6b091-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b091-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b091-126">OUTPUTS</span></span>

## <span data-ttu-id="6b091-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b091-127">NOTES</span></span>

## <span data-ttu-id="6b091-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b091-128">RELATED LINKS</span></span>

[<span data-ttu-id="6b091-129">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6b091-129">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="6b091-130">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="6b091-130">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="6b091-131">Lebenslauf-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6b091-131">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="6b091-132">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6b091-132">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


