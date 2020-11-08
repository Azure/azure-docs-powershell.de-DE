---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006089"
---
# Publish-AzureServiceProject

## Synopsis
Veröffentlichen Sie den aktuellen Dienst in Windows Azure.

## Syntax

### PublishFromServiceDefinition (Standard)
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### PublishFromPackage
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Mit dem Cmdlet " **Publish-AzureServiceProject** " wird der aktuelle Dienst in der Cloud veröffentlicht.
Sie können die Veröffentlichungskonfiguration (wie **Abonnement** , **StorageAccountName** , **Speicherort** , **Steckplatz** ) in der Befehlszeile oder in den lokalen Einstellungen über das Cmdlet " **Satz-AzureServiceProject** " angeben.

## Beispiele

### Beispiel 1: Veröffentlichen eines Dienstprojekts mit Standardwerten
```
PS C:\> Publish-AzureServiceProject
```

In diesem Beispiel wird der aktuelle Dienst unter Verwendung der aktuellen Diensteinstellungen und des aktuellen Azure Publish-Profils veröffentlicht.

### Beispiel 2: Erstellen eines Bereitstellungspakets
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

In diesem Beispiel wird eine Bereitstellungspaket Datei (cspkg) im Dienstverzeichnis erstellt und nicht in Windows Azure veröffentlicht.

## Parameter

### -Affinitygroup
Gibt die affinitätsgruppe an, die der Dienst verwenden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konfiguration
Gibt die Konfigurationsdatei des Diensts an.
Wenn Sie diesen Parameter angeben, geben Sie den *Package* -Parameter an.

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Deploymentname
Gibt den Bereitstellungsnamen an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Start
Öffnet ein Browserfenster, in dem Sie die Anwendung anzeigen können, nachdem Sie bereitgestellt wurde.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standort
Der Bereich, in dem die Anwendung gehostet wird.
Mögliche Werte: 
  
- Überall in Asien
- Überall in Europa
- Überall in den USA
- Ostasien
- East US
- Nord-Zentral-USA
- Nordeuropa
- Süd-Mittelamerika
- Südostasien
- West Europa
- West-US
 
Wenn kein Standort angegeben ist, wird der im letzten Aufruf von **AzureServiceProject** angegebene Speicherort verwendet. Wenn kein Standort angegeben wurde, wird der Standort nach dem Zufallsprinzip aus den Speicherorten "North Central US" und "South Central US" ausgewählt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Paket
Gibt die Paketdatei an, die bereitgestellt werden soll.
Geben Sie entweder eine lokale Datei mit der Dateinamenerweiterung cspkg oder einen URI mit einem BLOB an, das das Paket enthält.
Wenn Sie diesen Parameter angeben, geben Sie den Parameter *ServiceName* nicht an.

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

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

### -ServiceName
Gibt den Namen an, der für den Dienst beim Veröffentlichen in Windows Azure verwendet werden soll.
Der Name bestimmt einen Teil der Bezeichnung in der cloudapp.net-Unterdomäne, die verwendet wird, um den Dienst zu adressieren, wenn er in Windows Azure gehostet wird (also **Name**. cloudapp.net).
Jeder beim Veröffentlichen des Diensts angegebene Name überschreibt den Namen, der beim Erstellen des Diensts angegeben wurde.
(Siehe Cmdlet " **New-AzureServiceProject** ").

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Der für diesen Dienst zu verwendende Bereitstellungs Steckplatz.
Mögliche Werte sind "Staging" und "Production".
Wenn kein Steckplatz angegeben ist, wird der im letzten Aufruf von Set-AzureDeploymentSlot angegebene Steckplatz verwendet.
Wenn kein Steckplatz jemals angegeben wurde, wird der ' Production '-Slot verwendet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Gibt den Namen des Windows Azure-speicherkontos an, das beim Veröffentlichen des Diensts verwendet werden soll.
Dieser Wert wird erst verwendet, wenn der Dienst veröffentlicht wurde.
Wenn dieser Parameter nicht angegeben wird, wird der Wert aus dem letzten Befehl für **AzureServiceProject** abgerufen.
Wenn überhaupt kein Speicherkonto angegeben wurde, wird ein Speicherkonto verwendet, das dem Namen des Diensts entspricht.
Wenn kein solches Speicherkonto vorhanden ist, versucht das Cmdlet, eine neue zu erstellen.
Der Versuch kann jedoch fehlschlagen, wenn ein Speicherkonto, das dem Dienstnamen entspricht, in einem anderen Abonnement vorhanden ist.

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
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

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Satz-AzureServiceProject](./Set-AzureServiceProject.md)


