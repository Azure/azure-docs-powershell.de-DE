---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: df6fc949fe1aa105a84ede2329c71feb4b27a449
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657985"
---
# <span data-ttu-id="a6a9c-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="a6a9c-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="a6a9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a9c-103">Ordnet eine runbooks einem Terminplan zu.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="a6a9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6a9c-104">SYNTAX</span></span>

### <span data-ttu-id="a6a9c-105">ByRunbookName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6a9c-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a9c-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="a6a9c-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6a9c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6a9c-107">DESCRIPTION</span></span>
<span data-ttu-id="a6a9c-108">Das Cmdlet " **Register-AzAutomationScheduledRunbook** " ordnet eine Azure Automation-runbooks einem Terminplan zu.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="a6a9c-109">Der runbooks beginnt basierend auf dem von Ihnen angegebenen Zeitplan mithilfe des *ScheduleName* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="a6a9c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6a9c-110">EXAMPLES</span></span>

### <span data-ttu-id="a6a9c-111">Beispiel 1: Zuordnen eines runbooks zu einem Terminplan</span><span class="sxs-lookup"><span data-stu-id="a6a9c-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a6a9c-112">Dieser Befehl ordnet die runbooks mit dem Namen Runbk01 dem Zeitplan mit dem Namen "Sched01" im Azure Automation-Konto mit dem Namen "Contoso17" zu.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a6a9c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6a9c-113">PARAMETERS</span></span>

### <span data-ttu-id="a6a9c-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6a9c-114">-AutomationAccountName</span></span>
<span data-ttu-id="a6a9c-115">Gibt ein Automatisierungs Konto für das runbooks an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a6a9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a9c-116">-DefaultProfile</span></span>
<span data-ttu-id="a6a9c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a6a9c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6a9c-118">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a6a9c-118">-Parameters</span></span>
<span data-ttu-id="a6a9c-119">Gibt eine Hashtabelle mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="a6a9c-120">Die Schlüssel sind runbooks-Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="a6a9c-121">Die Werte sind runbooks-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="a6a9c-122">Wenn der runbooks als Antwort auf den zugeordneten Zeitplan gestartet wird, werden diese Parameter an den runbooks übergeben.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="a6a9c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a9c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6a9c-124">Gibt den Namen einer Ressourcengruppe für den geplanten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="a6a9c-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a6a9c-125">-RunbookName</span></span>
<span data-ttu-id="a6a9c-126">Gibt den Namen der runbooks an, die dieses Cmdlet einem Terminplan zuordnet.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="a6a9c-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="a6a9c-127">-RunOn</span></span>
<span data-ttu-id="a6a9c-128">Der Name der Hybriden runbooks-Arbeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-128">The name of the hybrid runbook worker group.</span></span>

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

### <span data-ttu-id="a6a9c-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="a6a9c-129">-ScheduleName</span></span>
<span data-ttu-id="a6a9c-130">Gibt den Namen des Zeitplans an, dem dieses Cmdlet eine runbooks zugeordnet hat.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="a6a9c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a9c-131">CommonParameters</span></span>
<span data-ttu-id="a6a9c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6a9c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a9c-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a9c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a9c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6a9c-134">INPUTS</span></span>

### <span data-ttu-id="a6a9c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a6a9c-135">System.String</span></span>

## <span data-ttu-id="a6a9c-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6a9c-136">OUTPUTS</span></span>

### <span data-ttu-id="a6a9c-137">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="a6a9c-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="a6a9c-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6a9c-138">NOTES</span></span>

## <span data-ttu-id="a6a9c-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6a9c-139">RELATED LINKS</span></span>

[<span data-ttu-id="a6a9c-140">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="a6a9c-140">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="a6a9c-141">Registrierung aufheben-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="a6a9c-141">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


