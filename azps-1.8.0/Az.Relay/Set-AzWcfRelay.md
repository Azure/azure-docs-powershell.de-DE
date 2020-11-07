---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 04925f904861eea006c6480dbdb48794afc55c56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659691"
---
# <span data-ttu-id="262e5-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="262e5-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="262e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="262e5-102">SYNOPSIS</span></span>
<span data-ttu-id="262e5-103">Aktualisiert die Beschreibung einer WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="262e5-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="262e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="262e5-104">SYNTAX</span></span>

### <span data-ttu-id="262e5-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="262e5-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="262e5-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="262e5-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="262e5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="262e5-107">DESCRIPTION</span></span>
<span data-ttu-id="262e5-108">Das Set-AzWcfRelay-Cmdlet aktualisiert die Beschreibung für das WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="262e5-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="262e5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="262e5-109">EXAMPLES</span></span>

### <span data-ttu-id="262e5-110">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="262e5-110">Example 1 - InputObject</span></span>
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

### <span data-ttu-id="262e5-111">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="262e5-111">Example 2 - Properties</span></span>
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

<span data-ttu-id="262e5-112">Aktualisiert den angegebenen WcfRelay mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="262e5-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="262e5-113">In diesem Beispiel wird die UserMetadata-Eigenschaft mit neuem Wert aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="262e5-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="262e5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="262e5-114">PARAMETERS</span></span>

### <span data-ttu-id="262e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262e5-115">-DefaultProfile</span></span>
<span data-ttu-id="262e5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="262e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="262e5-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="262e5-117">-InputObject</span></span>
<span data-ttu-id="262e5-118">WcfRelay-Objekt.</span><span class="sxs-lookup"><span data-stu-id="262e5-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="262e5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="262e5-119">-Name</span></span>
<span data-ttu-id="262e5-120">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="262e5-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="262e5-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="262e5-121">-Namespace</span></span>
<span data-ttu-id="262e5-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="262e5-122">Namespace Name.</span></span>

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

### <span data-ttu-id="262e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="262e5-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="262e5-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="262e5-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="262e5-125">-UserMetadata</span></span>
<span data-ttu-id="262e5-126">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den WcfRelay-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="262e5-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="262e5-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="262e5-127">-Confirm</span></span>
<span data-ttu-id="262e5-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="262e5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="262e5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262e5-129">-WhatIf</span></span>
<span data-ttu-id="262e5-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="262e5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="262e5-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="262e5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="262e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262e5-132">CommonParameters</span></span>
<span data-ttu-id="262e5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262e5-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="262e5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262e5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="262e5-135">INPUTS</span></span>

### <span data-ttu-id="262e5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="262e5-136">System.String</span></span>

### <span data-ttu-id="262e5-137">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="262e5-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="262e5-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="262e5-138">OUTPUTS</span></span>

### <span data-ttu-id="262e5-139">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="262e5-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="262e5-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="262e5-140">NOTES</span></span>

## <span data-ttu-id="262e5-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="262e5-141">RELATED LINKS</span></span>
