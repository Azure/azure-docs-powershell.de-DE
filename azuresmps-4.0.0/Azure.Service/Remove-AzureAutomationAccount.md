---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006701"
---
# <span data-ttu-id="aae8e-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aae8e-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="aae8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aae8e-102">SYNOPSIS</span></span>

<span data-ttu-id="aae8e-103">Entfernt ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="aae8e-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="aae8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aae8e-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aae8e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aae8e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="aae8e-106">Das Cmdlet **Remove-AzureAutomationAccount** entfernt ein Konto aus der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="aae8e-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="aae8e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aae8e-107">EXAMPLES</span></span>

### <span data-ttu-id="aae8e-108">Beispiel 1: Entfernen eines Automatisierungs Kontos</span><span class="sxs-lookup"><span data-stu-id="aae8e-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="aae8e-109">Mit diesem Befehl wird ein Automatisierungs Kontonamens MyAutomationAccount entfernt, ohne dass die Benutzerüberprüfung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="aae8e-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="aae8e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aae8e-110">PARAMETERS</span></span>

### <span data-ttu-id="aae8e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="aae8e-111">-Force</span></span>
<span data-ttu-id="aae8e-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="aae8e-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aae8e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="aae8e-113">-Name</span></span>
<span data-ttu-id="aae8e-114">Gibt den Namen des Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="aae8e-114">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae8e-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="aae8e-115">-Profile</span></span>
<span data-ttu-id="aae8e-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="aae8e-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aae8e-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="aae8e-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aae8e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae8e-118">CommonParameters</span></span>
<span data-ttu-id="aae8e-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae8e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae8e-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae8e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae8e-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aae8e-121">INPUTS</span></span>

## <span data-ttu-id="aae8e-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aae8e-122">OUTPUTS</span></span>

## <span data-ttu-id="aae8e-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="aae8e-123">NOTES</span></span>

## <span data-ttu-id="aae8e-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aae8e-124">RELATED LINKS</span></span>

[<span data-ttu-id="aae8e-125">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aae8e-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="aae8e-126">Neu – AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aae8e-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


