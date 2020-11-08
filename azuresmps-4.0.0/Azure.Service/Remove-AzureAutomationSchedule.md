---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006376"
---
# <span data-ttu-id="a887b-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a887b-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="a887b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a887b-102">SYNOPSIS</span></span>

<span data-ttu-id="a887b-103">Löscht einen Azure-Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="a887b-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="a887b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a887b-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a887b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a887b-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a887b-106">Das Cmdlet **Remove-AzureAutomationSchedule** löscht einen Zeitplan aus der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="a887b-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="a887b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a887b-107">EXAMPLES</span></span>

### <span data-ttu-id="a887b-108">Beispiel 1: Entfernen eines Zeitplans</span><span class="sxs-lookup"><span data-stu-id="a887b-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="a887b-109">Mit diesem Befehl wird der Zeitplan mit dem Namen MySchedule entfernt.</span><span class="sxs-lookup"><span data-stu-id="a887b-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="a887b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a887b-110">PARAMETERS</span></span>

### <span data-ttu-id="a887b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a887b-111">-AutomationAccountName</span></span>
<span data-ttu-id="a887b-112">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a887b-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="a887b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a887b-113">-Force</span></span>
<span data-ttu-id="a887b-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a887b-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a887b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a887b-115">-Name</span></span>
<span data-ttu-id="a887b-116">Gibt den Namen des zu entfernenden Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="a887b-116">Specifies the name of the schedule to remove.</span></span>

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

### <span data-ttu-id="a887b-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="a887b-117">-Profile</span></span>
<span data-ttu-id="a887b-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a887b-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a887b-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a887b-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a887b-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a887b-120">-Confirm</span></span>
<span data-ttu-id="a887b-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a887b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a887b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a887b-122">-WhatIf</span></span>
<span data-ttu-id="a887b-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a887b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a887b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a887b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a887b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a887b-125">CommonParameters</span></span>
<span data-ttu-id="a887b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a887b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a887b-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a887b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a887b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a887b-128">INPUTS</span></span>

## <span data-ttu-id="a887b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a887b-129">OUTPUTS</span></span>

## <span data-ttu-id="a887b-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a887b-130">NOTES</span></span>

## <span data-ttu-id="a887b-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a887b-131">RELATED LINKS</span></span>

[<span data-ttu-id="a887b-132">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a887b-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="a887b-133">Neu – AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a887b-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="a887b-134">Satz-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a887b-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


