---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: 3aa57c1ec70d560a0fee395b27d79372bdf4fd61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477722"
---
# <span data-ttu-id="10e15-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="10e15-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="10e15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10e15-102">SYNOPSIS</span></span>
<span data-ttu-id="10e15-103">Erstellt eine WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="10e15-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10e15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10e15-104">SYNTAX</span></span>

### <span data-ttu-id="10e15-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="10e15-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10e15-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="10e15-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-WcfRelayType <String>] [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>]
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10e15-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10e15-107">DESCRIPTION</span></span>
<span data-ttu-id="10e15-108">Das New-AzureRmWcfRelay-Cmdlet erstellt eine WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="10e15-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="10e15-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10e15-109">EXAMPLES</span></span>

### <span data-ttu-id="10e15-110">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="10e15-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="10e15-111">Erstellt eine neue WcfRelay \` \` -TestWCFRelay2 im angegebenen Relay \` -Namespace TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="10e15-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="10e15-112">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10e15-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
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

<span data-ttu-id="10e15-113">Erstellt eine neue WcfRelay \` \` -TestWCFRelay im angegebenen Relay \` -Namespace TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="10e15-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="10e15-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="10e15-114">PARAMETERS</span></span>

### <span data-ttu-id="10e15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e15-115">-DefaultProfile</span></span>
<span data-ttu-id="10e15-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10e15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10e15-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10e15-117">-InputObject</span></span>
<span data-ttu-id="10e15-118">WcfRelay-Objekt.</span><span class="sxs-lookup"><span data-stu-id="10e15-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="10e15-119">-Name</span><span class="sxs-lookup"><span data-stu-id="10e15-119">-Name</span></span>
<span data-ttu-id="10e15-120">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="10e15-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="10e15-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="10e15-121">-Namespace</span></span>
<span data-ttu-id="10e15-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="10e15-122">Namespace Name.</span></span>

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

### <span data-ttu-id="10e15-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="10e15-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="10e15-124">true, wenn die Clientautorisierung für dieses Relay erforderlich ist, andernfalls false. andernfalls false</span><span class="sxs-lookup"><span data-stu-id="10e15-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="10e15-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="10e15-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="10e15-126">true, wenn Transportsicherheit für dieses Relay erforderlich ist, andernfalls false. andernfalls false</span><span class="sxs-lookup"><span data-stu-id="10e15-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="10e15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e15-127">-ResourceGroupName</span></span>
<span data-ttu-id="10e15-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="10e15-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="10e15-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="10e15-129">-UserMetadata</span></span>
<span data-ttu-id="10e15-130">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="10e15-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="10e15-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="10e15-131">-WcfRelayType</span></span>
<span data-ttu-id="10e15-132">WcfRelay-Typ.</span><span class="sxs-lookup"><span data-stu-id="10e15-132">WcfRelay Type.</span></span>
<span data-ttu-id="10e15-133">Mögliche Werte sind: "NetTcp" oder "http"</span><span class="sxs-lookup"><span data-stu-id="10e15-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="10e15-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="10e15-134">-Confirm</span></span>
<span data-ttu-id="10e15-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="10e15-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e15-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e15-136">-WhatIf</span></span>
<span data-ttu-id="10e15-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10e15-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10e15-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="10e15-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10e15-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e15-139">CommonParameters</span></span>
<span data-ttu-id="10e15-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e15-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="10e15-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10e15-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e15-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10e15-142">INPUTS</span></span>

### <span data-ttu-id="10e15-143">System. String</span><span class="sxs-lookup"><span data-stu-id="10e15-143">System.String</span></span>
<span data-ttu-id="10e15-144">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="10e15-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="10e15-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10e15-145">OUTPUTS</span></span>

### <span data-ttu-id="10e15-146">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="10e15-146">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="10e15-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="10e15-147">NOTES</span></span>

## <span data-ttu-id="10e15-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10e15-148">RELATED LINKS</span></span>
