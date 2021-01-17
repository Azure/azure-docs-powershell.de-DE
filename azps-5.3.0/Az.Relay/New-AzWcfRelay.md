---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 8fa9f3e2bbded846569609d9b1bae191d9f5ad89
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468616"
---
# <span data-ttu-id="20de1-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="20de1-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="20de1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20de1-102">SYNOPSIS</span></span>
<span data-ttu-id="20de1-103">Erstellt ein WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="20de1-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="20de1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20de1-104">SYNTAX</span></span>

### <span data-ttu-id="20de1-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="20de1-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20de1-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="20de1-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20de1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20de1-107">DESCRIPTION</span></span>
<span data-ttu-id="20de1-108">Das New-AzWcfRelay erstellt ein WcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="20de1-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="20de1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20de1-109">EXAMPLES</span></span>

### <span data-ttu-id="20de1-110">Beispiel 1 : InputObject</span><span class="sxs-lookup"><span data-stu-id="20de1-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="20de1-111">Erstellt einen neuen WcfRelay \` TestWCFRelay2 im angegebenen \` \` Relay-Namespace TestNameSpace-Relay. \`</span><span class="sxs-lookup"><span data-stu-id="20de1-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="20de1-112">Beispiel 2: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20de1-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="20de1-113">Erstellt eine neue WcfRelay \` TestWCFRelay im angegebenen \` \` Relay-Namespace TestNameSpace-Relay1. \`</span><span class="sxs-lookup"><span data-stu-id="20de1-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="20de1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20de1-114">PARAMETERS</span></span>

### <span data-ttu-id="20de1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20de1-115">-DefaultProfile</span></span>
<span data-ttu-id="20de1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20de1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20de1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20de1-117">-InputObject</span></span>
<span data-ttu-id="20de1-118">WcfRelay-Objekt.</span><span class="sxs-lookup"><span data-stu-id="20de1-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="20de1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="20de1-119">-Name</span></span>
<span data-ttu-id="20de1-120">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="20de1-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="20de1-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="20de1-121">-Namespace</span></span>
<span data-ttu-id="20de1-122">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="20de1-122">Namespace Name.</span></span>

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

### <span data-ttu-id="20de1-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="20de1-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="20de1-124">true, wenn für dieses Relay eine Clientautorisierung erforderlich ist; andernfalls "false"</span><span class="sxs-lookup"><span data-stu-id="20de1-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="20de1-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="20de1-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="20de1-126">true, wenn Transportsicherheit für dieses Relay erforderlich ist; andernfalls "false"</span><span class="sxs-lookup"><span data-stu-id="20de1-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="20de1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20de1-127">-ResourceGroupName</span></span>
<span data-ttu-id="20de1-128">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="20de1-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="20de1-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="20de1-129">-UserMetadata</span></span>
<span data-ttu-id="20de1-130">Ruft Benutzermetadaten als Platzhalter ab oder legt diese als Platzhalter fest, um benutzerdefinierte Zeichenfolgendaten für den HybridConnection-Endpunkt zu speichern. sie kann zum Speichern von beschreibenden Daten verwendet werden, z. B. eine Liste der Teams und deren Kontaktinformationen, und es können auch benutzerdefinierte Konfigurationseinstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="20de1-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="20de1-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="20de1-131">-WcfRelayType</span></span>
<span data-ttu-id="20de1-132">WcfRelay-Typ.</span><span class="sxs-lookup"><span data-stu-id="20de1-132">WcfRelay Type.</span></span>
<span data-ttu-id="20de1-133">Mögliche Werte sind: "NetTcp" oder "Http".</span><span class="sxs-lookup"><span data-stu-id="20de1-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="20de1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20de1-134">-Confirm</span></span>
<span data-ttu-id="20de1-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20de1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20de1-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="20de1-136">-WhatIf</span></span>
<span data-ttu-id="20de1-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20de1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20de1-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20de1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20de1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20de1-139">CommonParameters</span></span>
<span data-ttu-id="20de1-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20de1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20de1-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20de1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20de1-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20de1-142">INPUTS</span></span>

### <span data-ttu-id="20de1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="20de1-143">System.String</span></span>

### <span data-ttu-id="20de1-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="20de1-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="20de1-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20de1-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="20de1-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20de1-146">OUTPUTS</span></span>

### <span data-ttu-id="20de1-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="20de1-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="20de1-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="20de1-148">NOTES</span></span>

## <span data-ttu-id="20de1-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="20de1-149">RELATED LINKS</span></span>
