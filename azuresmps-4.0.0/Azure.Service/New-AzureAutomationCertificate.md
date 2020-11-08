---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006428"
---
# New-AzureAutomationCertificate

## Synopsis

Erstellt ein Azure-Automatisierungs Zertifikat.

## Syntax

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Das Cmdlet **New-AzureAutomationCertificate** erstellt ein Zertifikat in Microsoft Azure Automation.
Sie geben den Pfad zu einer Zertifikatsdatei an, die hochgeladen werden soll.

## Beispiele

### Beispiel 1: Erstellen eines Zertifikats
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

Mit diesen Befehlen wird ein Zertifikat in Azure Automation mit dem Namen "myCertificate" erstellt.
Mit dem ersten Befehl wird das Kennwort für die Zertifikatdatei erstellt, das im zweiten Befehl zum Erstellen des Zertifikats verwendet wird.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, in dem das Zertifikat gespeichert werden soll.

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

### -Beschreibung
Gibt eine Beschreibung für das Zertifikat an.

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

### -Exportierbar
Gibt an, dass das Zertifikat exportiert werden kann.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für das Zertifikat an.

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

### -Kennwort
Gibt das Kennwort für die Zertifikatsdatei an.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den Pfad zu einer Skriptdatei an, die hochgeladen werden soll.
Die Datei kann "CER" oder ". pfx" sein.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. CertificateInfo

## Notizen

## Verwandte Links

[Get-AzureAutomationCertificate](./Get-AzureAutomationCertificate.md)

[Remove-AzureAutomationCertificate](./Remove-AzureAutomationCertificate.md)

[Satz-AzureAutomationCertificate](./Set-AzureAutomationCertificate.md)


