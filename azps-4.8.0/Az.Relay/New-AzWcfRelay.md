---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 8fa9f3e2bbded846569609d9b1bae191d9f5ad89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165014"
---
# <span data-ttu-id="ef046-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="ef046-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="ef046-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef046-102">SYNOPSIS</span></span>
<span data-ttu-id="ef046-103">Erstellt eine WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ef046-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="ef046-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef046-104">SYNTAX</span></span>

### <span data-ttu-id="ef046-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef046-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef046-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ef046-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef046-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef046-107">DESCRIPTION</span></span>
<span data-ttu-id="ef046-108">Das New-AzWcfRelay-Cmdlet erstellt eine WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ef046-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="ef046-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef046-109">EXAMPLES</span></span>

### <span data-ttu-id="ef046-110">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="ef046-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

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

<span data-ttu-id="ef046-111">Erstellt eine neue WcfRelay \` \` -TestWCFRelay2 im angegebenen Relay \` -Namespace TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="ef046-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="ef046-112">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef046-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

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

<span data-ttu-id="ef046-113">Erstellt eine neue WcfRelay \` \` -TestWCFRelay im angegebenen Relay \` -Namespace TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="ef046-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="ef046-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef046-114">PARAMETERS</span></span>

### <span data-ttu-id="ef046-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef046-115">-DefaultProfile</span></span>
<span data-ttu-id="ef046-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef046-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef046-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ef046-117">-InputObject</span></span>
<span data-ttu-id="ef046-118">WcfRelay-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ef046-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="ef046-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ef046-119">-Name</span></span>
<span data-ttu-id="ef046-120">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="ef046-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="ef046-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ef046-121">-Namespace</span></span>
<span data-ttu-id="ef046-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="ef046-122">Namespace Name.</span></span>

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

### <span data-ttu-id="ef046-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="ef046-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="ef046-124">true, wenn die Clientautorisierung für dieses Relay erforderlich ist, andernfalls false. andernfalls false</span><span class="sxs-lookup"><span data-stu-id="ef046-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="ef046-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="ef046-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="ef046-126">true, wenn Transportsicherheit für dieses Relay erforderlich ist, andernfalls false. andernfalls false</span><span class="sxs-lookup"><span data-stu-id="ef046-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="ef046-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef046-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef046-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef046-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef046-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="ef046-129">-UserMetadata</span></span>
<span data-ttu-id="ef046-130">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ef046-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="ef046-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="ef046-131">-WcfRelayType</span></span>
<span data-ttu-id="ef046-132">WcfRelay-Typ.</span><span class="sxs-lookup"><span data-stu-id="ef046-132">WcfRelay Type.</span></span>
<span data-ttu-id="ef046-133">Mögliche Werte sind: "NetTcp" oder "http"</span><span class="sxs-lookup"><span data-stu-id="ef046-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="ef046-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef046-134">-Confirm</span></span>
<span data-ttu-id="ef046-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef046-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef046-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef046-136">-WhatIf</span></span>
<span data-ttu-id="ef046-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef046-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef046-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef046-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef046-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef046-139">CommonParameters</span></span>
<span data-ttu-id="ef046-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef046-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef046-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef046-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef046-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef046-142">INPUTS</span></span>

### <span data-ttu-id="ef046-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ef046-143">System.String</span></span>

### <span data-ttu-id="ef046-144">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="ef046-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="ef046-145">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef046-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ef046-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef046-146">OUTPUTS</span></span>

### <span data-ttu-id="ef046-147">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="ef046-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="ef046-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef046-148">NOTES</span></span>

## <span data-ttu-id="ef046-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef046-149">RELATED LINKS</span></span>
