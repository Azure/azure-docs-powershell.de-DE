---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498018"
---
# Set-AzureRmApiManagementPolicy

## Synopsis
Legt die angegebene Bereichs Richtlinie für die API-Verwaltung fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Mandantenebene (Standard)
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Produktebene
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### API-Ebene
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Vorgangsebene
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRmApiManagementPolicy** " legt die angegebene Bereichs Richtlinie für die API-Verwaltung fest.

## Beispiele

### Beispiel 1: Festlegen der Richtlinie für Mandantenebene
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

Dieser Befehl legt die Richtlinie für Mandantenebene aus einer Datei mit dem Namen tenantpolicy.xml fest.

### Beispiel 2: Festlegen einer Richtlinie für den Produktbereich
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

Dieser Befehl legt die Richtlinie für den Produktbereich für die API-Verwaltung fest.

### Beispiel 3: Festlegen von API-Bereichs Richtlinien
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

Dieser Befehl legt API-Bereichs Richtlinien für die API-Verwaltung fest.

### Beispiel 4: Festlegen des Vorgangs Bereichs Richtlinien
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

Dieser Befehl legt die Richtlinie für den Vorgangsbereich für die API-Verwaltung fest.

## Parameter

### -ApiId
Gibt den Bezeichner der vorhandenen API an.
Wenn Sie diesen Parameter angeben, legt das Cmdlet die Richtlinie für den API-Bereich fest.

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
Gibt die Instanz von **PsApiManagementContext** an.

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

### -Format
Gibt das Format der Richtlinie an.
Der Standardwert ist "application/vnd. ms-Azure-APIM. Policy + XML".

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
Gibt den Bezeichner des vorhandenen Vorgangs an.
Wenn mit ApiId angegeben, wird die Richtlinie für den Vorgangsbereich festgelegt.
Diese Parameter sind erforderlich.

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
passthru

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

### – Richtlinien
Gibt das Richtliniendokument als Zeichenfolge an.
Dieser Parameter ist erforderlich, wenn die- *PolicyFilePath* nicht angegeben ist.

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

### -PolicyFilePath
Gibt den Pfad der Richtliniendokument Datei an.
Dieser Parameter ist erforderlich, wenn der *Richtlinien* Parameter nicht angegeben ist.

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

### -ProductID
Gibt den Bezeichner des vorhandenen Produkts an.
Wenn dieser Parameter angegeben wird, legt das Cmdlet die Richtlinie für den Produktbereich fest.

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

### bool

## Notizen

## Verwandte Links

[Get-AzureRmApiManagementPolicy](./Get-AzureRmApiManagementPolicy.md)

[Remove-AzureRmApiManagementPolicy](./Remove-AzureRmApiManagementPolicy.md)


