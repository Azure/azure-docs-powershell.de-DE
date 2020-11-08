---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006577"
---
# Get-AzureAutomationAccount

## Synopsis

Ruft Azure Automation-Konten ab.

## Syntax

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Das Cmdlet " **Get-AzureAutomationAccount** " Ruft die Microsoft Azure Automation-Konten für Ihr Abonnement ab.
Bei einem Automatisierungs Konto handelt es sich um einen Container für Automatisierungs Ressourcen, der von den Ressourcen anderer Automatisierungs Konten isoliert ist.
Automatisierungs Ressourcen umfassen runbooks, Aufträge und Ressourcen.

## Beispiele

### Beispiel 1: Abrufen eines Automatisierungs Kontos
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

Dieser Befehl ruft das Automatisierungs Konto mit dem Namen Contoso17 ab.

## Parameter

### -Standort
Gibt eine Azure-Position an, die Automatisierungs Konten zugeordnet ist.

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

### -Name
Gibt den Namen eines Azure Automation-Kontos an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. AutomationAccount

## Notizen

## Verwandte Links

[Neu – AzureAutomationAccount](./New-AzureAutomationAccount.md)

[Remove-AzureAutomationAccount](./Remove-AzureAutomationAccount.md)


