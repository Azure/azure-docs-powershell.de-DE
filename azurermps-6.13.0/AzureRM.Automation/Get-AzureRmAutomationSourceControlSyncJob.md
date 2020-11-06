---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 213df264e4ecd458c8505d521556f49265577333
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501214"
---
# <span data-ttu-id="be944-101">Get-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="be944-101">Get-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="be944-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be944-102">SYNOPSIS</span></span>
<span data-ttu-id="be944-103">Ruft Synchronisierungsaufträge für die Azure Automation-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="be944-103">Gets Azure Automation source control sync jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be944-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be944-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be944-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be944-105">DESCRIPTION</span></span>
<span data-ttu-id="be944-106">Das Cmdlet "Get-AzureRmAutomationSourceControlSyncJob" ruft Synchronisierungsaufträge für die Azure Automation-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="be944-106">The Get-AzureRmAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="be944-107">Um einen bestimmten Synchronisierungsauftrag für die Quellcodeverwaltung abzurufen, geben Sie dessen ID an.</span><span class="sxs-lookup"><span data-stu-id="be944-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="be944-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be944-108">EXAMPLES</span></span>

### <span data-ttu-id="be944-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be944-109">Example 1</span></span>
<span data-ttu-id="be944-110">Dieser Befehl ruft alle Automatisierungs-Quellcodeverwaltungs-Synchronisierungsaufträge für das Quell Code Verwaltungs VSTSNative ab.</span><span class="sxs-lookup"><span data-stu-id="be944-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="be944-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="be944-111">Example 2</span></span>
<span data-ttu-id="be944-112">Dieser Befehl ruft den Synchronisierungsauftrag für die Quellcodeverwaltung mit ID 08d6d266-27b6-463c-beea-bc48a67ace15 für das Quell Code Verwaltungs VSTSNative ab.</span><span class="sxs-lookup"><span data-stu-id="be944-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="be944-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="be944-113">PARAMETERS</span></span>

### <span data-ttu-id="be944-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="be944-114">-AutomationAccountName</span></span>
<span data-ttu-id="be944-115">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="be944-115">The automation account name.</span></span>

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

### <span data-ttu-id="be944-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be944-116">-DefaultProfile</span></span>
<span data-ttu-id="be944-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be944-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be944-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="be944-118">-JobId</span></span>
<span data-ttu-id="be944-119">Die Synchronisierungsauftrags-ID des Quellcodeverwaltungs-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="be944-119">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be944-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be944-120">-ResourceGroupName</span></span>
<span data-ttu-id="be944-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="be944-121">The resource group name.</span></span>

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

### <span data-ttu-id="be944-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="be944-122">-SourceControlName</span></span>
<span data-ttu-id="be944-123">Der Name des Quellsteuerelements des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="be944-123">The source control name of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be944-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be944-124">CommonParameters</span></span>
<span data-ttu-id="be944-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be944-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be944-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be944-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be944-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be944-127">INPUTS</span></span>

### <span data-ttu-id="be944-128">System. String</span><span class="sxs-lookup"><span data-stu-id="be944-128">System.String</span></span>

### <span data-ttu-id="be944-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="be944-129">System.Guid</span></span>

## <span data-ttu-id="be944-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be944-130">OUTPUTS</span></span>

### <span data-ttu-id="be944-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="be944-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="be944-132">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="be944-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="be944-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="be944-133">NOTES</span></span>

## <span data-ttu-id="be944-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be944-134">RELATED LINKS</span></span>
