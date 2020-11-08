---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006426"
---
# <span data-ttu-id="6d379-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6d379-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="6d379-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d379-102">SYNOPSIS</span></span>

<span data-ttu-id="6d379-103">Erstellt eine Verbindung in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="6d379-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="6d379-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d379-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6d379-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d379-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6d379-106">Das Cmdlet **New-AzureAutomationConnection** erstellt eine Verbindung in der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="6d379-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="6d379-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d379-107">EXAMPLES</span></span>

## <span data-ttu-id="6d379-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d379-108">PARAMETERS</span></span>

### <span data-ttu-id="6d379-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6d379-109">-AutomationAccountName</span></span>
<span data-ttu-id="6d379-110">Gibt den Namen des Automatisierungs Kontos an, in dem die Verbindung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d379-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

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

### <span data-ttu-id="6d379-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="6d379-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="6d379-112">Gibt eine Hashtabelle an, die Schlüssel-Wert-Paare enthält.</span><span class="sxs-lookup"><span data-stu-id="6d379-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="6d379-113">Die Schlüsselstellen die Verbindungsfelder des angegebenen Verbindungstyps dar.</span><span class="sxs-lookup"><span data-stu-id="6d379-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="6d379-114">Die Werte stellen die spezifischen Werte dar, die für jedes Verbindungsfeld für die Verbindungsinstanz gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d379-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d379-115">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="6d379-115">-ConnectionTypeName</span></span>
<span data-ttu-id="6d379-116">Gibt den Namen des Verbindungstyps an.</span><span class="sxs-lookup"><span data-stu-id="6d379-116">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="6d379-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d379-117">-Description</span></span>
<span data-ttu-id="6d379-118">Gibt eine Beschreibung für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="6d379-118">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d379-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6d379-119">-Name</span></span>
<span data-ttu-id="6d379-120">Gibt einen Namen für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="6d379-120">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="6d379-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6d379-121">-Profile</span></span>
<span data-ttu-id="6d379-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6d379-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6d379-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6d379-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6d379-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d379-124">CommonParameters</span></span>
<span data-ttu-id="6d379-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d379-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d379-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d379-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d379-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d379-127">INPUTS</span></span>

## <span data-ttu-id="6d379-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d379-128">OUTPUTS</span></span>

### <span data-ttu-id="6d379-129">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="6d379-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="6d379-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d379-130">NOTES</span></span>

## <span data-ttu-id="6d379-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d379-131">RELATED LINKS</span></span>

[<span data-ttu-id="6d379-132">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6d379-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="6d379-133">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6d379-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="6d379-134">Satz-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="6d379-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


