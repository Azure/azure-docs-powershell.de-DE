---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368065"
---
# <span data-ttu-id="67f15-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="67f15-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="67f15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67f15-102">SYNOPSIS</span></span>
<span data-ttu-id="67f15-103">Erstellt eine HybridVerbindung im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="67f15-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="67f15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67f15-104">SYNTAX</span></span>

### <span data-ttu-id="67f15-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67f15-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67f15-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="67f15-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67f15-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67f15-107">DESCRIPTION</span></span>
<span data-ttu-id="67f15-108">Das New-AzRelayHybridConnection erstellt eine HybridVerbindung im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="67f15-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="67f15-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67f15-109">EXAMPLES</span></span>

### <span data-ttu-id="67f15-110">Beispiel 1 : InputObject</span><span class="sxs-lookup"><span data-stu-id="67f15-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="67f15-111">Erstellt einen neuen HybirdConnection \` TestHybirdConnection2 im angegebenen \` \` Relay-Namespace TestNameSpace-HybirdConnection. \`</span><span class="sxs-lookup"><span data-stu-id="67f15-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="67f15-112">Beispiel 2: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67f15-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="67f15-113">Erstellt einen neuen HybirdConnection \` TestHybirdConnection1 im angegebenen \` \` Relay-Namespace TestNameSpace-HybirdConnection. \`</span><span class="sxs-lookup"><span data-stu-id="67f15-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="67f15-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67f15-114">PARAMETERS</span></span>

### <span data-ttu-id="67f15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f15-115">-DefaultProfile</span></span>
<span data-ttu-id="67f15-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67f15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67f15-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67f15-117">-InputObject</span></span>
<span data-ttu-id="67f15-118">HybridConnections-Objekt.</span><span class="sxs-lookup"><span data-stu-id="67f15-118">HybridConnections object.</span></span>

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

### <span data-ttu-id="67f15-119">-Name</span><span class="sxs-lookup"><span data-stu-id="67f15-119">-Name</span></span>
<span data-ttu-id="67f15-120">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="67f15-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="67f15-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="67f15-121">-Namespace</span></span>
<span data-ttu-id="67f15-122">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="67f15-122">Namespace Name.</span></span>

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

### <span data-ttu-id="67f15-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="67f15-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="67f15-124">true, wenn für dieses HybridConnections eine Clientautorisierung erforderlich ist; andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="67f15-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="67f15-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f15-125">-ResourceGroupName</span></span>
<span data-ttu-id="67f15-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="67f15-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="67f15-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="67f15-127">-UserMetadata</span></span>
<span data-ttu-id="67f15-128">Ruft Benutzermetadaten als Platzhalter ab oder legt diese als Platzhalter fest, um benutzerdefinierte Zeichenfolgendaten für den HybridConnection-Endpunkt zu speichern. sie kann zum Speichern von beschreibenden Daten verwendet werden, z. B. eine Liste der Teams und deren Kontaktinformationen, und es können auch benutzerdefinierte Konfigurationseinstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="67f15-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="67f15-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67f15-129">-Confirm</span></span>
<span data-ttu-id="67f15-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67f15-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67f15-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="67f15-131">-WhatIf</span></span>
<span data-ttu-id="67f15-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67f15-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67f15-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67f15-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67f15-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f15-134">CommonParameters</span></span>
<span data-ttu-id="67f15-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f15-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f15-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f15-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f15-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67f15-137">INPUTS</span></span>

### <span data-ttu-id="67f15-138">System.String</span><span class="sxs-lookup"><span data-stu-id="67f15-138">System.String</span></span>

### <span data-ttu-id="67f15-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="67f15-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="67f15-140">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="67f15-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="67f15-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67f15-141">OUTPUTS</span></span>

### <span data-ttu-id="67f15-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="67f15-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="67f15-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="67f15-143">NOTES</span></span>

## <span data-ttu-id="67f15-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="67f15-144">RELATED LINKS</span></span>
