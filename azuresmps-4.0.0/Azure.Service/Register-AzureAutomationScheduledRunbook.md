---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006079"
---
# <span data-ttu-id="40e05-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="40e05-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="40e05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40e05-102">SYNOPSIS</span></span>

<span data-ttu-id="40e05-103">Ordnet einem runbooks einen Terminplan zu.</span><span class="sxs-lookup"><span data-stu-id="40e05-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="40e05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40e05-104">SYNTAX</span></span>

### <span data-ttu-id="40e05-105">ByRunbookName (Standard)</span><span class="sxs-lookup"><span data-stu-id="40e05-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="40e05-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="40e05-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="40e05-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40e05-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="40e05-108">Das Cmdlet " **Register-AzureAutomationScheduledRunbook** " ordnet einem runbooks einen Terminplan zu.</span><span class="sxs-lookup"><span data-stu-id="40e05-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="40e05-109">Der runbooks beginnt basierend auf dem von Ihnen angegebenen Zeitplan mithilfe des *ScheduleName* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="40e05-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="40e05-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40e05-110">EXAMPLES</span></span>

### <span data-ttu-id="40e05-111">Beispiel 1: Zuordnen eines runbooks zu einem Terminplan</span><span class="sxs-lookup"><span data-stu-id="40e05-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="40e05-112">Dieser Befehl ordnet die runbooks mit dem Namen Runbk01 dem Zeitplan mit dem Namen "Sched01" im Azure Automation-Konto mit dem Namen "Contoso17" zu.</span><span class="sxs-lookup"><span data-stu-id="40e05-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="40e05-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="40e05-113">PARAMETERS</span></span>

### <span data-ttu-id="40e05-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40e05-114">-AutomationAccountName</span></span>
<span data-ttu-id="40e05-115">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="40e05-115">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e05-116">-Parameter</span><span class="sxs-lookup"><span data-stu-id="40e05-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e05-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="40e05-117">-Profile</span></span>
<span data-ttu-id="40e05-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="40e05-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40e05-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="40e05-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e05-120">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="40e05-120">-RunbookName</span></span>
<span data-ttu-id="40e05-121">Gibt den Namen des runbooks an.</span><span class="sxs-lookup"><span data-stu-id="40e05-121">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e05-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="40e05-122">-ScheduleName</span></span>
<span data-ttu-id="40e05-123">Gibt den Namen des Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="40e05-123">Specifies the name of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e05-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e05-124">CommonParameters</span></span>
<span data-ttu-id="40e05-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e05-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e05-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e05-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e05-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40e05-127">INPUTS</span></span>

## <span data-ttu-id="40e05-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40e05-128">OUTPUTS</span></span>

### <span data-ttu-id="40e05-129">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="40e05-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="40e05-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="40e05-130">NOTES</span></span>

## <span data-ttu-id="40e05-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40e05-131">RELATED LINKS</span></span>

[<span data-ttu-id="40e05-132">Neu – AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="40e05-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="40e05-133">Registrierung aufheben-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="40e05-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


