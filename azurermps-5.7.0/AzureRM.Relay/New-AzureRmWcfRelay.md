---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: c70c5459f87925d04291f4d5ead15f44ef681bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501429"
---
# New-AzureRmWcfRelay

## Synopsis
Erstellt eine WcfRelay im angegebenen Relay-Namespace.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### WcfRelayInputObjectSet
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### WcfRelayPropertiesSet
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-WcfRelayType <String>] [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>]
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das New-AzureRmWcfRelay-Cmdlet erstellt eine WcfRelay im angegebenen Relay-Namespace.

## Beispiele

### Beispiel 1: Inputobject
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

Erstellt eine neue WcfRelay \` \` -TestWCFRelay2 im angegebenen Relay \` -Namespace TestNameSpace-Relay \` .

### Beispiel 2 – Eigenschaften
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

Erstellt eine neue WcfRelay \` \` -TestWCFRelay im angegebenen Relay \` -Namespace TestNameSpace-Relay1 \` .

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
WcfRelay-Objekt.

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
WcfRelay-Name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Namespace Name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RequiresClientAuthorization
true, wenn die Clientautorisierung für dieses Relay erforderlich ist, andernfalls false. andernfalls false

```yaml
Type: Boolean
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RequiresTransportSecurity
true, wenn Transportsicherheit für dieses Relay erforderlich ist, andernfalls false. andernfalls false

```yaml
Type: Boolean
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserMetadata
Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WcfRelayType
WcfRelay-Typ.
Mögliche Werte sind: "NetTcp" oder "http"

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### -ResourceGroupName
System. String

### -Namespacename
System. String

### -WcfRelayName
System. String

### -Inputobject
Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes

### -WcfRelayType
System. String

### -RequiresClientAuthorization
System. Boolean

### -RequiresTransportSecurity
System. Boolean

### -UserMetadata
System. String

## Ausgaben

### Beispiel 1: Inputobject

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
Relaytype: http-CreatedAt: 4/26/2017 5:14:46 Uhr UpdatedAt: 4/26/2017 5:14:46 pm ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false UserMetadata: TestWCFRelay2 ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-Storage-WestUS/Providers/Microsoft.rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2: TestWCFRelay2 Typ: Microsoft. Relay/WcfRelays

### Beispiel 2 – Eigenschaften

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
Relaytype: NetTcp CreatedAt: 4/26/2017 5:20:08 pm UpdatedAt: 4/26/2017 5:20:08 pm ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: User Meta Data ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-Storage-WestUS/Providers/Microsoft.rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay: TestWCFRelay Type: Microsoft. Relay/WcfRelays

## Notizen

## Verwandte Links

