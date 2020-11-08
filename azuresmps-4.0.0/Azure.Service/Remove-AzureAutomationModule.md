---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006687"
---
# <span data-ttu-id="21569-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="21569-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="21569-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21569-102">SYNOPSIS</span></span>

<span data-ttu-id="21569-103">Entfernt ein Modul aus Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="21569-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="21569-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21569-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="21569-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21569-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="21569-106">Das Cmdlet **Remove-AzureAutomationModule** entfernt ein Automatisierungs Konto aus der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="21569-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="21569-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21569-107">EXAMPLES</span></span>

### <span data-ttu-id="21569-108">Beispiel 1: Entfernen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="21569-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="21569-109">Dieser Befehl entfernt ein Modul mit dem Namen ContosoModule aus dem Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="21569-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="21569-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="21569-110">PARAMETERS</span></span>

### <span data-ttu-id="21569-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="21569-111">-AutomationAccountName</span></span>
<span data-ttu-id="21569-112">Gibt den Namen des Automatisierungs Kontos mit dem Modul an.</span><span class="sxs-lookup"><span data-stu-id="21569-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="21569-113">-Force</span><span class="sxs-lookup"><span data-stu-id="21569-113">-Force</span></span>
<span data-ttu-id="21569-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="21569-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="21569-115">-Name</span><span class="sxs-lookup"><span data-stu-id="21569-115">-Name</span></span>
<span data-ttu-id="21569-116">Gibt den Namen des zu entfernenden Moduls an.</span><span class="sxs-lookup"><span data-stu-id="21569-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="21569-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="21569-117">-Profile</span></span>
<span data-ttu-id="21569-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="21569-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="21569-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="21569-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="21569-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21569-120">CommonParameters</span></span>
<span data-ttu-id="21569-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21569-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21569-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21569-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21569-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21569-123">INPUTS</span></span>

## <span data-ttu-id="21569-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21569-124">OUTPUTS</span></span>

## <span data-ttu-id="21569-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="21569-125">NOTES</span></span>

## <span data-ttu-id="21569-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21569-126">RELATED LINKS</span></span>

[<span data-ttu-id="21569-127">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="21569-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="21569-128">Neu – AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="21569-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="21569-129">Satz-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="21569-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


