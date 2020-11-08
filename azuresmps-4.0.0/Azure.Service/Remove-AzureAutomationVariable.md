---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006375"
---
# <span data-ttu-id="51f6a-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="51f6a-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="51f6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51f6a-102">SYNOPSIS</span></span>

<span data-ttu-id="51f6a-103">Entfernt eine Automatisierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="51f6a-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="51f6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51f6a-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51f6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51f6a-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="51f6a-106">Das Cmdlet **Remove-AzureAutomationVariable** entfernt eine Variable aus der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="51f6a-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="51f6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51f6a-107">EXAMPLES</span></span>

### <span data-ttu-id="51f6a-108">Beispiel 1: Entfernen einer Variablen</span><span class="sxs-lookup"><span data-stu-id="51f6a-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="51f6a-109">Dieser Befehl entfernt eine Variable mit dem Namen MyStringVariable im Automatisierungs Konto mit dem Namen Contoso17, ohne die Benutzerüberprüfung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="51f6a-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="51f6a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="51f6a-110">PARAMETERS</span></span>

### <span data-ttu-id="51f6a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="51f6a-111">-AutomationAccountName</span></span>
<span data-ttu-id="51f6a-112">Gibt den Namen des Automatisierungs Kontos mit der Variablen an.</span><span class="sxs-lookup"><span data-stu-id="51f6a-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="51f6a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="51f6a-113">-Force</span></span>
<span data-ttu-id="51f6a-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="51f6a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51f6a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="51f6a-115">-Name</span></span>
<span data-ttu-id="51f6a-116">Gibt den Namen der Variablen an.</span><span class="sxs-lookup"><span data-stu-id="51f6a-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="51f6a-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="51f6a-117">-Profile</span></span>
<span data-ttu-id="51f6a-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="51f6a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51f6a-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="51f6a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51f6a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f6a-120">CommonParameters</span></span>
<span data-ttu-id="51f6a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f6a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f6a-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f6a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f6a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51f6a-123">INPUTS</span></span>

## <span data-ttu-id="51f6a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51f6a-124">OUTPUTS</span></span>

## <span data-ttu-id="51f6a-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="51f6a-125">NOTES</span></span>

## <span data-ttu-id="51f6a-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51f6a-126">RELATED LINKS</span></span>

[<span data-ttu-id="51f6a-127">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="51f6a-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="51f6a-128">Neu – AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="51f6a-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="51f6a-129">Satz-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="51f6a-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


