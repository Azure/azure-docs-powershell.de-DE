---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173108"
---
# <span data-ttu-id="a8f7b-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="a8f7b-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="a8f7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f7b-103">Erstellt eine HybridConnection im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="a8f7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8f7b-104">SYNTAX</span></span>

### <span data-ttu-id="a8f7b-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a8f7b-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8f7b-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a8f7b-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8f7b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8f7b-107">DESCRIPTION</span></span>
<span data-ttu-id="a8f7b-108">Das New-AzRelayHybridConnection-Cmdlet erstellt eine HybridConnection im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="a8f7b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8f7b-109">EXAMPLES</span></span>

### <span data-ttu-id="a8f7b-110">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="a8f7b-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="a8f7b-111">Erstellt eine neue HybirdConnection \` \` -TestHybirdConnection2 im angegebenen Relay \` -Namespace TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="a8f7b-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="a8f7b-112">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8f7b-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="a8f7b-113">Erstellt eine neue HybirdConnection \` \` -TestHybirdConnection1 im angegebenen Relay \` -Namespace TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="a8f7b-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="a8f7b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8f7b-114">PARAMETERS</span></span>

### <span data-ttu-id="a8f7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f7b-115">-DefaultProfile</span></span>
<span data-ttu-id="a8f7b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8f7b-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a8f7b-117">-InputObject</span></span>
<span data-ttu-id="a8f7b-118">HybridConnections-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f7b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a8f7b-119">-Name</span></span>
<span data-ttu-id="a8f7b-120">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f7b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a8f7b-121">-Namespace</span></span>
<span data-ttu-id="a8f7b-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-122">Namespace Name.</span></span>

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

### <span data-ttu-id="a8f7b-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="a8f7b-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="a8f7b-124">true, wenn die Clientautorisierung für diesen HybridConnections erforderlich ist, andernfalls false. andernfalls false</span><span class="sxs-lookup"><span data-stu-id="a8f7b-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f7b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f7b-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8f7b-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="a8f7b-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="a8f7b-127">-UserMetadata</span></span>
<span data-ttu-id="a8f7b-128">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f7b-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8f7b-129">-Confirm</span></span>
<span data-ttu-id="a8f7b-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8f7b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f7b-131">-WhatIf</span></span>
<span data-ttu-id="a8f7b-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8f7b-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8f7b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f7b-134">CommonParameters</span></span>
<span data-ttu-id="a8f7b-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8f7b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f7b-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8f7b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f7b-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8f7b-137">INPUTS</span></span>

### <span data-ttu-id="a8f7b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a8f7b-138">System.String</span></span>

### <span data-ttu-id="a8f7b-139">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="a8f7b-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="a8f7b-140">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a8f7b-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a8f7b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8f7b-141">OUTPUTS</span></span>

### <span data-ttu-id="a8f7b-142">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="a8f7b-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="a8f7b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8f7b-143">NOTES</span></span>

## <span data-ttu-id="a8f7b-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8f7b-144">RELATED LINKS</span></span>
