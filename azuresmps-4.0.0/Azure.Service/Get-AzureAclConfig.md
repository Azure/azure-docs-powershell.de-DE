---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005879"
---
# Get-AzureAclConfig

## Synopsis
Ruft das ACL-Konfigurationsobjekt von einem Azure Virtual Machine ab.

## Syntax

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureAclConfig** " Ruft das Konfigurationsobjekt für die Zugriffssteuerungsliste (ACL) von einem vorhandenen Azure Virtual Machine ab.

## Beispiele

### Beispiel 1: Abrufen eines ACL-Konfigurationsobjekts für einen Endpunkt einer virtuellen Maschine
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.
Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das Cmdlet " **Get-AzureAclConfig** ".
Dieses Cmdlet ruft die ACL-Konfiguration für den Endpunkt mit dem Namen Web ab.
Der Befehl speichert das ACL-Konfigurationsobjekt in der $ACL-Variablen.

## Parameter

### -Endpunktname
Gibt den Namen des Endpunkts an, für den dieses Cmdlet eine ACL erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des virtuellen Computers an, für das dieses Cmdlet eine ACL-Konfiguration erhält.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureVM](./Get-AzureVM.md)

[Neu – AzureAclConfig](./New-AzureAclConfig.md)

[Remove-AzureAclConfig](./Remove-AzureAclConfig.md)

[Satz-AzureAclConfig](./Set-AzureAclConfig.md)


