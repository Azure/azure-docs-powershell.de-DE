---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 2b029b2a93a063a322c11ea84cd46b787acc9960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846848"
---
# <span data-ttu-id="76515-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="76515-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="76515-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76515-102">SYNOPSIS</span></span>
<span data-ttu-id="76515-103">Aktualisiert die Beschreibung einer HybridConnection im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="76515-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="76515-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76515-104">SYNTAX</span></span>

### <span data-ttu-id="76515-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76515-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76515-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="76515-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76515-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76515-107">DESCRIPTION</span></span>
<span data-ttu-id="76515-108">Das Set-AzRelayHybridConnection-Cmdlet aktualisiert die Beschreibung für das HybridConnection im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="76515-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="76515-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76515-109">EXAMPLES</span></span>

### <span data-ttu-id="76515-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76515-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="76515-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="76515-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="76515-112">Aktualisiert den angegebenen HybridConnection mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="76515-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="76515-113">In diesem Beispiel wird die UserMetadata-Eigenschaft mit neuem Wert aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="76515-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="76515-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="76515-114">PARAMETERS</span></span>

### <span data-ttu-id="76515-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76515-115">-DefaultProfile</span></span>
<span data-ttu-id="76515-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76515-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76515-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76515-117">-InputObject</span></span>
<span data-ttu-id="76515-118">HybridConnections-Objekt.</span><span class="sxs-lookup"><span data-stu-id="76515-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76515-119">-Name</span><span class="sxs-lookup"><span data-stu-id="76515-119">-Name</span></span>
<span data-ttu-id="76515-120">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="76515-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="76515-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="76515-121">-Namespace</span></span>
<span data-ttu-id="76515-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="76515-122">Namespace Name.</span></span>

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

### <span data-ttu-id="76515-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76515-123">-ResourceGroupName</span></span>
<span data-ttu-id="76515-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76515-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="76515-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="76515-125">-UserMetadata</span></span>
<span data-ttu-id="76515-126">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="76515-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="76515-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76515-127">-Confirm</span></span>
<span data-ttu-id="76515-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76515-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76515-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76515-129">-WhatIf</span></span>
<span data-ttu-id="76515-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76515-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76515-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76515-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76515-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76515-132">CommonParameters</span></span>
<span data-ttu-id="76515-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76515-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76515-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76515-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76515-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76515-135">INPUTS</span></span>

### <span data-ttu-id="76515-136">System. String</span><span class="sxs-lookup"><span data-stu-id="76515-136">System.String</span></span>

### <span data-ttu-id="76515-137">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="76515-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="76515-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76515-138">OUTPUTS</span></span>

### <span data-ttu-id="76515-139">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="76515-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="76515-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="76515-140">NOTES</span></span>

## <span data-ttu-id="76515-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76515-141">RELATED LINKS</span></span>
