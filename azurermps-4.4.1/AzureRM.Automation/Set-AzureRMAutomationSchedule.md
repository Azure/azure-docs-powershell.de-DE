---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: 03763ad7c2212eb89650749eb6d407d9ce973693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479978"
---
# <span data-ttu-id="5986f-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5986f-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="5986f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5986f-102">SYNOPSIS</span></span>
<span data-ttu-id="5986f-103">Ändert einen Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="5986f-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5986f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5986f-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5986f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5986f-105">DESCRIPTION</span></span>
<span data-ttu-id="5986f-106">Das Cmdlet " **festlegen-AzureRmAutomationSchedule** " ändert einen Zeitplan in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="5986f-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="5986f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5986f-107">EXAMPLES</span></span>

### <span data-ttu-id="5986f-108">Beispiel 1: Ändern eines Zeitplans</span><span class="sxs-lookup"><span data-stu-id="5986f-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5986f-109">Mit diesem Befehl wird die Beschreibung des Zeitplans mit dem Namen Schedule01 geändert.</span><span class="sxs-lookup"><span data-stu-id="5986f-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="5986f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5986f-110">PARAMETERS</span></span>

### <span data-ttu-id="5986f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5986f-111">-AutomationAccountName</span></span>
<span data-ttu-id="5986f-112">Gibt den Namen eines Automatisierungs Kontos an, für das mit diesem Cmdlet ein Zeitplan geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5986f-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="5986f-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5986f-113">-Description</span></span>
<span data-ttu-id="5986f-114">Gibt eine Beschreibung für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="5986f-114">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="5986f-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="5986f-115">-IsEnabled</span></span>
<span data-ttu-id="5986f-116">Gibt an, ob das Cmdlet den Terminplan aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5986f-116">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="5986f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5986f-117">-Name</span></span>
<span data-ttu-id="5986f-118">Gibt den Namen des Zeitplans an, der von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5986f-118">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5986f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5986f-119">-ResourceGroupName</span></span>
<span data-ttu-id="5986f-120">Gibt den Namen einer Ressourcengruppe an, für die mit diesem Cmdlet ein Zeitplan geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5986f-120">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="5986f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5986f-121">-DefaultProfile</span></span>
<span data-ttu-id="5986f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5986f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5986f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5986f-123">CommonParameters</span></span>
<span data-ttu-id="5986f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5986f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5986f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5986f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5986f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5986f-126">INPUTS</span></span>

## <span data-ttu-id="5986f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5986f-127">OUTPUTS</span></span>

### <span data-ttu-id="5986f-128">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="5986f-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="5986f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="5986f-129">NOTES</span></span>

## <span data-ttu-id="5986f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5986f-130">RELATED LINKS</span></span>

[<span data-ttu-id="5986f-131">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5986f-131">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="5986f-132">Neu – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5986f-132">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="5986f-133">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5986f-133">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


