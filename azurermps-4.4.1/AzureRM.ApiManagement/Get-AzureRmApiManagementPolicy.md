---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498105"
---
# Get-AzureRmApiManagementPolicy

## Synopsis
Ruft die angegebene Bereichs Richtlinie ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Mandantenebene (Standard)
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Produktebene
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### API-Ebene
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Vorgangsebene
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmApiManagementPolicy** " Ruft die angegebene Bereichs Richtlinie ab.

## Beispiele

### Beispiel 1: Abrufen der Richtlinie für Mandantenebene
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

Dieser Befehl ruft die Richtlinie für Mandantenebene ab und speichert Sie in einer Datei mit dem Namen tenantpolicy.xml.

### Beispiel 2: Abrufen der Richtlinie für den Produktbereich
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

Dieser Befehl ruft die Richtlinie für den Produktbereich ab

### Beispiel 3: Abrufen der API-Bereichs Richtlinie
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

Dieser Befehl ruft eine Richtlinie für den API-Bereich ab.

### Beispiel 4: Abrufen der Richtlinie für den Vorgangsbereich
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

Mit diesem Befehl wird die Richtlinie für den Vorgangsbereich abgerufen.

## Parameter

### -ApiId
Gibt den Bezeichner der vorhandenen API an.
Wenn Sie diesen Parameter angeben, gibt das Cmdlet die Richtlinie für den API-Bereich zurück.

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
Gibt eine Instanz von **PsApiManagementContext** an.

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

### -Force
ps_force

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

### -Format
Gibt das Format der API-Verwaltungsrichtlinie an.
Der Standardwert für diesen Parameter ist "application/vnd. ms-Azure-APIM. Policy + XML".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vorgangs-Nr
Gibt den Bezeichner des vorhandenen API-Vorgangs an.
Wenn Sie diesen Parameter mit *ApiId* angeben, gibt das Cmdlet die Richtlinie für den Vorgangsbereich zurück.

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

### -ProductID
Gibt den Bezeichner eines vorhandenen Produkts an.
Wenn Sie diesen Parameter angeben, gibt das Cmdlet die Richtlinie für den Produktbereich zurück.

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

### -SaveAs
Gibt den Dateipfad an, in dem das Ergebnis gespeichert werden soll.
Wenn Sie diesen Parameter nicht angeben, wird das Ergebnis als Stich Pipeline durchlaufen.

```yaml
Type: System.String
Parameter Sets: (All)
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

### Zeichenfolge

## Notizen

## Verwandte Links

[Remove-AzureRmApiManagementPolicy](./Remove-AzureRmApiManagementPolicy.md)

[Satz-AzureRmApiManagementPolicy](./Set-AzureRmApiManagementPolicy.md)


