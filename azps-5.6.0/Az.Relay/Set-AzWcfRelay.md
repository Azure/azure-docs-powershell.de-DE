---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 85c8d65f8a690f9cc977ff069fe6972f5537a114
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943721"
---
# <span data-ttu-id="dfc7d-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="dfc7d-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="dfc7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfc7d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc7d-103">Aktualisiert die Beschreibung eines WcfRelays im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="dfc7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfc7d-104">SYNTAX</span></span>

### <span data-ttu-id="dfc7d-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dfc7d-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfc7d-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="dfc7d-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfc7d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfc7d-107">DESCRIPTION</span></span>
<span data-ttu-id="dfc7d-108">Das Set-AzWcfRelay cmdlet aktualisiert die Beschreibung für wcfRelay im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="dfc7d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dfc7d-109">EXAMPLES</span></span>

### <span data-ttu-id="dfc7d-110">Beispiel 1 – InputObject</span><span class="sxs-lookup"><span data-stu-id="dfc7d-110">Example 1 - InputObject</span></span>
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

### <span data-ttu-id="dfc7d-111">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dfc7d-111">Example 2 - Properties</span></span>
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

<span data-ttu-id="dfc7d-112">Aktualisiert das angegebene WcfRelay mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="dfc7d-113">In diesem Beispiel wird die UserMetadata-Eigenschaft mit einem neuen Wert aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="dfc7d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dfc7d-114">PARAMETERS</span></span>

### <span data-ttu-id="dfc7d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc7d-115">-DefaultProfile</span></span>
<span data-ttu-id="dfc7d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfc7d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfc7d-117">-InputObject</span></span>
<span data-ttu-id="dfc7d-118">WcfRelay-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="dfc7d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dfc7d-119">-Name</span></span>
<span data-ttu-id="dfc7d-120">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="dfc7d-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dfc7d-121">-Namespace</span></span>
<span data-ttu-id="dfc7d-122">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-122">Namespace Name.</span></span>

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

### <span data-ttu-id="dfc7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfc7d-123">-ResourceGroupName</span></span>
<span data-ttu-id="dfc7d-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="dfc7d-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="dfc7d-125">-UserMetadata</span></span>
<span data-ttu-id="dfc7d-126">Ruft benutzermetadata ab oder legt diese fest, um benutzerdefinierte Zeichenfolgendaten für den WcfRelay-Endpunkt zu speichern. sie kann zum Speichern beschreibender Daten verwendet werden, z. B. eine Liste von Teams, und deren Kontaktinformationen können auch benutzerdefinierte Konfigurationseinstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="dfc7d-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfc7d-127">-Confirm</span></span>
<span data-ttu-id="dfc7d-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfc7d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfc7d-129">-WhatIf</span></span>
<span data-ttu-id="dfc7d-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfc7d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfc7d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc7d-132">CommonParameters</span></span>
<span data-ttu-id="dfc7d-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc7d-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfc7d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc7d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dfc7d-135">INPUTS</span></span>

### <span data-ttu-id="dfc7d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="dfc7d-136">System.String</span></span>

### <span data-ttu-id="dfc7d-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="dfc7d-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="dfc7d-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dfc7d-138">OUTPUTS</span></span>

### <span data-ttu-id="dfc7d-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="dfc7d-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="dfc7d-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dfc7d-140">NOTES</span></span>

## <span data-ttu-id="dfc7d-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dfc7d-141">RELATED LINKS</span></span>
