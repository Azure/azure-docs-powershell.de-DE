---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005820"
---
# <span data-ttu-id="d32de-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d32de-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="d32de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d32de-102">SYNOPSIS</span></span>
<span data-ttu-id="d32de-103">Ruft Service Bus-Autorisierungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="d32de-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="d32de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d32de-104">SYNTAX</span></span>

### <span data-ttu-id="d32de-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="d32de-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d32de-106">Namespaces</span><span class="sxs-lookup"><span data-stu-id="d32de-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d32de-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d32de-107">DESCRIPTION</span></span>
<span data-ttu-id="d32de-108">Ruft Service Bus-Autorisierungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="d32de-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="d32de-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d32de-109">EXAMPLES</span></span>

### <span data-ttu-id="d32de-110">Beispiel 1: Abrufen der Autorisierungsregel auf Namespaceebene</span><span class="sxs-lookup"><span data-stu-id="d32de-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="d32de-111">Ruft alle verfügbaren Autorisierungsregeln für MyNamespace ab.</span><span class="sxs-lookup"><span data-stu-id="d32de-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="d32de-112">Beispiel 2: Abrufen der Autorisierungsregel für eine Warteschlange</span><span class="sxs-lookup"><span data-stu-id="d32de-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="d32de-113">Ruft alle verfügbaren Autorisierungsregeln einer myentity-Warteschlange für MyNamespace ab.</span><span class="sxs-lookup"><span data-stu-id="d32de-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="d32de-114">Beispiel 3: Abrufen der Autorisierungsregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="d32de-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="d32de-115">Ruft eine Autorisierungsregel namens myrule auf MyNamespace-Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="d32de-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="d32de-116">Beispiel 4: Abrufen der Autorisierungsregel nach Berechtigung</span><span class="sxs-lookup"><span data-stu-id="d32de-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="d32de-117">Ruft alle Autorisierungsregeln ab, die über die Berechtigung Senden auf Namespaceebene verfügen.</span><span class="sxs-lookup"><span data-stu-id="d32de-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="d32de-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d32de-118">PARAMETERS</span></span>

### <span data-ttu-id="d32de-119">-EntityName</span><span class="sxs-lookup"><span data-stu-id="d32de-119">-EntityName</span></span>
<span data-ttu-id="d32de-120">Der Entitätsname, auf den die Regel angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d32de-120">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="d32de-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="d32de-121">-EntityType</span></span>
<span data-ttu-id="d32de-122">Der Entitätstyp (Queue, Topic, Relay, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="d32de-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="d32de-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d32de-123">-Name</span></span>
<span data-ttu-id="d32de-124">Der Name der eindeutigen Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="d32de-124">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="d32de-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d32de-125">-Namespace</span></span>
<span data-ttu-id="d32de-126">Der Namespacename, um die Autorisierungsregel anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="d32de-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="d32de-127">Wenn kein Entitätsname angegeben wird, befindet sich die Regel auf der Namespaceebene.</span><span class="sxs-lookup"><span data-stu-id="d32de-127">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="d32de-128">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="d32de-128">-Permission</span></span>
<span data-ttu-id="d32de-129">Die Autorisierungsberechtigungen zum Filtern (senden, verwalten, Abhören).</span><span class="sxs-lookup"><span data-stu-id="d32de-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="d32de-130">Dies verwendet exakte Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="d32de-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d32de-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="d32de-131">-Profile</span></span>
<span data-ttu-id="d32de-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d32de-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d32de-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d32de-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d32de-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32de-134">CommonParameters</span></span>
<span data-ttu-id="d32de-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d32de-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32de-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d32de-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32de-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d32de-137">INPUTS</span></span>

## <span data-ttu-id="d32de-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d32de-138">OUTPUTS</span></span>

## <span data-ttu-id="d32de-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d32de-139">NOTES</span></span>

## <span data-ttu-id="d32de-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d32de-140">RELATED LINKS</span></span>

[<span data-ttu-id="d32de-141">Neu – AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d32de-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d32de-142">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d32de-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d32de-143">Satz-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d32de-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


