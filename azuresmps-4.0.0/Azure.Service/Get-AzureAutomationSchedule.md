---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005861"
---
# <span data-ttu-id="49646-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="49646-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="49646-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49646-102">SYNOPSIS</span></span>

<span data-ttu-id="49646-103">Ruft einen Azure-Automatisierungs Zeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="49646-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="49646-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49646-104">SYNTAX</span></span>

### <span data-ttu-id="49646-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="49646-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49646-106">ByName</span><span class="sxs-lookup"><span data-stu-id="49646-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="49646-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49646-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="49646-108">Das Cmdlet " **Get-AzureAutomationSchedule** " erhält einen Microsoft Azure-Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="49646-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="49646-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49646-109">EXAMPLES</span></span>

### <span data-ttu-id="49646-110">Beispiel 1: Abrufen eines Zeitplans</span><span class="sxs-lookup"><span data-stu-id="49646-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="49646-111">Dieser Befehl ruft den Zeitplan mit dem Namen DailySchedule08 ab.</span><span class="sxs-lookup"><span data-stu-id="49646-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="49646-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="49646-112">PARAMETERS</span></span>

### <span data-ttu-id="49646-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="49646-113">-AutomationAccountName</span></span>
<span data-ttu-id="49646-114">Gibt den Namen eines Azure Automation-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="49646-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="49646-115">-Name</span><span class="sxs-lookup"><span data-stu-id="49646-115">-Name</span></span>
<span data-ttu-id="49646-116">Gibt den Namen eines Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="49646-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49646-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="49646-117">-Profile</span></span>
<span data-ttu-id="49646-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="49646-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49646-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="49646-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49646-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49646-120">CommonParameters</span></span>
<span data-ttu-id="49646-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49646-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49646-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49646-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49646-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49646-123">INPUTS</span></span>

## <span data-ttu-id="49646-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49646-124">OUTPUTS</span></span>

### <span data-ttu-id="49646-125">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="49646-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="49646-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="49646-126">NOTES</span></span>

## <span data-ttu-id="49646-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49646-127">RELATED LINKS</span></span>

[<span data-ttu-id="49646-128">Neu – AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="49646-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="49646-129">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="49646-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="49646-130">Satz-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="49646-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


