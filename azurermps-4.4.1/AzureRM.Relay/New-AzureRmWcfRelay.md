---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: a7a8734395b08c906b84cc4465528434fcb31eb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663839"
---
# <span data-ttu-id="1e06a-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="1e06a-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="1e06a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e06a-102">SYNOPSIS</span></span>
<span data-ttu-id="1e06a-103">Erstellt eine WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1e06a-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e06a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e06a-104">SYNTAX</span></span>

### <span data-ttu-id="1e06a-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1e06a-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e06a-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1e06a-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e06a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e06a-107">DESCRIPTION</span></span>
<span data-ttu-id="1e06a-108">Das New-AzureRmWcfRelay-Cmdlet erstellt eine WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1e06a-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="1e06a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e06a-109">EXAMPLES</span></span>

### <span data-ttu-id="1e06a-110">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="1e06a-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

<span data-ttu-id="1e06a-111">Erstellt eine neue WcfRelay \` \` -TestWCFRelay2 im angegebenen Relay \` -Namespace TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="1e06a-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="1e06a-112">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e06a-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

<span data-ttu-id="1e06a-113">Erstellt eine neue WcfRelay \` \` -TestWCFRelay im angegebenen Relay \` -Namespace TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="1e06a-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="1e06a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e06a-114">PARAMETERS</span></span>

### <span data-ttu-id="1e06a-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="1e06a-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="1e06a-116">true, wenn die Clientautorisierung für dieses Relay erforderlich ist, andernfalls false. andernfalls false</span><span class="sxs-lookup"><span data-stu-id="1e06a-116">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-117">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="1e06a-117">-RequiresTransportSecurity</span></span>
<span data-ttu-id="1e06a-118">true, wenn Transportsicherheit für dieses Relay erforderlich ist, andernfalls false. andernfalls false</span><span class="sxs-lookup"><span data-stu-id="1e06a-118">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="1e06a-119">-UserMetadata</span></span>
<span data-ttu-id="1e06a-120">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1e06a-120">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="1e06a-121">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="1e06a-121">-WcfRelayType</span></span>
<span data-ttu-id="1e06a-122">WcfRelay-Typ.</span><span class="sxs-lookup"><span data-stu-id="1e06a-122">WcfRelay Type.</span></span>
<span data-ttu-id="1e06a-123">Mögliche Werte sind: "NetTcp" oder "http"</span><span class="sxs-lookup"><span data-stu-id="1e06a-123">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e06a-124">-Confirm</span></span>
<span data-ttu-id="1e06a-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e06a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e06a-126">-WhatIf</span></span>
<span data-ttu-id="1e06a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e06a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e06a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e06a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1e06a-129">-InputObject</span></span>
<span data-ttu-id="1e06a-130">WcfRelay-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1e06a-130">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1e06a-131">-Name</span></span>
<span data-ttu-id="1e06a-132">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="1e06a-132">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1e06a-133">-Namespace</span></span>
<span data-ttu-id="1e06a-134">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="1e06a-134">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e06a-135">-ResourceGroupName</span></span>
<span data-ttu-id="1e06a-136">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1e06a-136">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e06a-137">-DefaultProfile</span></span>
<span data-ttu-id="1e06a-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e06a-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e06a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e06a-139">CommonParameters</span></span>
<span data-ttu-id="1e06a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e06a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e06a-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e06a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e06a-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e06a-142">INPUTS</span></span>

### <span data-ttu-id="1e06a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e06a-143">-ResourceGroupName</span></span>
<span data-ttu-id="1e06a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1e06a-144">System.String</span></span>

### <span data-ttu-id="1e06a-145">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="1e06a-145">-NamespaceName</span></span>
<span data-ttu-id="1e06a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1e06a-146">System.String</span></span>

### <span data-ttu-id="1e06a-147">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="1e06a-147">-WcfRelayName</span></span>
<span data-ttu-id="1e06a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1e06a-148">System.String</span></span>

### <span data-ttu-id="1e06a-149">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1e06a-149">-InputObject</span></span>
<span data-ttu-id="1e06a-150">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="1e06a-150">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="1e06a-151">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="1e06a-151">-WcfRelayType</span></span>
<span data-ttu-id="1e06a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="1e06a-152">System.String</span></span>

### <span data-ttu-id="1e06a-153">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="1e06a-153">-RequiresClientAuthorization</span></span>
<span data-ttu-id="1e06a-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e06a-154">System.Boolean</span></span>

### <span data-ttu-id="1e06a-155">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="1e06a-155">-RequiresTransportSecurity</span></span>
<span data-ttu-id="1e06a-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e06a-156">System.Boolean</span></span>

### <span data-ttu-id="1e06a-157">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="1e06a-157">-UserMetadata</span></span>
<span data-ttu-id="1e06a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="1e06a-158">System.String</span></span>

## <span data-ttu-id="1e06a-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e06a-159">OUTPUTS</span></span>

### <span data-ttu-id="1e06a-160">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="1e06a-160">Example 1 - InputObject</span></span>

### <span data-ttu-id="1e06a-161">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="1e06a-161">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="1e06a-162">Relaytype: http-CreatedAt: 4/26/2017 5:14:46 Uhr UpdatedAt: 4/26/2017 5:14:46 pm ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false UserMetadata: TestWCFRelay2 ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-Storage-WestUS/Providers/Microsoft.rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2: TestWCFRelay2 Typ: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="1e06a-162">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:14:46 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : TestWCFRelay2 Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="1e06a-163">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e06a-163">Example 2 - Properties</span></span>

### <span data-ttu-id="1e06a-164">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="1e06a-164">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="1e06a-165">Relaytype: NetTcp CreatedAt: 4/26/2017 5:20:08 pm UpdatedAt: 4/26/2017 5:20:08 pm ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: User Meta Data ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-Storage-WestUS/Providers/Microsoft.rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="1e06a-165">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:20:08 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="1e06a-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e06a-166">NOTES</span></span>

## <span data-ttu-id="1e06a-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e06a-167">RELATED LINKS</span></span>

