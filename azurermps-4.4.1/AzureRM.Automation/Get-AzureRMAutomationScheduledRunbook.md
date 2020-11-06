---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: fe8d7b4407aa5afc3454d80e4cf45c102d9006bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505674"
---
# <span data-ttu-id="aa732-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="aa732-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="aa732-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa732-102">SYNOPSIS</span></span>
<span data-ttu-id="aa732-103">Ruft Automatisierungs runbooks und zugeordnete Zeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="aa732-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa732-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa732-104">SYNTAX</span></span>

### <span data-ttu-id="aa732-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa732-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa732-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="aa732-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa732-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="aa732-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa732-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="aa732-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa732-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="aa732-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa732-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa732-110">DESCRIPTION</span></span>
<span data-ttu-id="aa732-111">Das Cmdlet " **Get-AzureRmAutomationScheduledRunbook** " Ruft einen oder mehrere Azure Automation-runbooks und zugeordnete Zeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="aa732-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="aa732-112">Standardmäßig ruft dieses Cmdlet alle geplanten runbooks ab.</span><span class="sxs-lookup"><span data-stu-id="aa732-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="aa732-113">Geben Sie den Namen eines runbooks oder einen Terminplan oder beides an, um bestimmte runbooks-Zeitpläne anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa732-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="aa732-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa732-114">EXAMPLES</span></span>

### <span data-ttu-id="aa732-115">Beispiel 1: Abrufen aller geplanten runbooks</span><span class="sxs-lookup"><span data-stu-id="aa732-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aa732-116">Dieser Befehl ruft alle geplanten runbooks im Azure Automation-Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="aa732-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="aa732-117">Beispiel 2: Abrufen aller einem runbooks zugeordneten Zeitpläne</span><span class="sxs-lookup"><span data-stu-id="aa732-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="aa732-118">Dieser Befehl ruft alle geplanten runbooks für das runbooks-Runbk01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="aa732-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="aa732-119">Beispiel 3: Abrufen aller runbooks, die einem Terminplan zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="aa732-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="aa732-120">Dieser Befehl ruft alle geplanten runbooks für den Terminplan-Schedule01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="aa732-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="aa732-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa732-121">PARAMETERS</span></span>

### <span data-ttu-id="aa732-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aa732-122">-AutomationAccountName</span></span>
<span data-ttu-id="aa732-123">Gibt ein Automatisierungs Konto für das runbooks an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa732-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aa732-124">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="aa732-124">-JobScheduleId</span></span>
<span data-ttu-id="aa732-125">Gibt die ID eines geplanten Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="aa732-125">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa732-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa732-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa732-127">Gibt den Namen einer Ressourcengruppe für geplante runbooks an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="aa732-127">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aa732-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="aa732-128">-RunbookName</span></span>
<span data-ttu-id="aa732-129">Gibt den Namen einer runbooks an, für die dieses Cmdlet geplante runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="aa732-129">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa732-130">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="aa732-130">-ScheduleName</span></span>
<span data-ttu-id="aa732-131">Gibt den Namen eines Zeitplans an, für den dieses Cmdlet geplante runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="aa732-131">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa732-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa732-132">-DefaultProfile</span></span>
<span data-ttu-id="aa732-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa732-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa732-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa732-134">CommonParameters</span></span>
<span data-ttu-id="aa732-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa732-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa732-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa732-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa732-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa732-137">INPUTS</span></span>

## <span data-ttu-id="aa732-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa732-138">OUTPUTS</span></span>

### <span data-ttu-id="aa732-139">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="aa732-139">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="aa732-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa732-140">NOTES</span></span>

## <span data-ttu-id="aa732-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa732-141">RELATED LINKS</span></span>

[<span data-ttu-id="aa732-142">Registrieren-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="aa732-142">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="aa732-143">Registrierung aufheben-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="aa732-143">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


