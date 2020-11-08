---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: a6d8a618ea9561c244b161407807ddfbe99b854a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008159"
---
# <span data-ttu-id="0e1b3-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="0e1b3-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="0e1b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1b3-103">Ruft Synchronisierungsaufträge für die Azure Automation-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="0e1b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e1b3-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e1b3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e1b3-105">DESCRIPTION</span></span>
<span data-ttu-id="0e1b3-106">Das Cmdlet "Get-AzAutomationSourceControlSyncJob" ruft Synchronisierungsaufträge für die Azure Automation-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="0e1b3-107">Um einen bestimmten Synchronisierungsauftrag für die Quellcodeverwaltung abzurufen, geben Sie dessen ID an.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="0e1b3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e1b3-108">EXAMPLES</span></span>

### <span data-ttu-id="0e1b3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e1b3-109">Example 1</span></span>
<span data-ttu-id="0e1b3-110">Dieser Befehl ruft alle Automatisierungs-Quellcodeverwaltungs-Synchronisierungsaufträge für das Quell Code Verwaltungs VSTSNative ab.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="0e1b3-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0e1b3-111">Example 2</span></span>
<span data-ttu-id="0e1b3-112">Dieser Befehl ruft den Synchronisierungsauftrag für die Quellcodeverwaltung mit ID 08d6d266-27b6-463c-beea-bc48a67ace15 für das Quell Code Verwaltungs VSTSNative ab.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative" `
                                                  -JobId "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

### <span data-ttu-id="0e1b3-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0e1b3-113">Example 3</span></span>

<span data-ttu-id="0e1b3-114">Ruft Synchronisierungsaufträge für die Azure Automation-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-114">Gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="0e1b3-115">automatisch</span><span class="sxs-lookup"><span data-stu-id="0e1b3-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAutomationSourceControlSyncJob -AutomationAccountName 'devAccount' -JobId 00000000-0000-0000-0000-00000000000000000 -ResourceGroupName 'rg1' -SourceControlName 'VSTSNative'
```

## <span data-ttu-id="0e1b3-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e1b3-116">PARAMETERS</span></span>

### <span data-ttu-id="0e1b3-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0e1b3-117">-AutomationAccountName</span></span>
<span data-ttu-id="0e1b3-118">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-118">The automation account name.</span></span>

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

### <span data-ttu-id="0e1b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1b3-119">-DefaultProfile</span></span>
<span data-ttu-id="0e1b3-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e1b3-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="0e1b3-121">-JobId</span></span>
<span data-ttu-id="0e1b3-122">Die Synchronisierungsauftrags-ID des Quellcodeverwaltungs-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-122">The source control sync job id.</span></span>

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

### <span data-ttu-id="0e1b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e1b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="0e1b3-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-124">The resource group name.</span></span>

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

### <span data-ttu-id="0e1b3-125">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="0e1b3-125">-SourceControlName</span></span>
<span data-ttu-id="0e1b3-126">Der Name des Quellsteuerelements des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-126">The source control name of the job.</span></span>

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

### <span data-ttu-id="0e1b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1b3-127">CommonParameters</span></span>
<span data-ttu-id="0e1b3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e1b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1b3-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e1b3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1b3-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e1b3-130">INPUTS</span></span>

### <span data-ttu-id="0e1b3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0e1b3-131">System.String</span></span>

### <span data-ttu-id="0e1b3-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0e1b3-132">System.Guid</span></span>

## <span data-ttu-id="0e1b3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e1b3-133">OUTPUTS</span></span>

### <span data-ttu-id="0e1b3-134">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="0e1b3-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="0e1b3-135">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="0e1b3-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="0e1b3-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e1b3-136">NOTES</span></span>

## <span data-ttu-id="0e1b3-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e1b3-137">RELATED LINKS</span></span>
