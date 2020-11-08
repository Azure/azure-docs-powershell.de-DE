---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006251"
---
# Set-AzureVMChefExtension

## Synopsis
Fügt dem virtuellen Computer die Erweiterung "Chef" hinzu.

## Syntax

### Windows (Standard)
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureVMChefExtension** " fügt der virtuellen Maschine die Erweiterung "Chef" hinzu.

## Beispiele

### Beispiel 1: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

Mit diesem Befehl wird eine Erweiterung des Chefkochs zu einem virtuellen Windows-Computer hinzugefügt.
Wenn die virtuelle Maschine auftaucht, ist Sie bootstrapped mit dem Chefkoch und führt Apache auf Sie.

### Beispiel 2: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Windows-Computer mit Bootstrapping
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

Mit diesem Befehl wird die Erweiterung des Chefkochs zu einem virtuellen Windows-Computer hinzugefügt.
Wenn die virtuelle Maschine gestartet wird, ist Sie bootstrapped mit dem Chefkoch und führt Apache darauf aus.
Nach dem Bootstrapping verweist der virtuelle Computer auf die im JSON-Format angegebenen *bootstrapoptions* .

### Beispiel 3: Hinzufügen einer Erweiterung des Chefkochs zu einem virtuellen Windows-Computer und Installieren von Apache und git
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

Mit diesem Befehl wird die Erweiterung des Chefkochs zu einem virtuellen Windows-Computer hinzugefügt.
Wenn die virtuelle Maschine gestartet wird, ist Sie mit dem Chefkoch bootstrapped und hat Apache und Git installiert.
Wenn Sie den Client. RB nicht angeben, müssen Sie den Chefkoch-Server-URL und den Namen des Validierungs Clients angeben.

### Beispiel 4: Hinzufügen einer Chefkoch-Erweiterung zu einem virtuellen Linux-Computer
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

Mit diesem Befehl wird die Erweiterung des Chefkochs zu einem virtuellen Linux-Computer hinzugefügt.
Wenn die virtuelle Maschine gestartet wird, ist Sie bootstrapped mit dem Chefkoch.
Wenn Sie den Client. RB nicht angeben, müssen Sie die Server-URL und die Organisation des Chefkochs angeben.

## Parameter

### -Bootstrapoptions
Gibt Bootstrap-Optionen im JSON-Format (JavaScript Object Notation) an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BootstrapVersion
Gibt die Version des Chefkoch-Clients an, die zusammen mit der Erweiterung installiert wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ChefDaemonInterval
Gibt die Häufigkeit (in Minuten) an, auf der der Chef-Service ausgeführt wird. Wenn Sie nicht möchten, dass der Chef-Service auf dem Azure VM installiert wird, setzen Sie in diesem Feld den Wert 0.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ChefServerUrl
Gibt die URL des Chef Servers an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRb
Gibt den vollständigen Pfad des Chefkoch-Clients. RB an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Daemon
Konfiguriert den Chef-Client Dienst für die unbeaufsichtigte Ausführung. Die Knoten Plattform sollte Windows sein.
Zulässige Optionen: "keine", "Dienst" und "Aufgabe".
keine – zurzeit wird verhindert, dass der Chef-Client-Dienst als Dienst konfiguriert wird.
Dienst – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als Dienst ausgeführt wird.
Aufgabe – konfiguriert den Chef-Client so, dass er automatisch im Hintergrund als secheduled-Aufgabe ausgeführt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -Jsonattribute
Eine JSON-Zeichenfolge, die der ersten Ausführung von Chef-Client hinzugefügt werden soll. beispielsweise-jsonattribute ' {"foo": "Leiste"} '

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Gibt an, dass mit diesem Cmdlet ein Linux-basierter virtueller Computer erstellt wird.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrganizationName
Gibt den Organisationsnamen der Erweiterung "Chef" an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -RunList
Gibt die Liste "Leiter Knoten ausführen" an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Der Verschlüsselungsschlüssel, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secretdatei
Der Pfad zu der Datei, die den Verschlüsselungsschlüssel enthält, der zum Verschlüsseln und Entschlüsseln der Daten Beutel-Elementwerte verwendet wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ValidationClientName
Gibt den Namen des Validierungs Clients an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ValidationPem
Gibt den Datei Pfad des Chefkochs Validator. PEM an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gibt die Versionsnummer der Erweiterung "Chef" an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des beständigen virtuellen Computers an.

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

### -Windows
Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
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

[Get-AzureVMChefExtension](./Get-AzureVMChefExtension.md)

[Remove-AzureVMChefExtension](./Remove-AzureVMChefExtension.md)


