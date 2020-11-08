---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006138"
---
# New-AzureCertificateSetting

## Synopsis
Erstellt ein Zertifikat Einstellungsobjekt für ein Zertifikat befindet sich in einem Dienst.

## Syntax

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureCertificateSetting** erstellt ein Zertifikat Einstellungsobjekt für ein Zertifikat, das sich in einem Azure-Dienst befindet.

Mithilfe des Cmdlets **Add-AzureProvisioningConfig** können Sie ein Certificate Setting-Objekt verwenden, um ein Configuration-Objekt zu erstellen.
Verwenden Sie ein Configuration-Objekt zum Erstellen eines virtuellen Computers mithilfe des Cmdlets **New-AzureVM** .
Mithilfe des Cmdlets **New-AzureQuickVM** können Sie ein Zertifikat Einstellungsobjekt zum Erstellen eines virtuellen Computers verwenden.

## Beispiele

### Beispiel 1: Erstellen eines Zertifikats Einstellungs Objekts
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

Mit diesem Befehl wird ein Zertifikat Einstellungsobjekt für ein vorhandenes Zertifikat erstellt.

### Beispiel 2: Erstellen eines virtuellen Computers, der ein Konfigurations Einstellungsobjekt verwendet
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Mit dem ersten Befehl wird das Zertifikat ContosoCert. CER dem Dienst mit dem Namen ContosoService mithilfe des Cmdlets **Add-AzureCertificate** hinzugefügt.

Der zweite Befehl erstellt ein Zertifikat Einstellungsobjekt und speichert es dann in der $CertificateSetting-Variablen.

Der dritte Befehl ruft mit dem Cmdlet **Get-AzureVMImage** ein Bild aus dem Bild-Repository ab.
Dieser Befehl speichert das Bild in der $Image Variablen.

Mit dem Final-Befehl wird ein Konfigurationsobjekt für virtuelle Computer basierend auf dem Bild in $Image mithilfe des Cmdlets **New-AzureVMConfig** erstellt.
Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das Cmdlet **Add-AzureProvisioningConfig** .
Dieses Cmdlet fügt der Konfiguration Bereitstellungsinformationen hinzu.
Der Befehl übergibt das Objekt an das Cmdlet **New-AzureVM** , das den virtuellen Computer erstellt.

## Parameter

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

### -StoreName
Gibt den Zertifikatspeicher an, in dem das Zertifikat abgelegt werden soll.
Gültige Werte sind: 

- AddressBook
- AuthRoot
- CertificateAuthority
- Nicht erlaubt
- Meine
- Stamm
- TrustedPeople
- TrustedPublisher

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureCertificate](./Add-AzureCertificate.md)

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Neu – AzureQuickVM](./New-AzureQuickVM.md)

[Neu – AzureVM](./New-AzureVM.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)


