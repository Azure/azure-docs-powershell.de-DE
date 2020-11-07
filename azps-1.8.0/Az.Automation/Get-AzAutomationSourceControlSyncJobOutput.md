---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 63ff1ea82f3167738161191900e9516513b034bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661795"
---
# <span data-ttu-id="c54e8-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="c54e8-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="c54e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c54e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c54e8-103">Ruft die Ausgabe eines Synchronisierungsauftrags für die Azure Automation-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="c54e8-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="c54e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c54e8-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c54e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c54e8-105">DESCRIPTION</span></span>
<span data-ttu-id="c54e8-106">Das Cmdlet " **Get-AzAutomationSourceControlSyncJobOutput** " Ruft die Ausgabe für einen Synchronisierungsauftrag für die Azure Automation-Quellcodeverwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="c54e8-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="c54e8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c54e8-107">EXAMPLES</span></span>

### <span data-ttu-id="c54e8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c54e8-108">Example 1</span></span>
<span data-ttu-id="c54e8-109">Dieser Befehl ruft die Ausgabe des Synchronisierungsauftrags für die Quellcodeverwaltung mit ID 08d6d266-27b6-463c-beea-bc48a67ace15 für das Quell Code Verwaltungs VSTSNative ab.</span><span class="sxs-lookup"><span data-stu-id="c54e8-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="c54e8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c54e8-110">PARAMETERS</span></span>

### <span data-ttu-id="c54e8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c54e8-111">-AutomationAccountName</span></span>
<span data-ttu-id="c54e8-112">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="c54e8-112">The automation account name.</span></span>

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

### <span data-ttu-id="c54e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c54e8-113">-DefaultProfile</span></span>
<span data-ttu-id="c54e8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c54e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c54e8-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="c54e8-115">-JobId</span></span>
<span data-ttu-id="c54e8-116">Die Synchronisierungsauftrags-ID des Quellcodeverwaltungs-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="c54e8-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c54e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="c54e8-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c54e8-118">The resource group name.</span></span>

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

### <span data-ttu-id="c54e8-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="c54e8-119">-SourceControlName</span></span>
<span data-ttu-id="c54e8-120">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="c54e8-120">The source control name.</span></span>

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

### <span data-ttu-id="c54e8-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="c54e8-121">-Stream</span></span>
<span data-ttu-id="c54e8-122">Der Stream-Typ.</span><span class="sxs-lookup"><span data-stu-id="c54e8-122">The stream type.</span></span>
<span data-ttu-id="c54e8-123">Standardmäßig auf Any.</span><span class="sxs-lookup"><span data-stu-id="c54e8-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54e8-124">-Datenstrom-Nr.</span><span class="sxs-lookup"><span data-stu-id="c54e8-124">-StreamId</span></span>
<span data-ttu-id="c54e8-125">Die Datenstrom-ID.</span><span class="sxs-lookup"><span data-stu-id="c54e8-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c54e8-126">CommonParameters</span></span>
<span data-ttu-id="c54e8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c54e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c54e8-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c54e8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c54e8-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c54e8-129">INPUTS</span></span>

### <span data-ttu-id="c54e8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c54e8-130">System.String</span></span>

### <span data-ttu-id="c54e8-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c54e8-131">System.Guid</span></span>

### <span data-ttu-id="c54e8-132">Microsoft. Azure. Commands. Automation. Common. SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="c54e8-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="c54e8-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c54e8-133">OUTPUTS</span></span>

### <span data-ttu-id="c54e8-134">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="c54e8-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="c54e8-135">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="c54e8-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="c54e8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c54e8-136">NOTES</span></span>

## <span data-ttu-id="c54e8-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c54e8-137">RELATED LINKS</span></span>
