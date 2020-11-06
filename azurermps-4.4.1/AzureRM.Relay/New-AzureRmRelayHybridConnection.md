---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 315c50dbbc68865058f6c5663952fe2f42bc5c85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478977"
---
# <span data-ttu-id="68cfd-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="68cfd-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="68cfd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="68cfd-103">Erstellt eine HybridConnection im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="68cfd-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68cfd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68cfd-104">SYNTAX</span></span>

### <span data-ttu-id="68cfd-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="68cfd-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68cfd-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="68cfd-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68cfd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68cfd-107">DESCRIPTION</span></span>
<span data-ttu-id="68cfd-108">Das New-AzureRmRelayHybridConnection-Cmdlet erstellt eine HybridConnection im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="68cfd-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="68cfd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68cfd-109">EXAMPLES</span></span>

### <span data-ttu-id="68cfd-110">Beispiel 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="68cfd-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection
```

<span data-ttu-id="68cfd-111">Erstellt eine neue HybirdConnection \` \` -TestHybirdConnection2 im angegebenen Relay \` -Namespace TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="68cfd-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="68cfd-112">Beispiel 2 – Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68cfd-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"
```

<span data-ttu-id="68cfd-113">Erstellt eine neue HybirdConnection \` \` -TestHybirdConnection1 im angegebenen Relay \` -Namespace TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="68cfd-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="68cfd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="68cfd-114">PARAMETERS</span></span>

### <span data-ttu-id="68cfd-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="68cfd-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="68cfd-116">true, wenn die Clientautorisierung für diesen HybridConnections erforderlich ist, andernfalls false. andernfalls false</span><span class="sxs-lookup"><span data-stu-id="68cfd-116">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="68cfd-117">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="68cfd-117">-UserMetadata</span></span>
<span data-ttu-id="68cfd-118">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="68cfd-118">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="68cfd-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68cfd-119">-Confirm</span></span>
<span data-ttu-id="68cfd-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68cfd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68cfd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68cfd-121">-WhatIf</span></span>
<span data-ttu-id="68cfd-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68cfd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68cfd-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68cfd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68cfd-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68cfd-124">-InputObject</span></span>
<span data-ttu-id="68cfd-125">HybridConnections-Objekt.</span><span class="sxs-lookup"><span data-stu-id="68cfd-125">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68cfd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="68cfd-126">-Name</span></span>
<span data-ttu-id="68cfd-127">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="68cfd-127">HybridConnections Name.</span></span>

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

### <span data-ttu-id="68cfd-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="68cfd-128">-Namespace</span></span>
<span data-ttu-id="68cfd-129">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="68cfd-129">Namespace Name.</span></span>

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

### <span data-ttu-id="68cfd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68cfd-130">-ResourceGroupName</span></span>
<span data-ttu-id="68cfd-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="68cfd-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="68cfd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cfd-132">-DefaultProfile</span></span>
<span data-ttu-id="68cfd-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68cfd-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68cfd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cfd-134">CommonParameters</span></span>
<span data-ttu-id="68cfd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68cfd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cfd-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68cfd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cfd-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68cfd-137">INPUTS</span></span>

### <span data-ttu-id="68cfd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68cfd-138">-ResourceGroupName</span></span>
<span data-ttu-id="68cfd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="68cfd-139">System.String</span></span>

### <span data-ttu-id="68cfd-140">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="68cfd-140">-NamespaceName</span></span>
<span data-ttu-id="68cfd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="68cfd-141">System.String</span></span>

### <span data-ttu-id="68cfd-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="68cfd-142">-HybridConnectionsName</span></span>
<span data-ttu-id="68cfd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="68cfd-143">System.String</span></span>

### <span data-ttu-id="68cfd-144">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68cfd-144">-InputObject</span></span>
<span data-ttu-id="68cfd-145">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="68cfd-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="68cfd-146">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="68cfd-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="68cfd-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68cfd-147">System.Boolean</span></span>

### <span data-ttu-id="68cfd-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="68cfd-148">-UserMetadata</span></span>
<span data-ttu-id="68cfd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="68cfd-149">System.String</span></span>

## <span data-ttu-id="68cfd-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68cfd-150">OUTPUTS</span></span>

### <span data-ttu-id="68cfd-151">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="68cfd-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="68cfd-152">Examples-1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="68cfd-152">Examples - 1 : InputObject</span></span>
<span data-ttu-id="68cfd-153">CreatedAt: 4/26/2017 10:04:15 pm UpdatedAt: 4/26/2017 10:04:15 pm ListenerCount: RequiresClientAuthorization: true UserMetadata: User Meta Data ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 Name: TestHybirdConnection2 Art: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="68cfd-153">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="68cfd-154">Beispiele-2: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68cfd-154">Examples - 2 : Properties</span></span>
<span data-ttu-id="68cfd-155">CreatedAt: 4/26/2017 10:04:15 pm UpdatedAt: 4/26/2017 10:04:15 pm ListenerCount: RequiresClientAuthorization: true UserMetadata: User Meta Data ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 Name: TestHybirdConnection1 Typ: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="68cfd-155">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="68cfd-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="68cfd-156">NOTES</span></span>

## <span data-ttu-id="68cfd-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68cfd-157">RELATED LINKS</span></span>

