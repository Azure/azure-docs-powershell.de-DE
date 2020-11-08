---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: f7671d35901705ef96f6c1bf13c487c688a6214c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165706"
---
# <span data-ttu-id="6a8d8-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="6a8d8-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="6a8d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a8d8-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8d8-103">Aktualisiert die Beschreibung einer WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="6a8d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a8d8-104">SYNTAX</span></span>

### <span data-ttu-id="6a8d8-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6a8d8-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a8d8-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="6a8d8-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a8d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a8d8-107">DESCRIPTION</span></span>
<span data-ttu-id="6a8d8-108">Das Set-AzWcfRelay-Cmdlet aktualisiert die Beschreibung für das WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="6a8d8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a8d8-109">EXAMPLES</span></span>

### <span data-ttu-id="6a8d8-110">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="6a8d8-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="6a8d8-111">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a8d8-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="6a8d8-112">Aktualisiert den angegebenen WcfRelay mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="6a8d8-113">In diesem Beispiel wird die UserMetadata-Eigenschaft mit neuem Wert aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="6a8d8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a8d8-114">PARAMETERS</span></span>

### <span data-ttu-id="6a8d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8d8-115">-DefaultProfile</span></span>
<span data-ttu-id="6a8d8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8d8-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6a8d8-117">-InputObject</span></span>
<span data-ttu-id="6a8d8-118">WcfRelay-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8d8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6a8d8-119">-Name</span></span>
<span data-ttu-id="6a8d8-120">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-120">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8d8-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6a8d8-121">-Namespace</span></span>
<span data-ttu-id="6a8d8-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-122">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a8d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="6a8d8-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8d8-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="6a8d8-125">-UserMetadata</span></span>
<span data-ttu-id="6a8d8-126">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den WcfRelay-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8d8-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6a8d8-127">-Confirm</span></span>
<span data-ttu-id="6a8d8-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a8d8-129">-WhatIf</span></span>
<span data-ttu-id="6a8d8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a8d8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8d8-132">CommonParameters</span></span>
<span data-ttu-id="6a8d8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8d8-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a8d8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8d8-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a8d8-135">INPUTS</span></span>

### <span data-ttu-id="6a8d8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6a8d8-136">System.String</span></span>

### <span data-ttu-id="6a8d8-137">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="6a8d8-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="6a8d8-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a8d8-138">OUTPUTS</span></span>

### <span data-ttu-id="6a8d8-139">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="6a8d8-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="6a8d8-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a8d8-140">NOTES</span></span>

## <span data-ttu-id="6a8d8-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a8d8-141">RELATED LINKS</span></span>
