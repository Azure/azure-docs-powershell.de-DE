---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997370"
---
# <span data-ttu-id="ccbde-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ccbde-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="ccbde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccbde-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbde-103">Ruft einen Automatisierungs Zeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="ccbde-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="ccbde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccbde-104">SYNTAX</span></span>

### <span data-ttu-id="ccbde-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="ccbde-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccbde-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ccbde-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccbde-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccbde-107">DESCRIPTION</span></span>
<span data-ttu-id="ccbde-108">Das Cmdlet " **Get-AzAutomationSchedule** " erhält einen Azure-Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="ccbde-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="ccbde-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccbde-109">EXAMPLES</span></span>

### <span data-ttu-id="ccbde-110">Beispiel 1: Abrufen eines Zeitplans</span><span class="sxs-lookup"><span data-stu-id="ccbde-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ccbde-111">Dieser Befehl ruft den Zeitplan mit dem Namen DailySchedule08 ab.</span><span class="sxs-lookup"><span data-stu-id="ccbde-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="ccbde-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccbde-112">PARAMETERS</span></span>

### <span data-ttu-id="ccbde-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ccbde-113">-AutomationAccountName</span></span>
<span data-ttu-id="ccbde-114">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Zeitplan erhält.</span><span class="sxs-lookup"><span data-stu-id="ccbde-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="ccbde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbde-115">-DefaultProfile</span></span>
<span data-ttu-id="ccbde-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ccbde-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccbde-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ccbde-117">-Name</span></span>
<span data-ttu-id="ccbde-118">Gibt den Namen eines Zeitplans an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ccbde-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ccbde-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccbde-119">-ResourceGroupName</span></span>
<span data-ttu-id="ccbde-120">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Zeitplan erhält.</span><span class="sxs-lookup"><span data-stu-id="ccbde-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="ccbde-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbde-121">CommonParameters</span></span>
<span data-ttu-id="ccbde-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbde-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbde-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbde-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbde-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccbde-124">INPUTS</span></span>

### <span data-ttu-id="ccbde-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ccbde-125">System.String</span></span>

## <span data-ttu-id="ccbde-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccbde-126">OUTPUTS</span></span>

### <span data-ttu-id="ccbde-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="ccbde-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="ccbde-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccbde-128">NOTES</span></span>

## <span data-ttu-id="ccbde-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccbde-129">RELATED LINKS</span></span>

[<span data-ttu-id="ccbde-130">Neu – AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ccbde-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="ccbde-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ccbde-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="ccbde-132">Satz-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ccbde-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


