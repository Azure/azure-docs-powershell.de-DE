---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006377"
---
# <span data-ttu-id="7321a-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7321a-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="7321a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7321a-102">SYNOPSIS</span></span>

<span data-ttu-id="7321a-103">Entfernt eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="7321a-103">Removes a runbook.</span></span>

## <span data-ttu-id="7321a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7321a-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7321a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7321a-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7321a-106">Mit dem Cmdlet **Remove-AzureAutomationRunbook** wird ein runbooks aus Microsoft Azure Automation entfernt.</span><span class="sxs-lookup"><span data-stu-id="7321a-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="7321a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7321a-107">EXAMPLES</span></span>

### <span data-ttu-id="7321a-108">Beispiel 1: Entfernen eines runbooks</span><span class="sxs-lookup"><span data-stu-id="7321a-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="7321a-109">Dieser Befehl entfernt das runbooks mit dem Namen MyRunbook im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7321a-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7321a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7321a-110">PARAMETERS</span></span>

### <span data-ttu-id="7321a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7321a-111">-AutomationAccountName</span></span>
<span data-ttu-id="7321a-112">Gibt den Namen des Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="7321a-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="7321a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7321a-113">-Force</span></span>
<span data-ttu-id="7321a-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7321a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7321a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7321a-115">-Name</span></span>
<span data-ttu-id="7321a-116">Gibt den Namen des zu entfernenden runbooks an.</span><span class="sxs-lookup"><span data-stu-id="7321a-116">Specifies the name of the runbook to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7321a-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="7321a-117">-Profile</span></span>
<span data-ttu-id="7321a-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7321a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7321a-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7321a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7321a-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7321a-120">-Confirm</span></span>
<span data-ttu-id="7321a-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7321a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7321a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7321a-122">-WhatIf</span></span>
<span data-ttu-id="7321a-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7321a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7321a-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7321a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7321a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7321a-125">CommonParameters</span></span>
<span data-ttu-id="7321a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7321a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7321a-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7321a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7321a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7321a-128">INPUTS</span></span>

## <span data-ttu-id="7321a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7321a-129">OUTPUTS</span></span>

## <span data-ttu-id="7321a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="7321a-130">NOTES</span></span>

## <span data-ttu-id="7321a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7321a-131">RELATED LINKS</span></span>

[<span data-ttu-id="7321a-132">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7321a-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="7321a-133">Neu – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7321a-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="7321a-134">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7321a-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="7321a-135">Satz-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7321a-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="7321a-136">Anfang-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7321a-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


