---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168401"
---
# <span data-ttu-id="7d304-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7d304-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="7d304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d304-102">SYNOPSIS</span></span>
<span data-ttu-id="7d304-103">Ruft einen Automatisierungszeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="7d304-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="7d304-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d304-104">SYNTAX</span></span>

### <span data-ttu-id="7d304-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d304-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d304-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7d304-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d304-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d304-107">DESCRIPTION</span></span>
<span data-ttu-id="7d304-108">Das **Cmdlet "Get-AzAutomationSchedule"** ruft einen Zeitplan für die Azure-Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="7d304-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="7d304-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d304-109">EXAMPLES</span></span>

### <span data-ttu-id="7d304-110">Beispiel 1: Einen Zeitplan erhalten</span><span class="sxs-lookup"><span data-stu-id="7d304-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7d304-111">Dieser Befehl ruft den Zeitplan namens "DailySchedule08" ab.</span><span class="sxs-lookup"><span data-stu-id="7d304-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="7d304-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d304-112">PARAMETERS</span></span>

### <span data-ttu-id="7d304-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7d304-113">-AutomationAccountName</span></span>
<span data-ttu-id="7d304-114">Gibt den Namen eines Automatisierungskontos an, für das dieses Cmdlet einen Zeitplan erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="7d304-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="7d304-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d304-115">-DefaultProfile</span></span>
<span data-ttu-id="7d304-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7d304-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d304-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7d304-117">-Name</span></span>
<span data-ttu-id="7d304-118">Gibt den Namen eines Zeitplans an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7d304-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d304-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d304-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d304-120">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Zeitplan erhält.</span><span class="sxs-lookup"><span data-stu-id="7d304-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="7d304-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d304-121">CommonParameters</span></span>
<span data-ttu-id="7d304-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d304-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d304-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d304-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d304-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d304-124">INPUTS</span></span>

### <span data-ttu-id="7d304-125">System.String</span><span class="sxs-lookup"><span data-stu-id="7d304-125">System.String</span></span>

## <span data-ttu-id="7d304-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d304-126">OUTPUTS</span></span>

### <span data-ttu-id="7d304-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="7d304-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="7d304-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7d304-128">NOTES</span></span>

## <span data-ttu-id="7d304-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7d304-129">RELATED LINKS</span></span>

[<span data-ttu-id="7d304-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7d304-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="7d304-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7d304-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="7d304-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7d304-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


