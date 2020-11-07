---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 9542b5af753a94e952ad2407df9ddd80f51aeb0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664515"
---
# <span data-ttu-id="41f21-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="41f21-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="41f21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41f21-102">SYNOPSIS</span></span>
<span data-ttu-id="41f21-103">Aktualisiert die Beschreibung einer HybridConnection im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="41f21-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41f21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41f21-104">SYNTAX</span></span>

### <span data-ttu-id="41f21-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="41f21-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41f21-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="41f21-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41f21-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41f21-107">DESCRIPTION</span></span>
<span data-ttu-id="41f21-108">Das Set-AzureRmRelayHybridConnection-Cmdlet aktualisiert die Beschreibung für das HybridConnection im angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="41f21-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="41f21-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41f21-109">EXAMPLES</span></span>

### <span data-ttu-id="41f21-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="41f21-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

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

### <span data-ttu-id="41f21-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="41f21-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

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

<span data-ttu-id="41f21-112">Aktualisiert den angegebenen HybridConnection mit einer neuen Beschreibung im angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="41f21-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="41f21-113">In diesem Beispiel wird die UserMetadata-Eigenschaft mit neuem Wert aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="41f21-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="41f21-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="41f21-114">PARAMETERS</span></span>

### <span data-ttu-id="41f21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f21-115">-DefaultProfile</span></span>
<span data-ttu-id="41f21-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="41f21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41f21-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41f21-117">-InputObject</span></span>
<span data-ttu-id="41f21-118">HybridConnections-Objekt.</span><span class="sxs-lookup"><span data-stu-id="41f21-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41f21-119">-Name</span><span class="sxs-lookup"><span data-stu-id="41f21-119">-Name</span></span>
<span data-ttu-id="41f21-120">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="41f21-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="41f21-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="41f21-121">-Namespace</span></span>
<span data-ttu-id="41f21-122">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="41f21-122">Namespace Name.</span></span>

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

### <span data-ttu-id="41f21-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f21-123">-ResourceGroupName</span></span>
<span data-ttu-id="41f21-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="41f21-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="41f21-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="41f21-125">-UserMetadata</span></span>
<span data-ttu-id="41f21-126">Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="41f21-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="41f21-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41f21-127">-Confirm</span></span>
<span data-ttu-id="41f21-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41f21-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41f21-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f21-129">-WhatIf</span></span>
<span data-ttu-id="41f21-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41f21-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41f21-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41f21-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41f21-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f21-132">CommonParameters</span></span>
<span data-ttu-id="41f21-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41f21-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="41f21-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f21-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f21-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41f21-135">INPUTS</span></span>

### <span data-ttu-id="41f21-136">System. String</span><span class="sxs-lookup"><span data-stu-id="41f21-136">System.String</span></span>
<span data-ttu-id="41f21-137">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="41f21-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>


## <span data-ttu-id="41f21-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41f21-138">OUTPUTS</span></span>

### <span data-ttu-id="41f21-139">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="41f21-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>


## <span data-ttu-id="41f21-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="41f21-140">NOTES</span></span>

## <span data-ttu-id="41f21-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41f21-141">RELATED LINKS</span></span>
