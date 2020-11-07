---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cd7dad03d8542685339778d0b0cdac967f83ea21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663875"
---
# Get-AzureRmOperationalInsightsStorageInsight

## Synopsis
Ruft Informationen zu einem Speicher Einblick ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByWorkspaceName (Standard)
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmOperationalInsightsStorageInsight** " Ruft Informationen zu einem vorhandenen Speicher Insight ab.
Wenn ein Speicher Insight-Name angegeben wird, erhält dieses Cmdlet Informationen zu dieser Speicher Einsicht.
Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Speicher Einblicken in einem Arbeitsbereich ab.

## Beispiele

### Beispiel 1: Abrufen eines Speicher Einblicks nach Namen
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

Dieser Befehl ruft den Speicher Einblick mit dem Namen MyStorageInsight aus dem Arbeitsbereich mit dem Namen ContosoWorkspace ab.

### Beispiel 2: Abrufen eines Speicher Einblicks mithilfe eines Workspace-Objekts
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

Der erste Befehl verwendet das Cmdlet " **Get-AzureRmOperationalInsightsWorkspace** ", um einen Arbeitsbereich für operationelle Einblicke abzurufen, und speichert ihn dann in der $Workspace-Variablen.

Der zweite Befehl ruft den Speicher Einblick mit dem Namen MyStorageInsight für den Arbeitsbereich in $Workspace ab.

## Parameter

### -Name
Gibt den Namen der Speicher Insight an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Arbeitsbereich
Gibt den Arbeitsbereich an, der die Speicher Einblicke enthält.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Gibt den Namen des Arbeitsbereichs an, der die Speicher Einblicke enthält.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### PSWorkspace
Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.

## Ausgaben

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight]

### Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight

## Notizen

## Verwandte Links

[Azure-Cmdlets für operationelle Einblicke](./AzureRM.OperationalInsights.md)


