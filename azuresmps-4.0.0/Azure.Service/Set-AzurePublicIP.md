---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006161"
---
# Set-AzurePublicIP

## Synopsis
Fügt eine öffentliche IP-Adresse zu einem Azure Virtual Machine hinzu.

## Syntax

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzurePublicIP** " fügt eine öffentliche IP-Adresse zu einem Azure-virtuellen Computer hinzu.
Wenn Sie dieses Cmdlet für einen vorhandenen virtuellen Computer ausführen, aktualisieren Sie den virtuellen Computer, um Ihre Änderungen zu implementieren.
Sie können ein Domain Name-Label angeben, um einen entsprechenden DNS-Eintrag für die öffentliche IP-Adresse zu erstellen.

## Beispiele

### Beispiel 1: Hinzufügen einer öffentlichen IP zu einem vorhandenen virtuellen Computer
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen FTPInstance im Dienst FTPInAzure mit dem Cmdlet **Get-AzureVM** ab.
Der Befehl übergibt diesen virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet fügt den öffentlichen IP-Namen ftpip hinzu.
Der Befehl übergibt den virtuellen Computer an das Cmdlet **Update-AzureVM** , das Ihre Änderungen implementiert.

### Beispiel 2: Hinzufügen einer öffentlichen IP zu einem neuen virtuellen Computer
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Mit diesem Befehl wird ein Virtual Machine-Konfigurationsobjekt mithilfe des Cmdlets **New-AzureVMConfig** erstellt.
Der Befehl übergibt das Objekt an das Cmdlet **Add-AzureProvisioningConfig** , das zusätzliche Konfiguration bereitstellt.
Das aktuelle Cmdlet fügt den öffentlichen IP-Namen ftpip hinzu.
Der Befehl übergibt die Konfiguration an das Cmdlet **New-AzureVM** , das den virtuellen Computer erstellt.

### Beispiel 3: Hinzufügen einer öffentlichen IP-Adresse und einer Bezeichnung zu einem vorhandenen virtuellen Computer
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen FTPInstance im Dienst FTPInAzure mit dem Cmdlet **Get-AzureVM** ab.
Der Befehl übergibt diesen virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet addiert den öffentlichen IP-Namen ftpip und das Label ipname.
Der Befehl aktualisiert den virtuellen Computer, der Ihre Änderungen implementiert.

### Beispiel 4: Hinzufügen einer öffentlichen IP-Adresse und einer Bezeichnung zu einem neuen virtuellen Computer
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Mit diesem Befehl wird ein Virtual Machine Configuration-Objekt erstellt, und das Objekt wird dann an **Add-AzureProvisioningConfig** übergeben, wodurch eine zusätzliche Konfiguration bereitgestellt wird.
Das aktuelle Cmdlet addiert den öffentlichen IP-Namen ftpip und das Label ipname.
Der Befehl erstellt den virtuellen Computer.

## Parameter

### -DomainNameLabel
Gibt den Namen an, der für einen entsprechenden DNS-Eintrag für die öffentliche IP-Adresse verwendet werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
Gibt den TCP-Leerlauftimeout Zeitraum in Minuten an.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

### -PublicIPName
Gibt den öffentlichen IP-Namen an.

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

### -VM
Gibt den virtuellen Computer an, dem dieses Cmdlet Public IP hinzufügt.

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

### Microsoft. WindowsAzure. Commands. Servicemanagement. Model. IPersistentVM

## Notizen

## Verwandte Links

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[Get-AzureVM](./Get-AzureVM.md)

[Neu – AzureVM](./New-AzureVM.md)

[Neu – AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzurePublicIP](./Remove-AzurePublicIP.md)

[Update-AzureVM](./Update-AzureVM.md)


