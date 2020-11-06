---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: e58f3d429d036afa13f82e8e140ca8195eed612a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477370"
---
# <span data-ttu-id="07ba4-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="07ba4-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="07ba4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="07ba4-103">Ordnet eine runbooks einem Terminplan zu.</span><span class="sxs-lookup"><span data-stu-id="07ba4-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07ba4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07ba4-104">SYNTAX</span></span>

### <span data-ttu-id="07ba4-105">ByRunbookName (Standard)</span><span class="sxs-lookup"><span data-stu-id="07ba4-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07ba4-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="07ba4-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ba4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07ba4-107">DESCRIPTION</span></span>
<span data-ttu-id="07ba4-108">Das Cmdlet " **Register-AzureRmAutomationScheduledRunbook** " ordnet eine Azure Automation-runbooks einem Terminplan zu.</span><span class="sxs-lookup"><span data-stu-id="07ba4-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="07ba4-109">Der runbooks beginnt basierend auf dem von Ihnen angegebenen Zeitplan mithilfe des *ScheduleName* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="07ba4-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="07ba4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07ba4-110">EXAMPLES</span></span>

### <span data-ttu-id="07ba4-111">Beispiel 1: Zuordnen eines runbooks zu einem Terminplan</span><span class="sxs-lookup"><span data-stu-id="07ba4-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="07ba4-112">Dieser Befehl ordnet die runbooks mit dem Namen Runbk01 dem Zeitplan mit dem Namen "Sched01" im Azure Automation-Konto mit dem Namen "Contoso17" zu.</span><span class="sxs-lookup"><span data-stu-id="07ba4-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="07ba4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="07ba4-113">PARAMETERS</span></span>

### <span data-ttu-id="07ba4-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="07ba4-114">-AutomationAccountName</span></span>
<span data-ttu-id="07ba4-115">Gibt ein Automatisierungs Konto für das runbooks an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07ba4-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="07ba4-116">-Parameter</span><span class="sxs-lookup"><span data-stu-id="07ba4-116">-Parameters</span></span>
<span data-ttu-id="07ba4-117">Gibt eine Hashtabelle mit Schlüssel-Wert-Paaren an.</span><span class="sxs-lookup"><span data-stu-id="07ba4-117">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="07ba4-118">Die Schlüssel sind runbooks-Parameternamen.</span><span class="sxs-lookup"><span data-stu-id="07ba4-118">The keys are runbook parameter names.</span></span>
<span data-ttu-id="07ba4-119">Die Werte sind runbooks-Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="07ba4-119">The values are runbook parameter values.</span></span>
<span data-ttu-id="07ba4-120">Wenn der runbooks als Antwort auf den zugeordneten Zeitplan gestartet wird, werden diese Parameter an den runbooks übergeben.</span><span class="sxs-lookup"><span data-stu-id="07ba4-120">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="07ba4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ba4-121">-ResourceGroupName</span></span>
<span data-ttu-id="07ba4-122">Gibt den Namen einer Ressourcengruppe für den geplanten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="07ba4-122">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="07ba4-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="07ba4-123">-RunbookName</span></span>
<span data-ttu-id="07ba4-124">Gibt den Namen der runbooks an, die dieses Cmdlet einem Terminplan zuordnet.</span><span class="sxs-lookup"><span data-stu-id="07ba4-124">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="07ba4-125">-RunOn</span><span class="sxs-lookup"><span data-stu-id="07ba4-125">-RunOn</span></span>
<span data-ttu-id="07ba4-126">Der Name der Hybriden runbooks-Arbeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="07ba4-126">The name of the hybrid runbook worker group.</span></span>

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

### <span data-ttu-id="07ba4-127">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="07ba4-127">-ScheduleName</span></span>
<span data-ttu-id="07ba4-128">Gibt den Namen des Zeitplans an, dem dieses Cmdlet eine runbooks zugeordnet hat.</span><span class="sxs-lookup"><span data-stu-id="07ba4-128">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="07ba4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ba4-129">-DefaultProfile</span></span>
<span data-ttu-id="07ba4-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07ba4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07ba4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ba4-131">CommonParameters</span></span>
<span data-ttu-id="07ba4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ba4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ba4-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ba4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ba4-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07ba4-134">INPUTS</span></span>

## <span data-ttu-id="07ba4-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07ba4-135">OUTPUTS</span></span>

### <span data-ttu-id="07ba4-136">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="07ba4-136">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="07ba4-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="07ba4-137">NOTES</span></span>

## <span data-ttu-id="07ba4-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07ba4-138">RELATED LINKS</span></span>

[<span data-ttu-id="07ba4-139">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="07ba4-139">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="07ba4-140">Registrierung aufheben-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="07ba4-140">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


