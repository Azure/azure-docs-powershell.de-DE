---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006091"
---
# <span data-ttu-id="16dc2-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dc2-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="16dc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16dc2-102">SYNOPSIS</span></span>

<span data-ttu-id="16dc2-103">Veröffentlicht eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="16dc2-103">Publishes a runbook.</span></span>

## <span data-ttu-id="16dc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16dc2-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="16dc2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16dc2-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="16dc2-106">Das Cmdlet **Publish-AzureAutomationRunbook** veröffentlicht einen runbooks zur Verwendung in der Produktionsumgebung von Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="16dc2-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="16dc2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16dc2-107">EXAMPLES</span></span>

### <span data-ttu-id="16dc2-108">Beispiel 1: Veröffentlichen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="16dc2-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="16dc2-109">Dieser Befehl veröffentlicht die runbooks mit dem Namen Runbk01 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="16dc2-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="16dc2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="16dc2-110">PARAMETERS</span></span>

### <span data-ttu-id="16dc2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="16dc2-111">-AutomationAccountName</span></span>
<span data-ttu-id="16dc2-112">Gibt den Namen des Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="16dc2-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="16dc2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="16dc2-113">-Name</span></span>
<span data-ttu-id="16dc2-114">Gibt den Namen des runbooks an.</span><span class="sxs-lookup"><span data-stu-id="16dc2-114">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="16dc2-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="16dc2-115">-Profile</span></span>
<span data-ttu-id="16dc2-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="16dc2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16dc2-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="16dc2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="16dc2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dc2-118">CommonParameters</span></span>
<span data-ttu-id="16dc2-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16dc2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dc2-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16dc2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dc2-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16dc2-121">INPUTS</span></span>

## <span data-ttu-id="16dc2-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16dc2-122">OUTPUTS</span></span>

## <span data-ttu-id="16dc2-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="16dc2-123">NOTES</span></span>

## <span data-ttu-id="16dc2-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16dc2-124">RELATED LINKS</span></span>

[<span data-ttu-id="16dc2-125">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dc2-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="16dc2-126">Neu – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dc2-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="16dc2-127">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dc2-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="16dc2-128">Satz-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dc2-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="16dc2-129">Anfang-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dc2-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


