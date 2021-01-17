---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: a6d8a618ea9561c244b161407807ddfbe99b854a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471336"
---
# <span data-ttu-id="bea29-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="bea29-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="bea29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea29-102">SYNOPSIS</span></span>
<span data-ttu-id="bea29-103">Ruft Synchronisierungsaufträge für die Azure Automation-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="bea29-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="bea29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bea29-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bea29-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bea29-105">DESCRIPTION</span></span>
<span data-ttu-id="bea29-106">Das Get-AzAutomationSourceControlSyncJob ruft Synchronisierungsaufträge für die Azure-Automatisierungs-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="bea29-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="bea29-107">Um einen bestimmten Synchronisierungsauftrag für die Quellcodeverwaltung zu erhalten, geben Sie dessen ID an.</span><span class="sxs-lookup"><span data-stu-id="bea29-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="bea29-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bea29-108">EXAMPLES</span></span>

### <span data-ttu-id="bea29-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bea29-109">Example 1</span></span>
<span data-ttu-id="bea29-110">Dieser Befehl ruft alle Synchronisierungsaufträge des Automatisierungsquellensteuerelements für das Quellsteuerelement VSTSNative ab.</span><span class="sxs-lookup"><span data-stu-id="bea29-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="bea29-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bea29-111">Example 2</span></span>
<span data-ttu-id="bea29-112">Dieser Befehl ruft den Synchronisierungsauftrag für die Quellcodeverwaltung mit der ID 08d6d266-27b6-463c-beea-bc48a67ace15 für das Quellsteuerelement VSTSNative ab.</span><span class="sxs-lookup"><span data-stu-id="bea29-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative" `
                                                  -JobId "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

### <span data-ttu-id="bea29-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="bea29-113">Example 3</span></span>

<span data-ttu-id="bea29-114">Ruft Synchronisierungsaufträge für die Azure Automation-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="bea29-114">Gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="bea29-115">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="bea29-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAutomationSourceControlSyncJob -AutomationAccountName 'devAccount' -JobId 00000000-0000-0000-0000-00000000000000000 -ResourceGroupName 'rg1' -SourceControlName 'VSTSNative'
```

## <span data-ttu-id="bea29-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bea29-116">PARAMETERS</span></span>

### <span data-ttu-id="bea29-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bea29-117">-AutomationAccountName</span></span>
<span data-ttu-id="bea29-118">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="bea29-118">The automation account name.</span></span>

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

### <span data-ttu-id="bea29-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea29-119">-DefaultProfile</span></span>
<span data-ttu-id="bea29-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bea29-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea29-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="bea29-121">-JobId</span></span>
<span data-ttu-id="bea29-122">Die ID des Synchronisierungsauftrags der Quellcodeverwaltung.</span><span class="sxs-lookup"><span data-stu-id="bea29-122">The source control sync job id.</span></span>

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

### <span data-ttu-id="bea29-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea29-123">-ResourceGroupName</span></span>
<span data-ttu-id="bea29-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bea29-124">The resource group name.</span></span>

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

### <span data-ttu-id="bea29-125">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="bea29-125">-SourceControlName</span></span>
<span data-ttu-id="bea29-126">Der Name des Quellcodeverwaltungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="bea29-126">The source control name of the job.</span></span>

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

### <span data-ttu-id="bea29-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea29-127">CommonParameters</span></span>
<span data-ttu-id="bea29-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea29-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea29-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea29-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea29-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bea29-130">INPUTS</span></span>

### <span data-ttu-id="bea29-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bea29-131">System.String</span></span>

### <span data-ttu-id="bea29-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bea29-132">System.Guid</span></span>

## <span data-ttu-id="bea29-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bea29-133">OUTPUTS</span></span>

### <span data-ttu-id="bea29-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="bea29-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="bea29-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="bea29-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="bea29-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bea29-136">NOTES</span></span>

## <span data-ttu-id="bea29-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bea29-137">RELATED LINKS</span></span>
