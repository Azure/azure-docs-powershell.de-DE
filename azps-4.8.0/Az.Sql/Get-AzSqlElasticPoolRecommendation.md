---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010450"
---
# Get-AzSqlElasticPoolRecommendation

## Synopsis
Erhält Empfehlungen für elastische Pools.

## Syntax

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzSqlElasticPoolRecommendation** " erhält elastische Pool Empfehlungen für einen Server.
Diese Empfehlungen umfassen die folgenden Werte:
- DatabaseCollection. Eine Sammlung von Datenbanknamen, die zum Pool gehören. 
- DatabaseDtuMin. DTU-Garantie für Datenbanken im Elastic-Pool. 
 -- DatabaseDtuMax. DTU-Cap für Datenbanken im Elastic-Pool. 
- DTU. DTU-Garantie für den elastischen Pool. 
- StorageMb. Speicherplatz in Megabyte für den elastischen Pool 
- Edition. Edition für den elastischen Pool. Die akzeptablen Werte für diesen Parameter sind: Basic, Standard und Premium. 
- IncludeAllDatabases. Gibt an, ob alle Datenbanken im Elastic-Pool zurückgegeben werden. 
- Namen. Name des elastischen Pools.

## Beispiele

### Beispiel 1: Abrufen von Empfehlungen für einen Server
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Dieser Befehl ruft die Empfehlungen für den elastischen Pool für den Server mit dem Namen SERVER01 ab.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.

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

### -Servername
Gibt den Namen des Servers an, für den dieses Cmdlet Empfehlungen erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Management. SQL. LegacySdk. Models. UpgradeRecommendedElasticPoolProperties

## Notizen

## Verwandte Links
