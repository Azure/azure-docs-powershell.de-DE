---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300802"
---
# <span data-ttu-id="da212-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="da212-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="da212-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da212-102">SYNOPSIS</span></span>
<span data-ttu-id="da212-103">Startet einen Synchronisierungsauftrag für die Azure Automation-Quellcodeverwaltung.</span><span class="sxs-lookup"><span data-stu-id="da212-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="da212-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da212-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da212-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da212-105">DESCRIPTION</span></span>
<span data-ttu-id="da212-106">Das Start-AzAutomationSourceControlSyncJob-Cmdlet startet einen Synchronisierungsauftrag für die Azure Automation-Quellcodeverwaltung für den angegebenen Quell Code Verwaltungs Namen.</span><span class="sxs-lookup"><span data-stu-id="da212-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="da212-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da212-107">EXAMPLES</span></span>

### <span data-ttu-id="da212-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da212-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="da212-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="da212-109">PARAMETERS</span></span>

### <span data-ttu-id="da212-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da212-110">-AutomationAccountName</span></span>
<span data-ttu-id="da212-111">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="da212-111">The automation account name.</span></span>

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

### <span data-ttu-id="da212-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da212-112">-DefaultProfile</span></span>
<span data-ttu-id="da212-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da212-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da212-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="da212-114">-JobId</span></span>
<span data-ttu-id="da212-115">Die Synchronisierungsauftrags-ID des Quellcodeverwaltungs-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="da212-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da212-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da212-116">-ResourceGroupName</span></span>
<span data-ttu-id="da212-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da212-117">The resource group name.</span></span>

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

### <span data-ttu-id="da212-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="da212-118">-SourceControlName</span></span>
<span data-ttu-id="da212-119">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="da212-119">The source control name.</span></span>

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

### <span data-ttu-id="da212-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da212-120">-Confirm</span></span>
<span data-ttu-id="da212-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da212-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da212-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da212-122">-WhatIf</span></span>
<span data-ttu-id="da212-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da212-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da212-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da212-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da212-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da212-125">CommonParameters</span></span>
<span data-ttu-id="da212-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da212-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da212-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da212-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da212-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da212-128">INPUTS</span></span>

### <span data-ttu-id="da212-129">System. String</span><span class="sxs-lookup"><span data-stu-id="da212-129">System.String</span></span>

## <span data-ttu-id="da212-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da212-130">OUTPUTS</span></span>

### <span data-ttu-id="da212-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="da212-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="da212-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="da212-132">NOTES</span></span>

## <span data-ttu-id="da212-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da212-133">RELATED LINKS</span></span>
