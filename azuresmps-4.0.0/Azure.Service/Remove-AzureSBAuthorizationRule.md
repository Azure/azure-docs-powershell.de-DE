---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006337"
---
# <span data-ttu-id="9d237-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9d237-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="9d237-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d237-102">SYNOPSIS</span></span>
<span data-ttu-id="9d237-103">Entfernt vorhandene ServiceBus-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="9d237-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="9d237-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d237-104">SYNTAX</span></span>

### <span data-ttu-id="9d237-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="9d237-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d237-106">Namespaces</span><span class="sxs-lookup"><span data-stu-id="9d237-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d237-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d237-107">DESCRIPTION</span></span>
<span data-ttu-id="9d237-108">Entfernt vorhandene ServiceBus-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="9d237-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="9d237-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d237-109">EXAMPLES</span></span>

### <span data-ttu-id="9d237-110">Beispiel 1: Entfernen der Autorisierungsregel auf Namespaceebene</span><span class="sxs-lookup"><span data-stu-id="9d237-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="9d237-111">Entfernt die Autorisierungsregel myrule aus MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="9d237-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="9d237-112">Beispiel 2: Entfernen der Autorisierungsregel für eine Warteschlange</span><span class="sxs-lookup"><span data-stu-id="9d237-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="9d237-113">Entfernt die Autorisierungsregel namens myrule für eine myentity-Warteschlange in MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="9d237-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="9d237-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d237-114">PARAMETERS</span></span>

### <span data-ttu-id="9d237-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="9d237-115">-EntityName</span></span>
<span data-ttu-id="9d237-116">Der Entitätsname, auf den die Regel angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d237-116">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d237-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="9d237-117">-EntityType</span></span>
<span data-ttu-id="9d237-118">Der Entitätstyp (Queue, Topic, Relay, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="9d237-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d237-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9d237-119">-Name</span></span>
<span data-ttu-id="9d237-120">Der Name der eindeutigen Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="9d237-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="9d237-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9d237-121">-Namespace</span></span>
<span data-ttu-id="9d237-122">Der Namespacename, um die Autorisierungsregel anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="9d237-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="9d237-123">Wenn kein Entitätsname angegeben wird, befindet sich die Regel auf der Namespaceebene.</span><span class="sxs-lookup"><span data-stu-id="9d237-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="9d237-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d237-124">-PassThru</span></span>
<span data-ttu-id="9d237-125">Gibt an, dass dieses Cmdlet ein Objekt zurückgibt, das das Element darstellt, auf dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d237-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="9d237-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9d237-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9d237-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="9d237-127">-Profile</span></span>
<span data-ttu-id="9d237-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9d237-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d237-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9d237-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d237-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d237-130">CommonParameters</span></span>
<span data-ttu-id="9d237-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d237-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d237-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d237-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d237-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d237-133">INPUTS</span></span>

## <span data-ttu-id="9d237-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d237-134">OUTPUTS</span></span>

## <span data-ttu-id="9d237-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d237-135">NOTES</span></span>

## <span data-ttu-id="9d237-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d237-136">RELATED LINKS</span></span>

[<span data-ttu-id="9d237-137">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9d237-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="9d237-138">Neu – AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9d237-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="9d237-139">Satz-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9d237-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


