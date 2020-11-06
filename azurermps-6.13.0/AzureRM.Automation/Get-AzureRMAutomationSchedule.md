---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 78e34c5d3d94a964fbff6d0cbaa74c9dd3dd2177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501226"
---
# <span data-ttu-id="20867-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="20867-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="20867-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20867-102">SYNOPSIS</span></span>
<span data-ttu-id="20867-103">Ruft einen Automatisierungs Zeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="20867-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20867-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20867-104">SYNTAX</span></span>

### <span data-ttu-id="20867-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="20867-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20867-106">ByName</span><span class="sxs-lookup"><span data-stu-id="20867-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20867-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20867-107">DESCRIPTION</span></span>
<span data-ttu-id="20867-108">Das Cmdlet " **Get-AzureRmAutomationSchedule** " erhält einen Azure-Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="20867-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="20867-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20867-109">EXAMPLES</span></span>

### <span data-ttu-id="20867-110">Beispiel 1: Abrufen eines Zeitplans</span><span class="sxs-lookup"><span data-stu-id="20867-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="20867-111">Dieser Befehl ruft den Zeitplan mit dem Namen DailySchedule08 ab.</span><span class="sxs-lookup"><span data-stu-id="20867-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="20867-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="20867-112">PARAMETERS</span></span>

### <span data-ttu-id="20867-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20867-113">-AutomationAccountName</span></span>
<span data-ttu-id="20867-114">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Zeitplan erhält.</span><span class="sxs-lookup"><span data-stu-id="20867-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="20867-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20867-115">-DefaultProfile</span></span>
<span data-ttu-id="20867-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="20867-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20867-117">-Name</span><span class="sxs-lookup"><span data-stu-id="20867-117">-Name</span></span>
<span data-ttu-id="20867-118">Gibt den Namen eines Zeitplans an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="20867-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="20867-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20867-119">-ResourceGroupName</span></span>
<span data-ttu-id="20867-120">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Zeitplan erhält.</span><span class="sxs-lookup"><span data-stu-id="20867-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="20867-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20867-121">CommonParameters</span></span>
<span data-ttu-id="20867-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20867-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20867-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20867-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20867-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20867-124">INPUTS</span></span>

### <span data-ttu-id="20867-125">System. String</span><span class="sxs-lookup"><span data-stu-id="20867-125">System.String</span></span>

## <span data-ttu-id="20867-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20867-126">OUTPUTS</span></span>

### <span data-ttu-id="20867-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="20867-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="20867-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="20867-128">NOTES</span></span>

## <span data-ttu-id="20867-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20867-129">RELATED LINKS</span></span>

[<span data-ttu-id="20867-130">Neu – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="20867-130">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="20867-131">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="20867-131">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="20867-132">Satz-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="20867-132">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


