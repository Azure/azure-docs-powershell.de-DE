---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006188"
---
# New-AzureSSHKey

## Synopsis
Erstellt ein SSH-Schlüsselobjekt zum Einfügen eines vorhandenen Zertifikats in einen neuen Linux-basierten Azure Virtual Machines.

## Syntax

### keyPair
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### PublicKey
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureSSHKey** erstellt ein SSH-Schlüsselobjekt für ein Zertifikat, das bereits zu Azure hinzugefügt wurde.
Dieses SSH-Schlüsselobjekt kann dann von **New-AzureProvisioningConfig** verwendet werden, wenn das Konfigurationsobjekt für einen neuen virtuellen Computer mithilfe von **New-AzureVM** oder beim Erstellen eines neuen virtuellen Computers mit **New-AzureQuickVM** erstellt wird.
Wenn Sie als Teil eines Skripts für die Erstellung virtueller Maschinen enthalten sind, wird dem neuen virtuellen Computer der angegebene SSH-öffentlicher Schlüssel oder Schlüsselpaar hinzugefügt.

## Beispiele

### Beispiel 1: Erstellen eines Zertifikats Einstellungs Objekts
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

Dieser Befehl erstellt ein Zertifikat Einstellungsobjekt für ein vorhandenes Zertifikat und speichert das Objekt dann zur späteren Verwendung in einer Variablen.

### Beispiel 2: Hinzufügen eines Zertifikats zu einem Dienst
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

Dieser Befehl fügt einem Azure-Dienst ein Zertifikat hinzu und erstellt dann einen neuen virtuellen Linux-Computer, der das Zertifikat verwendet.

## Parameter

### -Fingerabdruck
Gibt den Fingerabdruck des Zertifikats an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -KeyPair
Gibt an, dass dieses Cmdlet ein Objekt zum Einfügen eines SSH-Schlüsselpaars in die neue Konfiguration des virtuellen Computers erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Gibt den Pfad zum Speichern des öffentlichen SSH-Schlüssels oder Schlüsselpaars an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicKey
Gibt an, dass dieses Cmdlet ein Objekt zum Einfügen eines öffentlichen SSH-Schlüssels in die Konfiguration des neuen virtuellen Computers erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Neu – AzureVMConfig](./New-AzureVMConfig.md)

[Neu – AzureVM](./New-AzureVM.md)

[Neu – AzureQuickVM](./New-AzureQuickVM.md)


