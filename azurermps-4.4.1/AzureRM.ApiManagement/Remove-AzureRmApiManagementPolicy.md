---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 5f7fa78cb368afe3e277661122682f43f885f7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477430"
---
# Remove-AzureRmApiManagementPolicy

## Synopsis
Entfernt die API-Verwaltungsrichtlinie aus einem angegebenen Bereich.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Mandantenebene (Standard)
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Produktebene
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### API-Ebene
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Vorgangsebene
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmApiManagementPolicy** entfernt die API-Verwaltungsrichtlinie aus dem angegebenen Bereich.

## Beispiele

### Beispiel 1: Entfernen der Richtlinie für Mandantenebene
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext
```

Dieser Befehl entfernt die Richtlinie für Mandantenebene aus der API-Verwaltung.

### Beispiel 2: Entfernen der Richtlinie für den Produktbereich
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

Dieser Befehl entfernt die Richtlinie für den Produktbereich aus der API-Verwaltung.

### Beispiel 3: Entfernen der API-Bereichs Richtlinie
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

Dieser Befehl entfernt API-Bereichs Richtlinien aus der API-Verwaltung.

### Beispiel 4: Entfernen der Richtlinie für den Vorgangsbereich
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

Dieser Befehl entfernt die Richtlinie für den Vorgangsbereich aus der API-Verwaltung.

## Parameter

### -ApiId
Gibt den Bezeichner einer vorhandenen API an.
Wenn Sie diesen Parameter angeben, entfernt das Cmdlet die Richtlinie für den API-Bereich.

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Gibt die Instanz des **PsApiManagementContext** -Objekts an.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vorgangs-Nr
Gibt den Bezeichner eines vorhandenen Vorgangs an.
Wenn Sie diesen Parameter mit dem *ApiId* -Parameter angeben, entfernt dieses Cmdlet die Richtlinie für den Vorgangsbereich.

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductID
Gibt den Bezeichner des vorhandenen Produkts an.
Wenn Sie diesen Parameter angeben, entfernt das Cmdlet die Richtlinie für den Produktbereich.

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
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

### Boolean

## Notizen

## Verwandte Links

[Get-AzureRmApiManagementPolicy](./Get-AzureRmApiManagementPolicy.md)

[Satz-AzureRmApiManagementPolicy](./Set-AzureRmApiManagementPolicy.md)


