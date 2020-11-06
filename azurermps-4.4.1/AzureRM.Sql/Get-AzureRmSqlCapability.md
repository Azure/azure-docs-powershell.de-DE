---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
ms.openlocfilehash: 98d45109af99658f8f6bd7847646818b30469a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503925"
---
# Get-AzureRmSqlCapability

## Synopsis
Ruft SQL-Datenbankfunktionen für das aktuelle Abonnement ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### FilterResults (Standard)
```
Get-AzureRmSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DefaultResults
```
Get-AzureRmSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmSqlCapability** " Ruft die Azure SQL-Datenbankfunktionen ab, die für das aktuelle Abonnement für einen Bereich verfügbar sind.
Wenn Sie die *ServerVersionName* -, *EditionName* -oder *ServiceObjectiveName* -Parameter angeben, gibt dieses Cmdlet die angegebenen Werte und ihre Vorgänger zurück.

## Beispiele

### Beispiel 1: Abrufen von Funktionen für das aktuelle Abonnement für einen Bereich
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

Dieser Befehl gibt die Funktionen für SQL-Datenbankinstanzen für das aktuelle Abonnement für die zentrale US-Region zurück.

### Beispiel 2: Abrufen von Standardfunktionen für das aktuelle Abonnement für einen Bereich
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

Dieser Befehl gibt die Standardfunktionen für SQL-Datenbanken für das aktuelle Abonnement in der zentralen US-Region zurück.

### Beispiel 3: Abrufen von Details zu einem Dienst Ziel
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

Dieser Befehl ruft Standardfunktionen für SQL-Datenbanken für das angegebene Dienst Ziel für das aktuelle Abonnement ab.

## Parameter

### – Standardeinstellungen
Gibt an, dass dieses Cmdlet nur Standardwerte erhält.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EditionName
Gibt den Namen der Database Edition an, für die dieses Cmdlet Funktionen erhält.

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standortname
Gibt den Namen des Speicherorts an, für den dieses Cmdlet Funktionen erhält.
Weitere Informationen finden Sie unter Azure-Bereiche https://azure.microsoft.com/en-us/regions/ ( https://azure.microsoft.com/en-us/regions/) .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerVersionName
Gibt den Namen der Server Version an, für die dieses Cmdlet Funktionen erhält.

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Gibt den Namen des Dienst Ziels an, für das dieses Cmdlet Funktionen erhält.

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### Microsoft.Azure.Commands.SQL.Location_Capabilities. Model. LocationCapabilityModel

## Notizen

## Verwandte Links

