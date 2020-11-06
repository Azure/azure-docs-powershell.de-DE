---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 5273161b18f49e2cfd8f772987d8f0d9ce90bc69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477397"
---
# Set-AzureRmApiManagementProperty

## Synopsis
Ändert eine API-Verwaltungseigenschaft.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tags <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **festlegen-AzureRmApiManagementProperty** " ändert eine Azure API-Verwaltungseigenschaft.

## Beispiele

### Beispiel 1: Ändern der Tags für eine Eigenschaft
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

Der erste Befehl weist der $Tags Variablen zwei Werte zu.

Der zweite Befehl ändert die Eigenschaft mit der ID Property11.
Der Befehl weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.

### Beispiel 2: Ändern einer Eigenschaft, um einen geheimen Wert zu haben
```
PS C:\>Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property12" -Secret $True -PassThru
```

Mit diesem Befehl wird die zu verschlüsselnde Eigenschaft geändert.

## Parameter

### -Context
Gibt ein **PsApiManagementContext** -Objekt an.

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

### -Name
Gibt den Namen der Eigenschaft an.
Die maximale Länge beträgt 100 Zeichen.
Namen enthalten nur Buchstaben, Ziffern, Punkt Zeichen, Striche und Unterstriche.

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

### -PassThru
Gibt an, dass dieses Cmdlet die **PsApiManagementProperty** zurückgibt, die von diesem Cmdlet geändert werden.

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

### -Eigenschafts-Nr
Gibt eine ID der Eigenschaft an, die von diesem Cmdlet geändert wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Gibt an, dass der Eigenschaftswert ein Schlüssel ist und verschlüsselt werden sollte.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tags
Gibt ein Array von Tags an, die dieses Cmdlet der Eigenschaft zuordnet.
Sie können Kategorien verwenden, um die Eigenschaftenliste zu filtern.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wert
Gibt einen Wert für die Eigenschaft an.
Dieser Wert kann Richtlinienausdrücke enthalten.
Die maximale Länge beträgt 1000 Zeichen.
Der Wert darf nicht leer sein oder nur aus Leerzeichen bestehen.

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

### Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty

## Notizen

## Verwandte Links

[Get-AzureRmApiManagementProperty](./Get-AzureRmApiManagementProperty.md)

[Neu – AzureRmApiManagementProperty](./New-AzureRmApiManagementProperty.md)

[Remove-AzureRmApiManagementProperty](./Remove-AzureRmApiManagementProperty.md)


