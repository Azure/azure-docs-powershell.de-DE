---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006633"
---
# <span data-ttu-id="54141-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="54141-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="54141-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54141-102">SYNOPSIS</span></span>

<span data-ttu-id="54141-103">Ändert den Wert eines Felds für eine Verbindung.</span><span class="sxs-lookup"><span data-stu-id="54141-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="54141-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54141-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="54141-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54141-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="54141-106">Das Cmdlet " **Satz-AzureAutomationConnectionFieldValue** " ändert den Wert für ein Feld für eine Verbindung in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="54141-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="54141-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54141-107">EXAMPLES</span></span>

## <span data-ttu-id="54141-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="54141-108">PARAMETERS</span></span>

### <span data-ttu-id="54141-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="54141-109">-AutomationAccountName</span></span>
<span data-ttu-id="54141-110">Gibt den Namen des Automatisierungs Kontos mit der Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="54141-110">Specifies the name of the Automation account with the connection.</span></span>

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

### <span data-ttu-id="54141-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="54141-111">-ConnectionFieldName</span></span>
<span data-ttu-id="54141-112">Gibt einen Namen für das Feld an.</span><span class="sxs-lookup"><span data-stu-id="54141-112">Specifies a name for the field.</span></span>

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

### <span data-ttu-id="54141-113">-Name</span><span class="sxs-lookup"><span data-stu-id="54141-113">-Name</span></span>
<span data-ttu-id="54141-114">Gibt einen Namen für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="54141-114">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="54141-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="54141-115">-Profile</span></span>
<span data-ttu-id="54141-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="54141-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54141-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="54141-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54141-118">-Wert</span><span class="sxs-lookup"><span data-stu-id="54141-118">-Value</span></span>
<span data-ttu-id="54141-119">Gibt einen Wert an, der im Connection-Feld gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="54141-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54141-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54141-120">CommonParameters</span></span>
<span data-ttu-id="54141-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54141-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54141-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54141-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54141-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54141-123">INPUTS</span></span>

## <span data-ttu-id="54141-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54141-124">OUTPUTS</span></span>

## <span data-ttu-id="54141-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="54141-125">NOTES</span></span>

## <span data-ttu-id="54141-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54141-126">RELATED LINKS</span></span>

[<span data-ttu-id="54141-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="54141-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="54141-128">Neu – AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="54141-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="54141-129">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="54141-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


