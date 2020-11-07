---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847351"
---
# <span data-ttu-id="2a15a-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2a15a-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="2a15a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a15a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a15a-103">Ändert einen Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="2a15a-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="2a15a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a15a-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a15a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a15a-105">DESCRIPTION</span></span>
<span data-ttu-id="2a15a-106">Das Cmdlet " **festlegen-AzAutomationSchedule** " ändert einen Zeitplan in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="2a15a-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="2a15a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a15a-107">EXAMPLES</span></span>

### <span data-ttu-id="2a15a-108">Beispiel 1: Ändern eines Zeitplans</span><span class="sxs-lookup"><span data-stu-id="2a15a-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2a15a-109">Mit diesem Befehl wird die Beschreibung des Zeitplans mit dem Namen Schedule01 geändert.</span><span class="sxs-lookup"><span data-stu-id="2a15a-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="2a15a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a15a-110">PARAMETERS</span></span>

### <span data-ttu-id="2a15a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2a15a-111">-AutomationAccountName</span></span>
<span data-ttu-id="2a15a-112">Gibt den Namen eines Automatisierungs Kontos an, für das mit diesem Cmdlet ein Zeitplan geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2a15a-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="2a15a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a15a-113">-DefaultProfile</span></span>
<span data-ttu-id="2a15a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2a15a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a15a-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a15a-115">-Description</span></span>
<span data-ttu-id="2a15a-116">Gibt eine Beschreibung für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="2a15a-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a15a-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="2a15a-117">-IsEnabled</span></span>
<span data-ttu-id="2a15a-118">Gibt an, ob das Cmdlet den Terminplan aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2a15a-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a15a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2a15a-119">-Name</span></span>
<span data-ttu-id="2a15a-120">Gibt den Namen des Zeitplans an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2a15a-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a15a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a15a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2a15a-122">Gibt den Namen einer Ressourcengruppe an, für die mit diesem Cmdlet ein Zeitplan geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2a15a-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="2a15a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a15a-123">CommonParameters</span></span>
<span data-ttu-id="2a15a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a15a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a15a-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a15a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a15a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a15a-126">INPUTS</span></span>

### <span data-ttu-id="2a15a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2a15a-127">System.String</span></span>

### <span data-ttu-id="2a15a-128">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2a15a-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2a15a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a15a-129">OUTPUTS</span></span>

### <span data-ttu-id="2a15a-130">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="2a15a-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="2a15a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a15a-131">NOTES</span></span>

## <span data-ttu-id="2a15a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a15a-132">RELATED LINKS</span></span>

[<span data-ttu-id="2a15a-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2a15a-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="2a15a-134">Neu – AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2a15a-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="2a15a-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2a15a-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


