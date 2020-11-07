---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7c766d3a112b880eaaa697e1f09d0d458dee5505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663542"
---
# Set-AzureRmRelayHybridConnection

## Synopsis
Aktualisiert die Beschreibung einer HybridConnection im angegebenen Relay-Namespace.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### HybridConnectionInputObjectSet
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### HybridConnectionPropertiesSet
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Set-AzureRmRelayHybridConnection-Cmdlet aktualisiert die Beschreibung für das HybridConnection im angegebenen Relay-Namespace.

## Beispiele

### Beispiel 1
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid
```

### Beispiel 2
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"
```

Aktualisiert den angegebenen HybridConnection mit einer neuen Beschreibung im angegebenen Namespace.
In diesem Beispiel wird die UserMetadata-Eigenschaft mit neuem Wert aktualisiert.

## Parameter

### -UserMetadata
Ruft ab oder legt fest, dass usermetadata ein Platzhalter zum Speichern von benutzerdefinierten Zeichenfolgendaten für den HybridConnection-Endpunkt ist. beispielsweise Es kann verwendet werden, um beschreibende Daten wie eine Liste von Teams und deren Kontaktinformationen zu speichern, auch benutzerdefinierte Konfigurationseinstellungen können gespeichert werden.

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
HybridConnections-Objekt.

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
HybridConnections-Name.

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
Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes

### -UserMetadata
System. String

## Ausgaben

### Examples-1: Inputobject
CreatedAt: 4/26/2017 10:04:15 pm UpdatedAt: 4/26/2017 10:08:11 pm ListenerCount: RequiresClientAuthorization: true UserMetadata: Test UserMetadata ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 Name: TestHybirdConnection2 Typ: Microsoft. Relay/HybridConnections

### Beispiele-2: Eigenschaften
CreatedAt: 4/26/2017 10:04:15 pm UpdatedAt: 4/26/2017 10:10:25 pm ListenerCount: RequiresClientAuthorization: true UserMetadata: Test UserMetadata updated ID:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 Name: TestHybirdConnection1 Typ: Microsoft. Relay/HybridConnections

## Notizen

## Verwandte Links

