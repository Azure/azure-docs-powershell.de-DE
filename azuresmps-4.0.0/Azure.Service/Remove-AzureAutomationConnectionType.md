---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4370FF88-E34F-499D-AF57-53C15B4EB6E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: e55d9e54dcaa0f547d64ec58b2772a581a8ec30a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006690"
---
# <span data-ttu-id="00f81-101">Remove-AzureAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="00f81-101">Remove-AzureAutomationConnectionType</span></span>

## <span data-ttu-id="00f81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00f81-102">SYNOPSIS</span></span>

<span data-ttu-id="00f81-103">Entfernt einen Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="00f81-103">Removes a connection type.</span></span>

## <span data-ttu-id="00f81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00f81-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnectionType -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00f81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00f81-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="00f81-106">Mit dem Cmdlet **Remove-AzureAutomationConnectionType** wird ein Azure Automation-Verbindungstyp entfernt.</span><span class="sxs-lookup"><span data-stu-id="00f81-106">The **Remove-AzureAutomationConnectionType** cmdlet removes an Azure Automation connection type.</span></span>

## <span data-ttu-id="00f81-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00f81-107">EXAMPLES</span></span>

## <span data-ttu-id="00f81-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="00f81-108">PARAMETERS</span></span>

### <span data-ttu-id="00f81-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00f81-109">-AutomationAccountName</span></span>
<span data-ttu-id="00f81-110">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="00f81-110">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="00f81-111">-Force</span><span class="sxs-lookup"><span data-stu-id="00f81-111">-Force</span></span>
<span data-ttu-id="00f81-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="00f81-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00f81-113">-Name</span><span class="sxs-lookup"><span data-stu-id="00f81-113">-Name</span></span>
<span data-ttu-id="00f81-114">Gibt den Namen des zu entfernenden Verbindungstyps an.</span><span class="sxs-lookup"><span data-stu-id="00f81-114">Specifies the name of the connection type to remove.</span></span>

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

### <span data-ttu-id="00f81-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="00f81-115">-Profile</span></span>
<span data-ttu-id="00f81-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="00f81-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00f81-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="00f81-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00f81-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f81-118">CommonParameters</span></span>
<span data-ttu-id="00f81-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f81-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f81-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f81-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f81-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00f81-121">INPUTS</span></span>

## <span data-ttu-id="00f81-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00f81-122">OUTPUTS</span></span>

## <span data-ttu-id="00f81-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="00f81-123">NOTES</span></span>

## <span data-ttu-id="00f81-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00f81-124">RELATED LINKS</span></span>

