---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006277"
---
# <span data-ttu-id="dcce0-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcce0-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="dcce0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dcce0-102">SYNOPSIS</span></span>

<span data-ttu-id="dcce0-103">Ändert einen Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="dcce0-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="dcce0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcce0-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dcce0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dcce0-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="dcce0-106">Das Cmdlet " **festlegen-AzureAutomationSchedule** " ändert einen Zeitplan in der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="dcce0-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="dcce0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dcce0-107">EXAMPLES</span></span>

### <span data-ttu-id="dcce0-108">Beispiel 1: Ändern eines Zeitplans</span><span class="sxs-lookup"><span data-stu-id="dcce0-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="dcce0-109">Mit diesem Befehl wird die Beschreibung des Zeitplans mit dem Namen Schedule01 geändert.</span><span class="sxs-lookup"><span data-stu-id="dcce0-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="dcce0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcce0-110">PARAMETERS</span></span>

### <span data-ttu-id="dcce0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dcce0-111">-AutomationAccountName</span></span>
<span data-ttu-id="dcce0-112">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="dcce0-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="dcce0-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dcce0-113">-Description</span></span>
<span data-ttu-id="dcce0-114">Gibt eine Beschreibung für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="dcce0-114">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcce0-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="dcce0-115">-IsEnabled</span></span>
<span data-ttu-id="dcce0-116">Gibt an, ob der Terminplan aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dcce0-116">Indicates whether the schedule is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcce0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dcce0-117">-Name</span></span>
<span data-ttu-id="dcce0-118">Gibt einen Namen für den Terminplan an.</span><span class="sxs-lookup"><span data-stu-id="dcce0-118">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="dcce0-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="dcce0-119">-Profile</span></span>
<span data-ttu-id="dcce0-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="dcce0-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dcce0-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="dcce0-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dcce0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcce0-122">CommonParameters</span></span>
<span data-ttu-id="dcce0-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcce0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcce0-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcce0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcce0-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dcce0-125">INPUTS</span></span>

## <span data-ttu-id="dcce0-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dcce0-126">OUTPUTS</span></span>

### <span data-ttu-id="dcce0-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="dcce0-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="dcce0-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="dcce0-128">NOTES</span></span>

## <span data-ttu-id="dcce0-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dcce0-129">RELATED LINKS</span></span>

[<span data-ttu-id="dcce0-130">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcce0-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="dcce0-131">Neu – AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcce0-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="dcce0-132">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcce0-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


