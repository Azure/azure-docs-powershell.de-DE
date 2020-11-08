---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006298"
---
# Remove-AzureTrafficManagerEndpoint

## Synopsis
Entfernt einen Endpunkt aus einem Datenverkehrs-Manager-Profil.

## Syntax

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureTrafficManagerEndpoint** entfernt einen Endpunkt aus einem Microsoft Azure Traffic Manager-Profil.
Nachdem Sie einen Endpunkt entfernt haben, übergeben Sie das Ergebnis mithilfe des Pipelineoperators an das Cmdlet " **Satz-AzureTrafficManagerProfile** ".
Dieses Cmdlet stellt eine Verbindung mit Azure her, um Ihre Änderungen zu speichern.

## Beispiele

### Beispiel 1: Entfernen eines Endpunkts aus einem Profil
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

Der erste Befehl verwendet das Cmdlet " **Get-AzureTrafficManagerProfile** ", um das Profil mit dem Namen ContosoProfile abzurufen, und speichert es dann in der $TrafficManagerProfile-Variablen.

Mit dem zweiten Befehl wird ein Endpunkt mit dem Domänennamen Contoso02App.cloudapp.net aus dem Profil des Datenverkehrs-Managers entfernt, das in $TrafficManagerProfile gespeichert ist.
Der Befehl übergibt das Profilobjekt an das Cmdlet " **Satz-AzureTrafficManagerProfile** ", um die Verbindung zu Azure herzustellen, um Ihre Änderungen zu speichern.

## Parameter

### -Domänenname
Gibt den Domänennamen des zu entfernenden Endpunkts an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### -TrafficManagerProfile
Gibt das Traffic Manager-Profilobjekt an, aus dem der Endpunkt entfernt werden soll.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

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

### Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition
Dieses Cmdlet generiert ein Traffic Manager-Profilobjekt, das Informationen über das aktualisierte Profil enthält.

## Notizen

## Verwandte Links

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Satz-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Satz-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


