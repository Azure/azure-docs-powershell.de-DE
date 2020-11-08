---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008128"
---
# <span data-ttu-id="35d02-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="35d02-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="35d02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35d02-102">SYNOPSIS</span></span>
<span data-ttu-id="35d02-103">Erstellt Azure-Automatisierungs-Software Update-Konfigurations Azure Query-Objekt.</span><span class="sxs-lookup"><span data-stu-id="35d02-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="35d02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35d02-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35d02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35d02-105">DESCRIPTION</span></span>
<span data-ttu-id="35d02-106">Erstellt ein Azure Querys-Objekt für Software Update Konfiguration, das zum Erstellen einer Software Update Konfiguration verwendet wird, die nach einem Zeitplan ausgeführt wird, um eine Liste dynamisch aufgelöster Azure Virtual Machines zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="35d02-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="35d02-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35d02-107">EXAMPLES</span></span>

### <span data-ttu-id="35d02-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35d02-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="35d02-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="35d02-109">PARAMETERS</span></span>

### <span data-ttu-id="35d02-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="35d02-110">-AutomationAccountName</span></span>
<span data-ttu-id="35d02-111">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="35d02-111">The automation account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35d02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d02-112">-DefaultProfile</span></span>
<span data-ttu-id="35d02-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35d02-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d02-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="35d02-114">-FilterOperator</span></span>
<span data-ttu-id="35d02-115">Tag-Filter-Operator.</span><span class="sxs-lookup"><span data-stu-id="35d02-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="35d02-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="35d02-116">-Location</span></span>
<span data-ttu-id="35d02-117">Liste der Speicherorte für Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="35d02-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="35d02-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d02-118">-ResourceGroupName</span></span>
<span data-ttu-id="35d02-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="35d02-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35d02-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="35d02-120">-Scope</span></span>
<span data-ttu-id="35d02-121">Ressourcen-IDs für Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="35d02-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="35d02-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="35d02-122">-Tag</span></span>
<span data-ttu-id="35d02-123">-Tag für Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="35d02-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="35d02-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d02-124">CommonParameters</span></span>
<span data-ttu-id="35d02-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d02-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="35d02-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d02-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d02-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35d02-127">INPUTS</span></span>

### <span data-ttu-id="35d02-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="35d02-128">System.String[]</span></span>

### <span data-ttu-id="35d02-129">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="35d02-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="35d02-130">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. TagOperators</span><span class="sxs-lookup"><span data-stu-id="35d02-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="35d02-131">System. String</span><span class="sxs-lookup"><span data-stu-id="35d02-131">System.String</span></span>

## <span data-ttu-id="35d02-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35d02-132">OUTPUTS</span></span>

### <span data-ttu-id="35d02-133">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="35d02-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="35d02-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="35d02-134">NOTES</span></span>

## <span data-ttu-id="35d02-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35d02-135">RELATED LINKS</span></span>
