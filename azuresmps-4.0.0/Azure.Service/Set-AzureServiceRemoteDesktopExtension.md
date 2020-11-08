---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006019"
---
# Set-AzureServiceRemoteDesktopExtension

## Synopsis
Aktiviert die Remote Desktop Erweiterung für bestimmte Rollen oder alle Rollen in einem bereitgestellten Dienst oder bei der Bereitstellung.

## Syntax

### Setextension (Standard)
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### SetExtensionUsingThumbprint
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureServiceRemoteDesktopExtension** " ermöglicht die Remote Desktop Erweiterung für bestimmte Rollen oder alle Rollen in einem bereitgestellten Dienst oder bei der Bereitstellung.

## Beispiele

### Beispiel 1: Aktivieren der Remote Desktop Erweiterung
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

Mit diesem Befehl wird die Remote Desktop Erweiterung für den angegebenen Dienst aktiviert.

### Beispiel 2: Aktivieren der Remote Desktop Erweiterung für eine bestimmte Rolle
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

Mit diesem Befehl wird die Remote Desktop Erweiterung für den angegebenen Dienst und die angegebene Rolle aktiviert.

## Parameter

### -CertificateThumbprint
Gibt einen Zertifikat Fingerabdruck an, der zum Verschlüsseln der privaten Konfiguration verwendet werden soll.
Dieses Zertifikat muss bereits im Zertifikatspeicher vorhanden sein.
Wenn Sie kein Zertifikat angeben, erstellt dieses Cmdlet ein Zertifikat.

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Anmeldeinformationen
Gibt die Anmeldeinformationen an, die für den Remote Desktop aktiviert werden sollen.
Zu den Anmeldeinformationen gehören ein Benutzername und ein Kennwort.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ablauf
Gibt ein Datum Zeit Objekt an, mit dem der Benutzer angeben kann, wann das Benutzerkonto abläuft.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Erweiterungs-Nr
Gibt die Erweiterungs-ID an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Role
Gibt ein optionales Array von Rollen an, für das die Remote Desktopkonfiguration angegeben werden soll.
Wenn dieser Parameter nicht angegeben wird, wird die Remote Desktopkonfiguration als Standardkonfiguration für alle Rollen verwendet.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Gibt den Azure-Dienstnamen der Bereitstellung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Gibt die Umgebung der Bereitstellung an, die geändert werden soll.
Die akzeptablen Werte für diesen Parameter sind: Production, Staging.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThumbprintAlgorithm
Gibt einen Hashalgorithmus für den Fingerabdruck an, der mit dem Fingerabdruck verwendet wird, um das Zertifikat zu identifizieren.
Dieser Parameter ist optional, und der Standardwert ist SHA1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gibt die Erweiterungsversion an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -X509Certificate
Gibt ein x509-Zertifikat an, das automatisch in den clouddienst hochgeladen und zum Verschlüsseln der privaten Konfiguration der Erweiterung verwendet wird.

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureServiceRemoteDesktopExtension](./Get-AzureServiceRemoteDesktopExtension.md)


