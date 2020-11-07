---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: af4927631b126f068495b3b130dfc560874834cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662405"
---
# Set-AzureRmWcfRelay

## Synopsis
Aktualisiert die Beschreibung einer WcfRelay im angegebenen Relay-Namespace.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### WcfRelayInputObjectSet
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### WcfRelayPropertiesSet
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Set-AzureRmWcfRelay-Cmdlet aktualisiert die Beschreibung für das WcfRelay im angegebenen Relay-Namespace.

## Beispiele

### Beispiel 1: Inputobject
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### Beispiel 2 – Eigenschaften
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

Aktualisiert den angegebenen WcfRelay mit einer neuen Beschreibung im angegebenen Namespace.
In diesem Beispiel wird die UserMetadata-Eigenschaft mit neuem Wert aktualisiert.

## Parameter

### -UserMetadata
Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

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

### -Inputobject
WcfRelay-Objekt.

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
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
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Namespace Name.

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

### -ResourceGroupName
Name der Ressourcengruppe.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -UserMetadata
System. String

## Ausgaben

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes

### Beispiel 1: Inputobject

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
Relaytype: http CreatedAt: 4/26/2017 5:14:46 pm UpdatedAt: 4/26/2017 5:16:50 pm ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false UserMetadata: UserMetadata ist ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt. beispielsweise Sie kann zum Speichern von DESC-riptive-Daten verwendet werden, wie beispielsweise die Liste der Teams und deren Kontaktinformationen, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.
ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-Storage-WestUS/Providers/Microsoft.rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Typ: Microsoft. Relay/WcfRelays

### Beispiel 2 – Eigenschaften

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
Relaytype: NetTcp CreatedAt: 4/26/2017 5:20:08 pm UpdatedAt: 4/26/2017 5:26:09 pm ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: User Meta Data ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-Storage-WestUS/Providers/Microsoft.rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay: TestWCFRelay Type: Microsoft. Relay/WcfRelays

## Notizen

## Verwandte Links

