---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 132726601b429819fa0d90186fd0d6448719df70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005152"
---
# <span data-ttu-id="6587a-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="6587a-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="6587a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6587a-102">SYNOPSIS</span></span>
<span data-ttu-id="6587a-103">Ordnet eine runbooks einem Terminplan zu.</span><span class="sxs-lookup"><span data-stu-id="6587a-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="6587a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6587a-104">SYNTAX</span></span>

### <span data-ttu-id="6587a-105">ByRunbookName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6587a-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6587a-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="6587a-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6587a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6587a-107">DESCRIPTION</span></span>
<span data-ttu-id="6587a-108">Das Cmdlet " **Register-AzAutomationScheduledRunbook** " ordnet eine Azure Automation-runbooks einem Terminplan zu.</span><span class="sxs-lookup"><span data-stu-id="6587a-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="6587a-109">Der runbooks beginnt basierend auf dem von Ihnen angegebenen Zeitplan mithilfe des *ScheduleName* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="6587a-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="6587a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6587a-110">EXAMPLES</span></span>

### <span data-ttu-id="6587a-111">Beispiel 1: Zuordnen eines runbooks zu einem Terminplan</span><span class="sxs-lookup"><span data-stu-id="6587a-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6587a-112">Dieser Befehl ordnet die runbooks mit dem Namen Runbk01 dem Zeitplan mit dem Namen "Sched01" im Azure Automation-Konto mit dem Namen "Contoso17" zu.</span><span class="sxs-lookup"><span data-stu-id="6587a-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="6587a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6587a-113">PARAMETERS</span></span>

### <span data-ttu-id="6587a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6587a-114">-AutomationAccountName</span></span>
<span data-ttu-id="6587a-115">Gibt ein Automatisierungs Konto für das runbooks an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6587a-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6587a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6587a-116">-DefaultProfile</span></span>
<span data-ttu-id="6587a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6587a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6587a-118">-Parameter</span><span class="sxs-lookup"><span data-stu-id="6587a-118">-Parameters</span></span>
<span data-ttu-id="6587a-119">Gibt eine Hashtabelle mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="6587a-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="6587a-120">Die Schlüssel sind runbooks-Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="6587a-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="6587a-121">Die Werte sind runbooks-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="6587a-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="6587a-122">Wenn der runbooks als Antwort auf den zugeordneten Zeitplan gestartet wird, werden diese Parameter an den runbooks übergeben.</span><span class="sxs-lookup"><span data-stu-id="6587a-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6587a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6587a-123">-ResourceGroupName</span></span>
<span data-ttu-id="6587a-124">Gibt den Namen einer Ressourcengruppe für den geplanten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="6587a-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="6587a-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="6587a-125">-RunbookName</span></span>
<span data-ttu-id="6587a-126">Gibt den Namen der runbooks an, die dieses Cmdlet einem Terminplan zuordnet.</span><span class="sxs-lookup"><span data-stu-id="6587a-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6587a-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="6587a-127">-RunOn</span></span>
<span data-ttu-id="6587a-128">Der Name der Hybriden runbooks-Arbeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6587a-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6587a-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="6587a-129">-ScheduleName</span></span>
<span data-ttu-id="6587a-130">Gibt den Namen des Zeitplans an, dem dieses Cmdlet eine runbooks zugeordnet hat.</span><span class="sxs-lookup"><span data-stu-id="6587a-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6587a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6587a-131">CommonParameters</span></span>
<span data-ttu-id="6587a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6587a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6587a-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6587a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6587a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6587a-134">INPUTS</span></span>

### <span data-ttu-id="6587a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6587a-135">System.String</span></span>

## <span data-ttu-id="6587a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6587a-136">OUTPUTS</span></span>

### <span data-ttu-id="6587a-137">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="6587a-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="6587a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="6587a-138">NOTES</span></span>

## <span data-ttu-id="6587a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6587a-139">RELATED LINKS</span></span>

[<span data-ttu-id="6587a-140">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="6587a-140">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="6587a-141">Registrierung aufheben-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="6587a-141">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


