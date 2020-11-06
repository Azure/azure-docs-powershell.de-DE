---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: 16df81633d4265b7b52dd2678bb58c80d4a756e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480978"
---
# <span data-ttu-id="84a49-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="84a49-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="84a49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84a49-102">SYNOPSIS</span></span>
<span data-ttu-id="84a49-103">Aktualisiert die Beschreibung einer WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="84a49-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84a49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84a49-104">SYNTAX</span></span>

### <span data-ttu-id="84a49-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="84a49-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84a49-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="84a49-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84a49-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84a49-107">DESCRIPTION</span></span>
<span data-ttu-id="84a49-108">Das Set-AzureRmWcfRelay-Cmdlet aktualisiert die Beschreibung für das WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="84a49-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="84a49-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84a49-109">EXAMPLES</span></span>

### <span data-ttu-id="84a49-110">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="84a49-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="84a49-111">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84a49-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="84a49-112">Aktualisiert den angegebenen WcfRelay mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="84a49-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="84a49-113">In diesem Beispiel wird die UserMetadata-Eigenschaft mit neuem Wert aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="84a49-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="84a49-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="84a49-114">PARAMETERS</span></span>

### <span data-ttu-id="84a49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a49-115">-DefaultProfile</span></span>
<span data-ttu-id="84a49-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84a49-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a49-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84a49-117">-InputObject</span></span>
<span data-ttu-id="84a49-118">WcfRelay-Objekt.</span><span class="sxs-lookup"><span data-stu-id="84a49-118">WcfRelay object.</span></span>

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a49-119">-Name</span><span class="sxs-lookup"><span data-stu-id="84a49-119">-Name</span></span>
<span data-ttu-id="84a49-120">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="84a49-120">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a49-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="84a49-121">-Namespace</span></span>
<span data-ttu-id="84a49-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="84a49-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a49-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a49-123">-ResourceGroupName</span></span>
<span data-ttu-id="84a49-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84a49-124">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a49-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="84a49-125">-UserMetadata</span></span>
<span data-ttu-id="84a49-126">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="84a49-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a49-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84a49-127">-Confirm</span></span>
<span data-ttu-id="84a49-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84a49-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a49-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a49-129">-WhatIf</span></span>
<span data-ttu-id="84a49-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84a49-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84a49-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84a49-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a49-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a49-132">CommonParameters</span></span>
<span data-ttu-id="84a49-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a49-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a49-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84a49-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a49-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84a49-135">INPUTS</span></span>

### <span data-ttu-id="84a49-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a49-136">-ResourceGroupName</span></span>
<span data-ttu-id="84a49-137">System. String</span><span class="sxs-lookup"><span data-stu-id="84a49-137">System.String</span></span>

### <span data-ttu-id="84a49-138">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="84a49-138">-NamespaceName</span></span>
<span data-ttu-id="84a49-139">System. String</span><span class="sxs-lookup"><span data-stu-id="84a49-139">System.String</span></span>

### <span data-ttu-id="84a49-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="84a49-140">-WcfRelayName</span></span>
<span data-ttu-id="84a49-141">System. String</span><span class="sxs-lookup"><span data-stu-id="84a49-141">System.String</span></span>

### <span data-ttu-id="84a49-142">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84a49-142">-InputObject</span></span>
<span data-ttu-id="84a49-143">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="84a49-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="84a49-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="84a49-144">-WcfRelayType</span></span>
<span data-ttu-id="84a49-145">System. String</span><span class="sxs-lookup"><span data-stu-id="84a49-145">System.String</span></span>

### <span data-ttu-id="84a49-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="84a49-146">-UserMetadata</span></span>
<span data-ttu-id="84a49-147">System. String</span><span class="sxs-lookup"><span data-stu-id="84a49-147">System.String</span></span>

## <span data-ttu-id="84a49-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84a49-148">OUTPUTS</span></span>

### <span data-ttu-id="84a49-149">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="84a49-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="84a49-150">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="84a49-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="84a49-151">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="84a49-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="84a49-152">Relaytype: http CreatedAt: 4/26/2017 5:14:46 pm UpdatedAt: 4/26/2017 5:16:50 pm ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false UserMetadata: UserMetadata ist ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt. beispielsweise Sie kann zum Speichern von DESC-riptive-Daten verwendet werden, wie beispielsweise die Liste der Teams und deren Kontaktinformationen, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="84a49-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="84a49-153">ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-Storage-WestUS/Providers/Microsoft.rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Typ: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="84a49-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="84a49-154">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84a49-154">Example 2 - Properties</span></span>

### <span data-ttu-id="84a49-155">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="84a49-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="84a49-156">Relaytype: NetTcp CreatedAt: 4/26/2017 5:20:08 pm UpdatedAt: 4/26/2017 5:26:09 pm ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: User Meta Data ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-Storage-WestUS/Providers/Microsoft.rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="84a49-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="84a49-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="84a49-157">NOTES</span></span>

## <span data-ttu-id="84a49-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84a49-158">RELATED LINKS</span></span>

