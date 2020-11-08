---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006686"
---
# <span data-ttu-id="c556a-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c556a-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="c556a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c556a-102">SYNOPSIS</span></span>

<span data-ttu-id="c556a-103">Entfernt eine Anmeldeinformationen aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="c556a-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="c556a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c556a-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c556a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c556a-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c556a-106">Mit dem Cmdlet **Remove-AzureAutomationCredential** werden Anmeldeinformationen aus Microsoft Azure Automation entfernt.</span><span class="sxs-lookup"><span data-stu-id="c556a-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="c556a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c556a-107">EXAMPLES</span></span>

### <span data-ttu-id="c556a-108">Beispiel 1: Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="c556a-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="c556a-109">Mit diesem Befehl werden die Anmeldeinformationen mit dem Namen myCredential im Automatisierungs Konto mit dem Namen Contoso17 entfernt.</span><span class="sxs-lookup"><span data-stu-id="c556a-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c556a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c556a-110">PARAMETERS</span></span>

### <span data-ttu-id="c556a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c556a-111">-AutomationAccountName</span></span>
<span data-ttu-id="c556a-112">Gibt den Namen des Automatisierungs Kontos mit den Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="c556a-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="c556a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c556a-113">-Force</span></span>
<span data-ttu-id="c556a-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c556a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c556a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c556a-115">-Name</span></span>
<span data-ttu-id="c556a-116">Gibt den Namen der zu entfernenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="c556a-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="c556a-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="c556a-117">-Profile</span></span>
<span data-ttu-id="c556a-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c556a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c556a-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c556a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c556a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c556a-120">CommonParameters</span></span>
<span data-ttu-id="c556a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c556a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c556a-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c556a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c556a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c556a-123">INPUTS</span></span>

## <span data-ttu-id="c556a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c556a-124">OUTPUTS</span></span>

## <span data-ttu-id="c556a-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="c556a-125">NOTES</span></span>

## <span data-ttu-id="c556a-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c556a-126">RELATED LINKS</span></span>

[<span data-ttu-id="c556a-127">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c556a-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="c556a-128">Neu – AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c556a-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="c556a-129">Satz-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c556a-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


