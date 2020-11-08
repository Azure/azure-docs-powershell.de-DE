---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006026"
---
# <span data-ttu-id="4633c-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4633c-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="4633c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4633c-102">SYNOPSIS</span></span>
<span data-ttu-id="4633c-103">Aktualisiert die vorhandene ServiceBus-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="4633c-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="4633c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4633c-104">SYNTAX</span></span>

### <span data-ttu-id="4633c-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="4633c-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4633c-106">Namespaces</span><span class="sxs-lookup"><span data-stu-id="4633c-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4633c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4633c-107">DESCRIPTION</span></span>
<span data-ttu-id="4633c-108">Aktualisiert die vorhandene ServiceBus-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="4633c-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="4633c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4633c-109">EXAMPLES</span></span>

### <span data-ttu-id="4633c-110">Beispiel 1: Erneuern des Primärschlüssels für die Autorisierungsregel auf Namespaceebene</span><span class="sxs-lookup"><span data-stu-id="4633c-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="4633c-111">Der Primärschlüssel wird erneuert.</span><span class="sxs-lookup"><span data-stu-id="4633c-111">The primary key is renewed.</span></span>

### <span data-ttu-id="4633c-112">Beispiel 2: Berechtigung zum Aktualisieren der Autorisierungsregel</span><span class="sxs-lookup"><span data-stu-id="4633c-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="4633c-113">Aktualisiert die Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="4633c-113">Updates the permissions.</span></span>

## <span data-ttu-id="4633c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4633c-114">PARAMETERS</span></span>

### <span data-ttu-id="4633c-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="4633c-115">-EntityName</span></span>
<span data-ttu-id="4633c-116">Der Entitätsname, auf den die Regel angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4633c-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="4633c-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="4633c-117">-EntityType</span></span>
<span data-ttu-id="4633c-118">Der Entitätstyp (Queue, Topic, Relay, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="4633c-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="4633c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4633c-119">-Name</span></span>
<span data-ttu-id="4633c-120">Der Name der eindeutigen Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="4633c-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="4633c-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4633c-121">-Namespace</span></span>
<span data-ttu-id="4633c-122">Der Namespacename, um die Autorisierungsregel anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="4633c-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="4633c-123">Wenn kein Entitätsname angegeben wird, befindet sich die Regel auf der Namespaceebene.</span><span class="sxs-lookup"><span data-stu-id="4633c-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="4633c-124">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="4633c-124">-Permission</span></span>
<span data-ttu-id="4633c-125">Die Autorisierungsberechtigungen (senden, verwalten, Abhören).</span><span class="sxs-lookup"><span data-stu-id="4633c-125">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="4633c-126">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="4633c-126">-PrimaryKey</span></span>
<span data-ttu-id="4633c-127">Der Primärschlüssel für die freigegebene zugriffssignatur.</span><span class="sxs-lookup"><span data-stu-id="4633c-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="4633c-128">Wird generiert, wenn Sie nicht bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4633c-128">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="4633c-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="4633c-129">-Profile</span></span>
<span data-ttu-id="4633c-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4633c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4633c-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4633c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4633c-132">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4633c-132">-SecondaryKey</span></span>
<span data-ttu-id="4633c-133">Der sekundäre Schlüssel für die freigegebene zugriffssignatur.</span><span class="sxs-lookup"><span data-stu-id="4633c-133">The Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="4633c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4633c-134">CommonParameters</span></span>
<span data-ttu-id="4633c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4633c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4633c-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4633c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4633c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4633c-137">INPUTS</span></span>

## <span data-ttu-id="4633c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4633c-138">OUTPUTS</span></span>

## <span data-ttu-id="4633c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="4633c-139">NOTES</span></span>

## <span data-ttu-id="4633c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4633c-140">RELATED LINKS</span></span>

[<span data-ttu-id="4633c-141">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4633c-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="4633c-142">Neu – AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4633c-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="4633c-143">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4633c-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


