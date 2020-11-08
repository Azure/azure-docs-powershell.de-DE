---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006193"
---
# <span data-ttu-id="0768c-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0768c-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="0768c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0768c-102">SYNOPSIS</span></span>
<span data-ttu-id="0768c-103">Erstellt eine neue ServiceBus-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="0768c-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="0768c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0768c-104">SYNTAX</span></span>

### <span data-ttu-id="0768c-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="0768c-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0768c-106">Namespaces</span><span class="sxs-lookup"><span data-stu-id="0768c-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0768c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0768c-107">DESCRIPTION</span></span>
<span data-ttu-id="0768c-108">Das Cmdlet **New-AzureSBAuthorizationRule** erstellt eine ServiceBus-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="0768c-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="0768c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0768c-109">EXAMPLES</span></span>

### <span data-ttu-id="0768c-110">Beispiel 1: Erstellen einer Autorisierungsregel mit generiertem Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="0768c-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="0768c-111">Erstellt eine neue Autorisierungsregel auf Namespaceebene mit der Berechtigung "Senden".</span><span class="sxs-lookup"><span data-stu-id="0768c-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="0768c-112">Beispiel 2: erstellt eine Autorisierungsregel, indem der Primärschlüssel bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0768c-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="0768c-113">Erstellt eine neue Autorisierungsregel auf der myentity-Warteschlangenebene mit allen Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="0768c-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="0768c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0768c-114">PARAMETERS</span></span>

### <span data-ttu-id="0768c-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="0768c-115">-EntityName</span></span>
<span data-ttu-id="0768c-116">Gibt den Entitätsnamen an, auf den die Regel angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0768c-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0768c-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="0768c-117">-EntityType</span></span>
<span data-ttu-id="0768c-118">Gibt den Entitätstyp an.</span><span class="sxs-lookup"><span data-stu-id="0768c-118">Specifies the entity type.</span></span>
<span data-ttu-id="0768c-119">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="0768c-119">Valid values are:</span></span>
  
- <span data-ttu-id="0768c-120">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="0768c-120">Queue</span></span>
- <span data-ttu-id="0768c-121">Thema</span><span class="sxs-lookup"><span data-stu-id="0768c-121">Topic</span></span>
- <span data-ttu-id="0768c-122">Relay</span><span class="sxs-lookup"><span data-stu-id="0768c-122">Relay</span></span>
- <span data-ttu-id="0768c-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="0768c-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0768c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0768c-124">-Name</span></span>
<span data-ttu-id="0768c-125">Gibt den eindeutigen Autorisierungsregel Namen an.</span><span class="sxs-lookup"><span data-stu-id="0768c-125">Specifies the unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0768c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0768c-126">-Namespace</span></span>
<span data-ttu-id="0768c-127">Gibt den Namespacenamen an, um die Autorisierungsregel anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="0768c-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="0768c-128">Wenn kein *Entitätsname* angegeben wird, befindet sich die Regel auf der Namespaceebene.</span><span class="sxs-lookup"><span data-stu-id="0768c-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="0768c-129">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="0768c-129">-Permission</span></span>
<span data-ttu-id="0768c-130">Die Autorisierungsberechtigungen (senden, verwalten, Abhören).</span><span class="sxs-lookup"><span data-stu-id="0768c-130">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0768c-131">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="0768c-131">-PrimaryKey</span></span>
<span data-ttu-id="0768c-132">Gibt den Primärschlüssel für die freigegebene zugriffssignatur an.</span><span class="sxs-lookup"><span data-stu-id="0768c-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="0768c-133">Wird generiert, wenn Sie nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0768c-133">Will be generated if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0768c-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="0768c-134">-Profile</span></span>
<span data-ttu-id="0768c-135">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0768c-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0768c-136">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0768c-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0768c-137">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0768c-137">-SecondaryKey</span></span>
<span data-ttu-id="0768c-138">Gibt den sekundären Schlüssel für die freigegebene zugriffssignatur an.</span><span class="sxs-lookup"><span data-stu-id="0768c-138">Specifies the Shared Access Signature secondary key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0768c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0768c-139">CommonParameters</span></span>
<span data-ttu-id="0768c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0768c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0768c-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0768c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0768c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0768c-142">INPUTS</span></span>

## <span data-ttu-id="0768c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0768c-143">OUTPUTS</span></span>

## <span data-ttu-id="0768c-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="0768c-144">NOTES</span></span>

## <span data-ttu-id="0768c-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0768c-145">RELATED LINKS</span></span>

[<span data-ttu-id="0768c-146">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0768c-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="0768c-147">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0768c-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="0768c-148">Satz-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0768c-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


